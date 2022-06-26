<template>
<div>
    <h2 class="text-xl text-center">{{ msg }}</h2>
    <counter-app />
    <color-app msg="This text color can be changed by you ! Please select Any color which you like !" />

    <child :data="name" :info="info" :func="getFunc"/>

</div>
</template>

<script>
import CounterApp from "./CounterApp.vue";
import ColorApp from "./ColorApp.vue";
import Child from "./Child.vue";
export default {
    name: "HelloWorld",
    data() {
        return {
            name: "Rakibul Islam",
            info: {
                age: 30,
                profession: "Web Developer",
            },
        };
    },
    methods: {
        getFunc() {
            alert("This alert from hello world !");
        },
    },
    props: {
        msg: String,
    },
    components: {
        CounterApp,
        ColorApp,
        Child,
    },
};
</script>

<style>

</style>
