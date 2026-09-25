<script setup>
import MainNavigation from './components/MainNavigation.vue'
import SiteFooter from './components/SiteFooter.vue'
import SiteContent from './components/SiteContent.vue'
</script>

<template>
    <header>
        <MainNavigation title="My Vue App" />
    </header>
    <main>
        <SiteContent />
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
