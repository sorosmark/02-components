<script setup>
import { ref } from 'vue';

import MainNavigation from './components/MainNavigation.vue'
import SiteFooter from './components/SiteFooter.vue'
import SiteContent from './components/SiteContent.vue'
import InputField from './components/InputField.vue'

const title = ref('VUE');

setTimeout(() => {
    title.value = 'REACT';
}, 3000);

function logMessage(name) {
    console.log('Input field changed!', name);
}
</script>

<template>
    <header>
        <!-- <MainNavigation title="title" /> -->
        <MainNavigation :title="title" />

    </header>
    <main>
        <SiteContent />
        <InputField @on-input="logMessage" />
    </main>
    <footer>
        <!-- sitefooter komponens hasznalata -->
        <SiteFooter />
    </footer>
</template>

<style scoped>
footer {
    background-color: rgb(182, 40, 182);
    padding: 20px 0;
    border-top: 1px solid #dee2e6;
    text-align: center;
}
</style>
