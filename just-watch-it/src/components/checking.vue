<template>
    <div>
        <div class="h-full  grow flex flex-col justify-center gap-10 items-center">
            <h3>{{ name }}</h3>
            <p>{{ brand }}</p>
            <p>{{ description }}</p>
            <p>${{ price }}</p>
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
                class="m-8 rounded-sm bg-neutral-300 p-2 font-extralight active:translate-y-[2px] border-[1px] border-transparent transition-transform ease-in-out hover:bg-neutral-100 hover:text-black hover:border-neutral-950">
                <h3 style="font-style: italic;">Just Buy It</h3>
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
