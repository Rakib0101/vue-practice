<template>
  <div class="text-center">
    <h2 class="text-4xl mt-8">My Name is {{data}}</h2>
    <p>I am {{info.age}} years old and my profession is {{ info.profession }}</p>
    <button class="border px-2 py-1 rounded-full mt-4" v-on:click="func()">Click Here</button>
  </div>
</template>

<script>
export default {
    props: {
        data: String,
        info: Object,
        func: Function,
    },
};
</script>

<style>

</style>
