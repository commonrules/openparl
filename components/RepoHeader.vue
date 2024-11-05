<script setup lang="ts">
import type { NavItem } from '@nuxt/content'

const navigation = inject<Ref<NavItem[]>>('navigation', ref([]))

const links = [{
  label: 'Content',
  icon: 'i-heroicons-book-open',
  to: '/getting-started'
}, {
  label: 'Pull Requests',
  icon: 'i-heroicons-square-3-stack-3d',
  to: '/pro'
}, {
  label: 'Discussion',
  icon: 'i-heroicons-rocket-launch',
  to: '/releases'
},{
  label: 'Legislative Activity',
  icon: 'i-heroicons-rocket-launch',
  to: '/releases'
}]
</script>

<template>
  <UHeader>
    <template #logo>
      <Logo class="w-auto h-6" />
    </template>

    <template #left>
        <div>Bundestag</div>
        /
        <div>GG</div>
    </template>

    <template #right>

      <Avatar />
    </template>

  </UHeader>

  <div class="text-2xl">Grundgesetz</div>

  <UHorizontalNavigation :links="links" class="border-b border-gray-200 dark:border-gray-800" />

</template>

