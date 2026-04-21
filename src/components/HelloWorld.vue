<template>
  <div class="flex h-full w-full items-center justify-center">
    <div class="relative flex h-140 w-70 flex-col items-center rounded-[48px] border border-gray-200 bg-white px-4 py-10 shadow-sm">
      <div class="absolute top-4 h-6 w-24 rounded-full bg-gray-100"></div>
      <div
        class="mt-6 w-full flex-1 overflow-hidden rounded-[36px]"
        style="background-color: #f5f1e8"
      >
        <div class="flex h-full w-full flex-col items-center justify-center gap-4">
          <span style="font-family: Georgia, 'Times New Roman', ui-serif, serif; color: #2b1f1a; font-size: 2rem; font-weight: 500; letter-spacing: -0.01em"
            >hello.</span
          >
          <img
            alt="Vue logo"
            class="logo"
            src="@/assets/logo.svg"
            width="48"
            height="48"
          />
        </div>
      </div>
      <div class="absolute bottom-5 h-1 w-28 rounded-full bg-gray-300"></div>
    </div>
  </div>
</template>

<script lang="ts" setup></script>
