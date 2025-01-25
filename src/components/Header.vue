<script setup>
import { ref } from "vue";
import { RouterLink } from "vue-router";

const isHidden = ref(true);
function toggleMenu() {
    isHidden.value = !isHidden.value;
}
</script>

<template lang="">
    <header class="bg-secondary fixed top-0 left-0 w-full z-50 px-5 py-8">
        <nav
            class="container flex flex-col items-start gap-7 md:flex-row md:items-center relative justify-between"
        >
            <div class="flex justify-between items-center w-full">
                <router-link class="text-2xl uppercase font-bold md:text-3xl" to="/"
                    >Fatma Tawfeek</router-link
                >
                <img
                    src="../components/icons/bars-solid.svg"
                    alt=""
                    class="h-6 w-6 cursor-pointer md:hidden"
                    @click="toggleMenu"
                />
            </div>
            <div id="nav-menu" class="md:block" :class="{ hidden: isHidden }">
                <ul class="flex flex-col gap-7 md:flex-row">
                    <li>
                        <router-link
                            class="text-md font-bold uppercase px-3 py-2"
                            active-class="bg-primary rounded-md"
                            to="/about"
                            >about</router-link
                        >
                    </li>
                    <li>
                        <router-link
                            class="text-md font-bold uppercase px-3 py-2"
                            active-class="bg-primary rounded-md"
                            to="/portfolio"
                            >portfolio</router-link
                        >
                    </li>
                    <li>
                        <router-link
                            class="text-md font-bold uppercase px-3 py-2"
                            active-class="bg-primary rounded-md"
                            to="/contact"
                            >contact</router-link
                        >
                    </li>
                </ul>
            </div>
        </nav>
    </header>
</template>

<style scoped></style>
