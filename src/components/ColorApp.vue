<template>
<div class="w-2/3 mx-auto shadow-md rounded-xl border p-8 mt-4">
    <h2 class="text-4xl text-center pt-4">Color App</h2>
    <div class="flex flex-col my-8">
        <div class="w-full text-center">
            <button class="p-2 bg-red-700 m-2 active:bg-pink-800" v-on:click="red()"></button>
            <button class="p-2 bg-blue-700 m-2" v-on:click="blue()"></button>
            <button class="p-2 bg-green-700 m-2" v-on:click="green()"></button>
            <button class="p-2 bg-gray-700 m-2" v-on:click="gray()"></button>
            <button class="p-2 bg-orange-700 m-2" v-on:click="orange()"></button>
            <button class="p-2 bg-violet-700 m-2" v-on:click="violet()"></button>
        </div>
        <div class="w-full text-center">
            <h2 class="text-2xl" 
            v-bind:class="{ 
                'text-red-700' : isRed,
                'text-blue-700' : isBlue,
                'text-green-700' : isGreen,
                'text-gray-700' : isGray,
                'text-orange-700' : isOrange,
                'text-violet-700' : isViolet,
             }">{{ msg }}</h2>
        </div>
    </div>
</div>
</template>

<script>
export default {
    props: {
        msg: String,
    },
    data() {
        return {
            isRed: false,
            isBlue: false,
            isGreen: false,
            isGray: false,
            isOrange: false,
            isViolet: false,
        };
    },
    methods: {
        red() {
            this.isRed = true;
            this.isBlue = false;
            this.isGreen = false;
            this.isGray = false;
            this.isOrange = false;
            this.isViolet = false;
        },
        blue() {
            this.isRed = false;
            this.isBlue = true;
            this.isGreen = false;
            this.isGray = false;
            this.isOrange = false;
            this.isViolet = false;
        },
        green() {
            this.isRed = true;
            this.isBlue = false;
            this.isGreen = true;
            this.isGray = false;
            this.isOrange = false;
            this.isViolet = false;
        },
        gray() {
            this.isRed = false;
            this.isBlue = false;
            this.isGreen = false;
            this.isGray = true;
            this.isOrange = false;
            this.isViolet = false;
        },
        orange() {
            this.isRed = false;
            this.isBlue = false;
            this.isGreen = false;
            this.isGray = false;
            this.isOrange = true;
            this.isViolet = false;
        },
        violet() {
            this.isRed = false;
            this.isBlue = false;
            this.isGreen = false;
            this.isGray = false;
            this.isOrange = false;
            this.isViolet = true;
        },
    },
};
</script>

<style>

</style>
