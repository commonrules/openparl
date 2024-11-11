<script setup lang="ts">
import type { NavItem } from '@nuxt/content'

const navigation = inject<Ref<NavItem[]>>('navigation', ref([]))


</script>

<template>
  <UHeader :ui="{
  wrapper: 'bg-background/75 backdrop-blur px sticky top-0 z-50',
  container: 'flex items-center justify-between gap-3 h-[--header-height]',
  left: 'lg:flex-1 flex items-center gap-1.5',
  center: '',
  right: 'flex items-center justify-end lg:flex-1 gap-1.5',
  logo: 'flex-shrink-0 font-bold text-xl text-gray-900 dark:text-white flex items-end gap-1.5',
  panel: {
    wrapper: 'fixed inset-0 z-50 overflow-y-auto bg-background lg:hidden',
    header: 'px-4 sm:px-6',
    body: 'px-4 sm:px-6 pt-3 pb-6',
  },
  button: {
    base: 'lg:hidden',
    icon: {
      open: 'i-heroicons-bars-3-20-solid',
      close: 'i-heroicons-x-mark-20-solid'
    }
  }
}
"
class="no-border"
>
    <template #logo>
      <Logo class="w-auto h-6" />
    </template>

    <template #left>
        <div>Bundestag</div>
        /
        <div>GG</div>
    </template>

    <template #center>

    </template>

    <template #right>

      <Avatar />
      
    </template>


  </UHeader>


  



</template>

<style scoped>
.no-border {
  border-bottom: none;
}
</style>
