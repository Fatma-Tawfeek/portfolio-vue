<script setup>
import { ref } from "vue";

let imageSrc = ref("");
let isHidden = ref(true);

function displayImageModal(e) {
    isHidden.value = false;
    imageSrc.value = e.currentTarget.children[0].src;
}

function closeImageModal() {
    isHidden.value = true;
}
</script>

<template lang="">
    <section
        class="bg-tertiary text-secondary min-h-full flex flex-col justify-center items-center py-20 text-center"
    >
        <div class="container">
            <h1 class="text-4xl font-bold uppercase mb-3">Portfolio</h1>
            <div class="flex justify-center items-center gap-5 w-75 mx-auto mb-5">
                <div class="w-1/3 h-1 bg-secondary"></div>
                <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" class="w-6">
                    <path
                        fill="#1c2642"
                        d="M316.9 18C311.6 7 300.4 0 288.1 0s-23.4 7-28.8 18L195 150.3 51.4 171.5c-12 1.8-22 10.2-25.7 21.7s-.7 24.2 7.9 32.7L137.8 329 113.2 474.7c-2 12 3 24.2 12.9 31.3s23 8 33.8 2.3l128.3-68.5 128.3 68.5c10.8 5.7 23.9 4.9 33.8-2.3s14.9-19.3 12.9-31.3L438.5 329 542.7 225.9c8.6-8.5 11.7-21.2 7.9-32.7s-13.7-19.9-25.7-21.7L381.2 150.3 316.9 18z"
                    />
                </svg>
                <div class="w-1/3 h-1 bg-secondary"></div>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-3 gap-5">
                <div
                    class="portfolio-item group rounded-lg relative overflow-hidden"
                    @click="displayImageModal($event)"
                >
                    <img
                        src="../assets/portfolio/poert1.png"
                        alt="portfolio-1"
                        class="w-full h-full drop-shadow-md mb-5 rounded-lg"
                    />
                    <div class="layer">
                        <img
                            src="../components/icons/plus-solid.svg"
                            class="w-20 opacity-0 group-hover:opacity-100 transition-all duration-500"
                            alt=""
                        />
                    </div>
                </div>
                <div
                    class="portfolio-item group rounded-lg relative overflow-hidden"
                    @click="displayImageModal($event)"
                >
                    <img
                        src="../assets/portfolio/port2.png"
                        alt="portfolio-1"
                        class="w-full h-full drop-shadow-md mb-5 rounded-lg"
                    />
                    <div class="layer">
                        <img
                            src="../components/icons/plus-solid.svg"
                            class="w-20 opacity-0 group-hover:opacity-100 transition-all duration-500"
                            alt=""
                        />
                    </div>
                </div>
                <div
                    class="portfolio-item group rounded-lg relative overflow-hidden"
                    @click="displayImageModal"
                >
                    <img
                        src="../assets/portfolio/port3.png"
                        alt="portfolio-1"
                        class="w-full h-full drop-shadow-md mb-5 rounded-lg"
                    />
                    <div class="layer">
                        <img
                            src="../components/icons/plus-solid.svg"
                            class="w-20 opacity-0 group-hover:opacity-100 transition-all duration-500"
                            alt=""
                        />
                    </div>
                </div>
                <div
                    class="portfolio-item group rounded-lg relative overflow-hidden"
                    @click="displayImageModal"
                >
                    <img
                        src="../assets/portfolio/poert1.png"
                        alt="portfolio-1"
                        class="w-full h-full drop-shadow-md mb-5 rounded-lg"
                    />
                    <div class="layer">
                        <img
                            src="../components/icons/plus-solid.svg"
                            class="w-20 opacity-0 group-hover:opacity-100 transition-all duration-500"
                            alt=""
                        />
                    </div>
                </div>
                <div
                    class="portfolio-item group rounded-lg relative overflow-hidden"
                    @click="displayImageModal"
                >
                    <img
                        src="../assets/portfolio/port2.png"
                        alt="portfolio-1"
                        class="w-full h-full drop-shadow-md mb-5 rounded-lg"
                    />
                    <div class="layer">
                        <img
                            src="../components/icons/plus-solid.svg"
                            class="w-20 opacity-0 group-hover:opacity-100 transition-all duration-500"
                            alt=""
                        />
                    </div>
                </div>
                <div
                    class="portfolio-item group rounded-lg relative overflow-hidden"
                    @click="displayImageModal"
                >
                    <img
                        src="../assets/portfolio/port3.png"
                        alt="portfolio-1"
                        class="w-full h-full drop-shadow-md mb-5 rounded-lg"
                    />
                    <div class="layer">
                        <img
                            src="../components/icons/plus-solid.svg"
                            class="w-20 opacity-0 group-hover:opacity-100 transition-all duration-500"
                            alt=""
                        />
                    </div>
                </div>
            </div>
        </div>
    </section>
    <section
        class="fixed top-0 left-0 w-full h-full bg-primary/20 flex justify-center items-center"
        :class="{ hidden: isHidden }"
        @click="closeImageModal($event)"
    >
        <div class="container">
            <img :src="imageSrc" class="md:w-1/2 mx-auto" alt="" @click.stop />
        </div>
    </section>
</template>

<style lang=""></style>
