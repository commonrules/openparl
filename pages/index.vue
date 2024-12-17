<script setup lang="ts">

useHead({
  title: 'Rechtsprechungsdatenbank',
})



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
}]


</script>

<template>

<div class="pb-10 pt-10">

  <ULandingGrid>
    <ULandingCard class="col-span-6 row-span-4" icon="i-heroicons-swatch" title="Privatrecht" description="Choose a primary and a gray color from your Tailwind CSS color palette." color="blue"/>
    <ULandingCard class="col-span-6 row-span-2" icon="i-heroicons-wrench-screwdriver" title="Öffentliches Recht" description="Change the style of any component in your App Config or with ui prop." color="blue"/>
    <ULandingCard class="col-span-6 row-span-2" icon="i-heroicons-face-smile" title="Strafrecht" description="Choose any of the 100k+ icons from the most popular icon libraries." color="blue" />
  </ULandingGrid>
</div>
<UIcon name="i-heroicons-folder-open" class="w-5 h-5 mb-4 mt-5 text-slate-400" />
<div class="pb-12 flex justify-start gap-5">
<UButton size="xl" variant="soft"  to="/repo1" class="bg-slate-100">GG
</UButton>
<UButton size="xl" variant="soft"  to="/repo1" class="bg-slate-100">BGB
</UButton>
<UButton size="xl" variant="soft"  to="/repo1" class="bg-slate-100">DDG
</UButton>
<UButton size="xl" variant="soft"  to="/repo1" class="bg-slate-100">Digitale-D-G
</UButton>
<UButton size="xl" variant="soft"  to="/repo1" class="bg-slate-100">HormBetrG
</UButton>
<UButton size="xl" variant="soft"  to="/repo1" class="bg-slate-100">SGB
</UButton>

</div>

<div class="text-4xl rounded-lg mt-8">
        Urteile
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

