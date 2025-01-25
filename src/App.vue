<script setup>
import { RouterView } from "vue-router";
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
</script>

<template>
    <!-- Header  -->
    <Header />
    <!-- Content  -->
    <main>
        <RouterView />
    </main>

    <!-- Footer  -->
    <Footer />
</template>

<style scoped></style>
