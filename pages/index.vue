<script setup lang="ts">

useHead({
  title: 'Rechtsprechungsdatenbank',
})

import { ref, onMounted } from 'vue';
import { createClient } from '@supabase/supabase-js';

// Initialize Supabase client
const supabaseUrl = 'https://klehrshrqiyqmwctddjr.supabase.co'; // Replace with your project URL
const supabaseKey = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6ImtsZWhyc2hycWl5cW13Y3RkZGpyIiwicm9sZSI6ImFub24iLCJpYXQiOjE3MzI5ODg2MDIsImV4cCI6MjA0ODU2NDYwMn0.BJq9hVM-H2MFccf9v2vByAzrFKhWVvgR5zFEgAg-iVk'; // Replace with your anon key
const supabase = createClient(supabaseUrl, supabaseKey);

// Reactive data for court rulings
const rulings = ref([]);

// Fetch data when the component is mounted
const fetchRulings = async () => {
  try {
    const { data, error } = await supabase
      .from('court_rulings')
      .select('*, courts(court_name)');
    if (error) {
      console.error('Error fetching data:', error);
    } else {
      rulings.value = data; // Update reactive property
    }
  } catch (err) {
    console.error('Unexpected error:', err);
  }
};

// Automatically fetch data when the component mounts
onMounted(fetchRulings);

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
    <ULandingCard class="col-span-6 row-span-4" icon="i-heroicons-swatch" title="IT-Sicherheitsrecht" description="Choose a primary and a gray color from your Tailwind CSS color palette." color="blue"/>
    <ULandingCard class="col-span-6 row-span-2" icon="i-heroicons-wrench-screwdriver" title="Internetrecht" description="Change the style of any component in your App Config or with ui prop." color="blue"/>
    <ULandingCard class="col-span-6 row-span-2" icon="i-heroicons-face-smile" title="Datenschutzrecht" description="Choose any of the 100k+ icons from the most popular icon libraries." color="blue" />
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
        Alle Urteile
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

