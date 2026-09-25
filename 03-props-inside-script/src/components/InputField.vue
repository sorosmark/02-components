<script setup>
    defineEmits(['on-input']);
</script>

<template>
    <input type="text" placeholder="Type something..." @click="$emit('on-input')" />

</template>

<style scoped>
</style>
