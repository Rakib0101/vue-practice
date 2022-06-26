<template>
<div class="w-1/2 mx-auto shadow-md border p-8 mt-4">
    <h2 class="text-xl text-center pt-4">Counter App</h2>
    <div class="flex justify-center my-8">
        
        <button class="border rounded bg-red-700 text-white px-2 py-1" v-on:click="decreement()">Decreement (-1)</button>
        <h3 class="text-4xl text-center mx-4">Count: {{count}}</h3>
        <button class="border rounded bg-green-700 text-white px-2 py-1" v-on:click="increement()">Increement (+1)</button>
    </div>
</div>
</template>

<script>
export default {
    data() {
        return {
            count: 0,
        };
    },
    methods: {
        increement() {
            this.count = this.count + 1;
        },
        decreement() {
            if (this.count > 0) {
                this.count = this.count - 1;
            }
        },
    },
};
</script>

<style>

</style>
