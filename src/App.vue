<template>
  <div class="flex min-h-screen w-full flex-col items-center justify-center gap-12 bg-orange-300">
    <div class="flex w-3/5 flex-col items-center justify-center gap-12">
      <RouterView />
    </div>

    <div class="flex w-96 flex-col items-center justify-center gap-6 text-orange-900">
      <p class="text-center text-lg">This is a starter kit using several, as usefull concidered technologies for developing an universal app as like:</p>
      <p class="flex gap-3 text-center text-base">
        <a
          v-for="(link, i) in links"
          :key="i"
          :href="link.url"
          target="_blank"
          rel="noopener"
          class="min-w-fit text-orange-900 underline after:text-white after:content-[','] last:after:content-['.']"
        >
          {{ link.text }}
        </a>
      </p>
    </div>
  </div>
</template>

<script lang="ts" setup>
const links = [
  { url: 'https://vuejs.org/', text: 'Vue 3' },
  { url: 'https://capacitorjs.com/"', text: 'Capacitor' },
  { url: 'https://www.typescriptlang.org/', text: 'TypeScript' },
  { url: 'https://tailwindcss.com/', text: 'Tailwindcss' },
  { url: 'https://pinia.vuejs.org/', text: 'Pinia' },
  { url: 'https://vitejs.dev/', text: 'Vite' },
  { url: 'https://oxc.rs/', text: 'Oxc' },
];
</script>
