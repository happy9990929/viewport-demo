<template>
  <header class="absolute w-full top-0 text-lg">
    <ul class="flex items-center justify-center bg-slate-500 text-white space-x-6 h-14 font-bold">
      <li>
        <router-link
          :to="{query: { type: 'vh'}}">100vh</router-link>
      </li>
      <li>
        <router-link
        :to="{query: { type: 'lvh' }}">100lvh</router-link>
      </li>
      <li>
        <router-link
          :to="{query: { type: 'svh'}}">100svh</router-link>
      </li>
      <li>
        <router-link
        :to="{query: { type: 'dvh' }}">100dvh</router-link>
      </li>
    </ul>
  </header>

</template>