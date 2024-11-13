<script setup lang="ts">
const links = [{
  label: 'Frontpage',

  to: '/'
}, {
  label: 'Political Discussion',
  to: '/components/horizontal-navigation'
}, {
  label: 'Updates',
}]

const modules = [{
  owner: 'mibressler',
  name: 'VueUse',
  about: 'Grundgesetz für die Bundesrepublik Deutschland',
  to: 'https://github.com/vueuse/vueuse',
  icon: 'i-simple-icons-nuxtdotjs'
}, {
  title: 'ESLint',
  description: 'ESLint module for Nuxt.',
  to: 'https://github.com/nuxt-community/eslint-module',
  icon: 'i-simple-icons-eslint'
}, ]

</script>

<template>

<a href="https://www.youtube.com/watch?v=sES2J__1PiY">
<div class="relative">
    <Carousel class="mt-10 rounded-3xl"/>
    <div class="absolute inset-0 flex items-end justify-start z-10 m-10">
        <div>
      <div class="text-7xl text-white p-4 rounded-lg">
        Something happens
      </div>
      <div class="text-xl font-bold text-white p-4 pt-0 rounded-lg flex justify-start">
        <div class="mr-4 mt-2 w-3 h-3 bg-red-500 rounded-full animate-flash"></div>
        LIVE
      </div>
      
    </div>
    </div>
  </div>
</a>


<UHorizontalNavigation :links="links" class="mt-5" :ui="{
  wrapper: 'relative w-full flex items-center justify-center',
  container: 'flex items-center min-w-0',
  inner: 'min-w-0',
  base: 'group relative w-full flex items-center gap-1.5 px-2.5 py-3.5 rounded-md font-normal text-sm focus:outline-none focus-visible:outline-none dark:focus-visible:outline-none focus-visible:ring-inset focus-visible:ring-2 focus-visible:ring-primary-500 dark:focus-visible:ring-primary-400 disabled:cursor-not-allowed disabled:opacity-75',
  before: 'before:absolute before:inset-x-0 before:inset-y-2 before:inset-px before:rounded-md hover:before:bg-gray-50 dark:hover:before:bg-gray-800/50',
  after: 'after:absolute after:bottom-0 after:inset-x-2.5 after:block after:h-[2px] after:mt-2',
  active: 'text-gray-900 dark:text-white after:bg-gray-500 dark:after:bg-primary-400 after:rounded-full',
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
"/>

<div class="text-4xl rounded-lg mt-2">
        Featured Repositories
      </div>

      <UPageGrid class="pt-7 pb-10">
    <UPageCard v-for="(module, index) in modules" :key="index" v-bind="module" target="_blank" class="pt-20">
      <div>
        <span class="font-normal">{{ module.owner }}</span>

        / <span class="line-clamp-2 font-semibold">{{ module.name }}</span>
      </div>
      <div>
        <span class="mt-2 line-clamp-2 text-slate-500 text-sm">{{ module.about }}</span>
      </div>
    </UPageCard>
  </UPageGrid>

</template>

<style scoped>
@keyframes flash {
  0%, 100% {
    opacity: 1;
  }
  50% {
    opacity: 0;
  }
}

.animate-flash {
  animation: flash 1s infinite;
}
</style>

