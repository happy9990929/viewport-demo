<script setup>
import { computed } from "vue";
import { useRoute } from "vue-router";

const route = useRoute();
const type = computed(() => route.query.type);
const height = computed(() => {
  if(type.value === 'vh') return 'h-screen';
  if(type.value === 'svh') return 'h-svh';
  if(type.value === 'dvh') return 'h-dvh';
  if(type.value === 'lvh') return 'h-lvh';

  return 'h-screen';
})

const title = computed(() => {
  if(type.value === 'vh') return '100vh';
  if(type.value === 'svh') return '100svh';
  if(type.value === 'dvh') return '100dvh';
  if(type.value === 'lvh') return '100lvh';
  return '100vh';
})
</script>

<template>
  <main class="h-full">
    <section class="p-4 pt-20" :class="height">
      <div class="rounded-3xl bg-amber-100 p-6 text-lg h-full">
        <h1 class="text-center font-black text-3xl  mb-3">{{ title }}</h1>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat quam rerum, doloremque amet harum illum ipsam numquam quisquam quae recusandae repudiandae, minima optio corrupti doloribus atque dolor magni incidunt in!
      </div>
    </section>

    <section class="bg-amber-200 p-4 mt-10">
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Fugiat quam rerum, doloremque amet harum illum ipsam numquam quisquam quae recusandae repudiandae, minima optio corrupti doloribus atque dolor magni incidunt in!
    </section>
  </main>
</template>
