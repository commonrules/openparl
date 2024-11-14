<script setup lang="ts">

useHead({
  title: 'Openparl',
})


const links = [{
  label: 'Frontpage',

  to: '/'
}, {
  label: 'Political Discussion',
  to: '/components/horizontal-navigation'
}, {
  label: 'Updates',
}]

const featuredLaws = [{
  owner: 'Bundestag',
  name: 'GG',
  about: 'Grundgesetz für die Bundesrepublik Deutschland',
  to: '/repo1',
  avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/b/b5/Deutscher_Bundestag_logo.svg/800px-Deutscher_Bundestag_logo.svg.png'
}, {
  owner: 'Bundestag',
  name: 'DDG',
  about: 'Digitale-Dienste-Gesetz',
  to: 'https://github.com/vueuse/vueuse',
  avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/b/b5/Deutscher_Bundestag_logo.svg/800px-Deutscher_Bundestag_logo.svg.png'
}, ]

const featuredRepos = [{
  owner: 'mibressler',
  name: 'BayDiGWiki',
  about: 'Wiki für das Bayerische Digitalgesetz',
  to: '/repo2',
  avatar: 'https://avatars.githubusercontent.com/u/53796824?v=4'
}, {
  owner: 'somedude27',
  name: 'openparl-feedback',
  about: 'Wiki für das Bayerische Digitalgesetz',
  to: 'https://github.com/vueuse/vueuse',
  avatar: 'https://avatars.githubusercontent.com/u/53796854?v=4'
},]

const featuredPreprints = [{
  owner: 'Vielmacher, A. et. al.',
  name: 'DAT.24007',
  about: 'Geltungskraft und Geltungsverlust von Rechtsnormen: Elemente einer Theorie der autoritativen Normgeltungsbeendigung',
  to: '/dat.00203',
  avatar: 'https://avatars.githubusercontent.com/u/53796854?v=4'
}, ]
</script>

<template>




<UHorizontalNavigation :links="links" class="mt-10" :ui="{
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

<div class="pb-16 pt-10">

  <ULandingGrid>
    <ULandingCard class="col-span-6 row-span-4" icon="i-heroicons-swatch" title="Privatrecht" description="Choose a primary and a gray color from your Tailwind CSS color palette." />
    <ULandingCard class="col-span-6 row-span-2" icon="i-heroicons-wrench-screwdriver" title="Öffentliches Recht" description="Change the style of any component in your App Config or with ui prop." />
    <ULandingCard class="col-span-6 row-span-2" icon="i-heroicons-face-smile" title="Strafrecht" description="Choose any of the 100k+ icons from the most popular icon libraries." />
  </ULandingGrid>
</div>

<div class="text-4xl rounded-lg mt-2">
        For You
      </div>

      <UPageGrid class="pt-7 pb-10">
    <UPageCard v-for="(module, index) in featuredLaws" :key="index" v-bind="module" class="pt-20 bg-slate-50 max-w-48 ring-0">
      <div>
        <UAvatar :src="module.avatar" class="mb-2.5" />
      </div>
      <div>
        <span class="font-normal">{{ module.owner }}</span>

        / <span class="line-clamp-2 font-semibold text-lg">{{ module.name }}</span>
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

