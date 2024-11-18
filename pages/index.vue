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
const featuredRepos = [{
  owner: 'Bundestag',
  name: 'GG',
  about: 'Grundgesetz für die Bundesrepublik Deutschland',
  to: '/repo1',
  avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/b/b5/Deutscher_Bundestag_logo.svg/800px-Deutscher_Bundestag_logo.svg.png',
  nopreprint: '/',
}, {
  owner: 'Bundestag',
  name: 'DDG',
  about: 'Digitale-Dienste-Gesetz',
  to: 'https://github.com/vueuse/vueuse',
  avatar: 'https://upload.wikimedia.org/wikipedia/commons/thumb/b/b5/Deutscher_Bundestag_logo.svg/800px-Deutscher_Bundestag_logo.svg.png',
  nopreprint: '/',
}, {
  owner: 'mibressler',
  name: 'BayDiGWiki',
  about: 'Wiki für das Bayerische Digitalgesetz',
  to: '/repo2',
  avatar: 'https://avatars.githubusercontent.com/u/53796824?v=4',
  nopreprint: '/',
}, {
  owner: 'somedude27',
  name: 'openparl-feedback',
  about: 'Wiki für das Bayerische Digitalgesetz',
  to: 'https://github.com/vueuse/vueuse',
  avatar: 'https://avatars.githubusercontent.com/u/53796854?v=4',
  nopreprint: '/',
}, {
  owner: 'Vielmacher, A. et. al.',
  name: 'DAT.24007',
  about: 'Geltungskraft und Geltungsverlust von Rechtsnormen: Elemente einer Theorie der autoritativen Normgeltungsbeendigung',
  to: '/dat.00203',
  avatar: 'https://avatars.githubusercontent.com/u/53796854?v=4',
  preprintname: 'Vielmacher, A. et. al',
  preprintabout: 'Vielmacher, A. et. al'
},]



const feedsort = [ {
  label: 'For You',
  icon: 'i-heroicons-square-3-stack-3d',
  to: '/pro',
  children: [{
    label: 'For You',
    to: '/pro/pricing',
    icon: 'i-heroicons-heart',
    description: 'See our algorithm <here>.'
  }, {
    label: 'Following',
    to: '/pro/templates',
    icon: 'i-heroicons-queue-list',
    description: 'Chronologically sorted feed.'
  }]
}, ]
</script>

<template>


<a href="https://www.youtube.com/watch?v=sES2J__1PiY">
<div class="relative">
    <Carousel class="mt-10 rounded-3xl"/>
    <div class="absolute inset-0 flex items-end justify-start z-10 m-10">
        <div>
      <div class="text-7xl text-white p-4 rounded-lg">
        200. Sitzung des Deutschen Bundestages
      </div>
      <div class="text-xl font-bold text-white p-4 pt-0 rounded-lg flex justify-start">
        <div class="mr-4 mt-2 w-3 h-3 bg-red-500 rounded-full animate-flash"></div>
        LIVE
      </div>
      
    </div>
    </div>
  </div>
</a>

<UIcon name="i-heroicons-arrow-uturn-left" class="w-5 h-5 mb-4 mt-16 text-slate-400" />
<div class="pb-5 flex justify-start gap-5">
<UButton size="xl" variant="soft"  to="/repo1" class="bg-slate-100"><span class="text-slate-400">mibressler/</span><span>GG</span>
  <template #leading>
      <UAvatar
        src="https://pbs.twimg.com/profile_images/1295402247640227840/EyEx_ve9_400x400.jpg"
        size="2xs"
      />
    </template>
</UButton>
<UButton size="xl" variant="soft"  to="/repo1" class="bg-slate-100">BGB
</UButton>
<UButton size="xl" variant="soft"  to="/repo1" class="bg-slate-100">Digitale-D-G
</UButton>
<UButton size="xl" variant="soft"  to="/repo1" class="bg-slate-100"><span class="text-slate-400">openparl:</span><span>DAT.24007</span>
  <template #leading>
      <UAvatar
        src="http://localhost:3000/logoblack.png"
        size="2xs"
      />
    </template>
</UButton>
<UButton size="xl" variant="soft"  to="/repo1" class="bg-slate-100"><span class="text-slate-400">beck:</span><span>KIR 2024, 77</span>
  <template #leading>
      <UAvatar
        src="https://presse.beck.de/media/2ileyyfj/chbeck-bildmarke.jpg"
        size="2xs"
      />
    </template>
</UButton>
<UButton size="xl" variant="soft"  to="/repo1" class="bg-slate-100">GG
</UButton>


</div>


<div class="flex justify-between">

      <div class="text-4xl rounded-lg mt-8">
        Feed  (Activity, new repos, discussion, new legislation activity, rulings) </div>


      

      <UHeaderLinks :links="feedsort" />



  </div>



<div class="text-4xl rounded-lg mt-8">
        Featured Repositories
      </div>

      <UPageGrid class="pt-7 pb-10" :ui="{
  wrapper: 'grid grid-cols-1 sm:grid-cols-2 xl:grid-cols-3 2xl:grid-cols-6 gap-8'
}">
    <UPageCard v-for="(module, index) in featuredRepos" :key="index" v-bind="module" class="pt-20 bg-slate-50 ring-0">
      <div>
        <UAvatar :src="module.avatar" class="mb-2.5" />
      </div>
      <div>
        <span class="font-normal">{{ module.owner }}</span>

        <span> &nbsp;{{ module.nopreprint }}</span> <span class="line-clamp-2 font-semibold text-lg">{{ module.name }}</span>
      </div>
      <div>
        <span class="mt-2 line-clamp-2 text-slate-500 text-sm">{{ module.about }}</span>
      </div>
  
    </UPageCard>
  </UPageGrid>





  <div class="text-4xl rounded-lg mt-8">
        For You
      </div>

      <UPageGrid class="pt-7 pb-10" :ui="{
  wrapper: 'grid grid-cols-1 sm:grid-cols-2 xl:grid-cols-3 2xl:grid-cols-6 gap-8'
}">
    <UPageCard v-for="(module, index) in featuredRepos" :key="index" v-bind="module" class="pt-20 bg-slate-50 ring-0">
      <div>
        <UAvatar :src="module.avatar" class="mb-2.5" />
      </div>
      <div>
        <span class="font-normal">{{ module.owner }}</span>

        <span> &nbsp;{{ module.nopreprint }}</span> <span class="line-clamp-2 font-semibold text-lg">{{ module.name }}</span>
      </div>
      <div>
        <span class="mt-2 line-clamp-2 text-slate-500 text-sm">{{ module.about }}</span>
      </div>
  
    </UPageCard>
  </UPageGrid>




  <div class="flex justify-between">
    <div class="w-1/2">
      <div class="text-4xl rounded-lg mt-8">
        Box
      </div>

    </div>
    <div class="w-1/2">
      <div class="text-4xl rounded-lg mt-8">
        Changelog
      </div>

    </div>

  </div>



  

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

