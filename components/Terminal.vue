<script setup lang="ts">
</script>

<template>
  <div class="fixed bottom-0 w-full">
    <UCommandPalette
    :empty-state="null"
    placeholder="Suche"
    class="bg-slate-50 dark:bg-gray-800"
    :close-button="{ icon: 'i-heroicons-arrow-right-end-on-rectangle', color: 'gray', variant: 'link', padded: false }"
  />
  </div>
</template>

