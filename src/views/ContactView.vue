<template lang="">
    <section
        class="bg-tertiary text-secondary min-h-full flex flex-col justify-center items-center py-20"
    >
        <div class="container">
            <h1 class="text-4xl font-bold uppercase mb-3 text-center">Contact Me</h1>
            <div class="flex justify-center items-center gap-5 w-75 mx-auto">
                <div class="w-1/3 h-1 bg-secondary"></div>
                <div class="mb-5">
                    <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 576 512" class="w-6">
                        <path
                            fill="#1c2642"
                            d="M316.9 18C311.6 7 300.4 0 288.1 0s-23.4 7-28.8 18L195 150.3 51.4 171.5c-12 1.8-22 10.2-25.7 21.7s-.7 24.2 7.9 32.7L137.8 329 113.2 474.7c-2 12 3 24.2 12.9 31.3s23 8 33.8 2.3l128.3-68.5 128.3 68.5c10.8 5.7 23.9 4.9 33.8-2.3s14.9-19.3 12.9-31.3L438.5 329 542.7 225.9c8.6-8.5 11.7-21.2 7.9-32.7s-13.7-19.9-25.7-21.7L381.2 150.3 316.9 18z"
                        />
                    </svg>
                </div>
                <div class="w-1/3 h-1 bg-secondary"></div>
            </div>
            <form class="md:w-3/4 mx-auto" @submit.prevent="onSubmit">
                <label
                    for="name"
                    class="text-primary relative top-7 left-0 transition-all duration-500"
                    >Name:</label
                >
                <input
                    type="text"
                    placeholder="Name"
                    id="name"
                    class="relative w-full p-2 mb-3 outline-none border-b-1 border-primary/50 bg-tertiary"
                    @input="displayLabel($event)"
                />
                <label
                    for="name"
                    class="text-primary relative top-7 left-0 transition-all duration-500"
                    >Email:</label
                >
                <input
                    type="email"
                    placeholder="Email"
                    class="w-full p-2 mb-3 outline-none border-b-1 border-primary/50 relative bg-tertiary"
                    @input="displayLabel($event)"
                />
                <label
                    for="name"
                    class="text-primary relative top-7 left-0 transition-all duration-500"
                    >Message:</label
                >
                <textarea
                    name=""
                    id=""
                    rows="5"
                    placeholder="Message"
                    class="w-full p-2 mb-3 outline-none border-b-1 border-primary/50 relative bg-tertiary"
                    @input="displayLabel($event)"
                ></textarea>
                <button
                    class="bg-primary hover:bg-[#bf332f] text-tertiary text-bold rounded-md py-2 px-5 cursor-pointer"
                    type="submit"
                >
                    Send Message
                </button>
            </form>
        </div>
    </section>
</template>
<script setup>
function displayLabel(event) {
    const input = event.target;
    const label = input.previousElementSibling;
    if (input.value) {
        label.classList.replace("top-7", "top-0");
    } else {
        label.classList.replace("top-0", "top-7");
    }
}
</script>
<style lang=""></style>
