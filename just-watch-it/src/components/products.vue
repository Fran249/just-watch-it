
<template>
  <section class="w-full min-h-screen flex justify-center items-center flex-wrap py-20 gap-16">
    <div v-for="watch in data" :key="watch.name" class="w-full max-w-sm bg-white border border-gray-200 shadow dark:bg-gray-800 dark:border-gray-700">
      <a href="#">
        <img class="p-8 rounded-t-lg" src="https://picsum.photos/500/300?grayscale" alt="product image" />
      </a>
      <div class="px-5 pb-5">
        <h5 class="text-xl font-semibold tracking-tight text-gray-900 dark:text-white">
         {{watch.name}}
        </h5>

        <div class="flex items-center mt-2.5 mb-5">
          <button>
            <slot slot="icon"></slot>
          </button>
          <span class="bg-neutral-300 text-black-800 text-xs font-semibold mr-2 px-2.5 py-0.5 rounded   ml-3">
            {{watch.likes}}
          </span>
        </div>
        <div class="flex items-center justify-between">
          <span class="text-3xl font-bold text-gray-900 dark:text-white">
            ${{watch.price}}
          </span>
          <a href="#" class="text-neutral-950 w-20 h-15 bg-neutral-100 text-center p-1 border-neutral-950 border-[1px]"
            style="font-style: italic;">
            <h3>Just Buy it</h3>
          </a>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>

const props = defineProps({
  data: Array,
})

</script>
<style>
@font-face {
  font-family: "just-do-it";
  src: url(just-do-it-font.otf);
}

h1 {
  font-family: "just-do-it";
}
</style>
