<script setup lang="ts">
import type { NavItem } from '@nuxt/content'

const navigation = inject<Ref<NavItem[]>>('navigation', ref([]))

const items = [
 [{
    label: 'Normzitat',
    icon: 'i-heroicons-pencil-square-20-solid',
    shortcuts: ['E'],
    click: () => {
      console.log('Edit')
    }
  }, {
    label: 'Link',
    icon: 'i-heroicons-document-duplicate-20-solid',
    shortcuts: ['D'],
  }, {
    label: 'Open in new tab',
    icon: 'i-heroicons-document-duplicate-20-solid',
    shortcuts: ['D'],
  }]
]

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
class="no-border group"
>
    <template #logo>
      <Logo class="w-auto h-6" />
    </template>

    <template #left>

      
        <div class="hover:bg-slate-50 hover:rounded px-1">Bundestag</div>
        /
        <div class="hover:bg-slate-50 hover:rounded px-1">GG</div>
        <div class="hover:bg-slate-50 hover:rounded px-1 text-slate-400">
          Art. 1 Abs. 2 S. 1</div>
  

      <UDropdown :items="items" mode="hover" :popper="{ placement: 'right-start' }">
        <UIcon name="i-heroicons-chevron-right" class=" w-4 h-4 opacity-0 group-hover:opacity-100 transition-opacity duration-300" />
  </UDropdown>



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
