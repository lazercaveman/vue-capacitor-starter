<template>
  <HelloWorld :links="technologies" />
</template>


<script lang="ts" setup>
import HelloWorld from '@/components/HelloWorld.vue'

const technologies = [
  { url: 'https://vuejs.org/', text: 'Vue 3' },
  { url: 'https://capacitorjs.com/"', text: 'Capacitor' },
  { url: 'https://www.typescriptlang.org/', text: 'TypeScript' },
  { url: 'https://tailwindcss.com/', text: 'Tailwindcss' },
  { url: 'https://pinia.vuejs.org/', text: 'Pinia' },
  { url: 'https://vitejs.dev/', text: 'Vite' },
]

</script>
