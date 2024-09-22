<template>
  <div class="relative rounded-full border border-neutral-400 px-2 py-2">
    <div class="border border-green-500 rounded-full px-7 py-7 bg-lime-800 bg-opacity-10">
      <img :src="src" alt="icon" />
    </div>
  </div>
</template>

<script setup>
defineProps(['src']);
</script>
