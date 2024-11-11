<script setup lang="ts">


const links = [
  [{
  label: 'Gesetzestext',
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
}], [{
    label: 'Open in Patina',
    labelClass: 'bg-gray-600 text-white pr-3 pl-3 pt-1 pb-1 rounded-md mb-0 mt-0',
  }, {
    icon: 'i-heroicons-heart'
  },{
    icon: 'i-heroicons-ellipsis-vertical'
   }]
]

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
  
  <div class="flex justify-end">
    <div class="w-1/3">
    </div>
    <div class="w-2/3">
  <UHorizontalNavigation :ui="{
    wrapper: 'relative w-full flex items-center justify-between',
    container: 'flex items-center min-w-0',
    inner: 'min-w-0',
    base: 'group relative w-full flex items-center gap-1.5 px-2.5 py-3.5 rounded-md font-medium text-sm focus:outline-none focus-visible:outline-none dark:focus-visible:outline-none focus-visible:ring-inset focus-visible:ring-2 focus-visible:ring-primary-500 dark:focus-visible:ring-primary-400 disabled:cursor-not-allowed disabled:opacity-75',
    before: 'before:absolute before:inset-x-0 before:inset-y-2 before:inset-px before:rounded-md hover:before:bg-gray-50 dark:hover:before:bg-gray-800/50',
    after: 'after:absolute after:bottom-0 after:inset-x-2.5 after:block after:h-[2px] after:mt-2',
    active: 'text-gray-900 dark:text-white after:bg-[linear-gradient(266deg,rgba(252,211,77,1)0%,rgba(252,211,77,1)33%,rgba(220,38,38,1)33%,rgba(220,38,38,1)66%,rgba(10,10,10,1)66%,rgba(10,10,10,1)100%)] dark:after:bg-primary-400 after:rounded-full',
    inactive: 'text-gray-500 dark:text-gray-400 hover:text-gray-900 dark:hover:text-white',
    label: 'truncate relative',
    icon: {
      base: 'flex-shrink-0 w-5 h-5 relative',
      active: 'text-gray-700 dark:text-gray-200',
      inactive: 'text-gray-400 dark:text-gray-500 group-hover:text-gray-700 dark:group-hover:text-gray-200'
    },
    avatar: {
      base: 'flex-shrink-0',
      size: '2xs'
    },
    badge: {
      base: 'flex-shrink-0 ms-auto relative rounded',
      color: 'gray',
      variant: 'solid',
      size: 'xs'
    }
  }
  " :links="links"  class="pl-5 bg-slate-50"/>
</div>
</div>
  </template>

<style scoped>
.no-border {
  border-bottom: none;
}

</style>