<template>
    <div class="mt-5">
        <div class="h-full  grow flex flex-col justify-center gap-3 md:gap-10 items-center">
            <div class="flex justify-center items-center gap-5">
                <button class="active:translate-y-[2px]" @click="quantity === 0 ? quantity = 0 : quantity--">
                    <slot name="minus-icon"></slot>
                </button>
                <p>{{ quantity }}</p>
                <button class="active:translate-y-[2px]" @click="quantity++">
                    <slot name="plus-icon"></slot>
                </button>
            </div>
            <button
                class="dark:bg-white dark:text-gray-900 dark:hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-offset-2 focus:ring-gray-800 text-base flex items-center justify-center leading-none text-white bg-gray-800 w-full py-4 hover:bg-gray-700 focus:outline-none">
                <h1 style="font-style: italic;">Just Buy It</h1>
            </button>
        </div>

    </div>
</template>

<script setup>

defineProps({
    name: String,
    brand: String,
    description: String,
    price: Number,
    quantity: Number,
})

</script>


<style scoped>
@font-face {
    font-family: "just-do-it";
    src: url(just-do-it-font.otf);
}

h3,
p {
    font-family: "just-do-it";
}
</style>
