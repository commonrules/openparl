<script setup lang="ts">
definePageMeta({
  layout: 'repo'
})

const links = [{
  label: 'Content',
  icon: 'i-heroicons-book-open',
  to: '/repo1'
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

<UPageHeader :ui="{
  wrapper: 'relative pt-2',
  container: 'flex flex-col lg:flex-row lg:items-center lg:justify-between',
  headline: 'mb-3 text-sm/6 font-semibold text-primary flex items-center gap-1.5',
  title: 'text-2xl sm:text-3xl font-normal text-gray-900 dark:text-white tracking-tight',
  description: 'mt-4 text-lg text-gray-500 dark:text-gray-400',
  icon: {
    wrapper: 'flex',
    base: 'w-10 h-10 flex-shrink-0 text-primary'
  },
  links: 'flex flex-wrap items-center gap-1.5 mt-4 lg:mt-0'

}"
title="Grundgesetz für die Bundesrepublik Deutschland"
class="pl-8 no-border mt-0 pt-0 pb-5 bg-slate-50"
/>


<UHorizontalNavigation :links="links"  class="pl-5 bg-slate-50"/>

</template>

<style scoped>
.no-border {
  border-bottom: none;
}
</style>