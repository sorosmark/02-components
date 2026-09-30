<script setup>

import MainNavigation from './components/MainNavigation.vue'
import SiteFooter from './components/SiteFooter.vue'
import SiteContent from './components/SiteContent.vue'
import InputField from './components/InputField.vue'

// function logMessage(name) {
//     console.log('Input field changed!', name);
// }

const submitForm = () => {
    console.log('Form submitted!', formdata);
    console.log('Form submitted!', JSON.stringify(formdata));
};

const formdata = reactive({
    email: '',
    firstname: '',
    lastname: ''
});
</script>

<template>
    <header>
        <MainNavigation/>

    </header>
    <main>
        <SiteContent />
        <!-- email input -->
        <InputField 
        :modelValue="formdata.email"
        id="e-mail"
        type="email"
        placeholder="Type your e-mail..."
        label="E-mail address"/>

        <!-- firstname -->
        <InputField 
        :modelValue="formdata.firstname"
        id="firstname"
        type="text"
        placeholder="Type your first name..."
        label="First name"/>


        <!-- lastname -->
        <InputField 
        :modelValue="formdata.lastname"
        id="lastname"
        type="text"
        placeholder="Type your last name..."
        label="Last name"/>

        <button @click="submitForm">Submit</button>
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
