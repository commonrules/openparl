<script setup lang="ts">
import type { NavItem } from '@nuxt/content'

const navigation = inject<Ref<NavItem[]>>('navigation', ref([]))

const links = [{
  label: 'Docs',
  icon: 'i-heroicons-book-open',
  to: '/getting-started'
}, {
  label: 'Pro',
  icon: 'i-heroicons-square-3-stack-3d',
  to: '/pro'
}, {
  label: 'Releases',
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
    </template>

    <template #right>

      <Avatar />
    </template>

  </UHeader>
</template>

