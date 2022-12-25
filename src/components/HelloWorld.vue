<template>
  <div  class="w-96 text-gray-300">
    <h1 class="mb-8 text-3xl text-green-400 text-center"> Vue Capacitor Starter </h1>
    <p class="mb-6 text-lg text-center">
      This is a starter kit using several, as usefull concidered technologies for developing an universal app as like:
    </p>
    <p class="flex gap-3 text-base text-center">
      <a 
        v-for="(link, i) in links"
        :key="i"
        :href="link.url" 
        target="_blank" 
        rel="noopener" 
        class="min-w-fit text-yellow-400 underline after:text-white after:content-[','] last:after:content-['.']"
      >
          {{link.text}}
      </a>
    </p>
  </div>
</template>



<script lang="ts" setup>
import { defineProps } from 'vue';

type TechnologiesType = Array<{
  url: string,
  text: string,
}>

defineProps<{ 
  links: TechnologiesType 
}>();

</script>
