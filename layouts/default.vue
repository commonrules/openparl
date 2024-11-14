<script setup lang="ts">
const links = [
  [{
    label: 'Home',
    icon: 'i-heroicons-home',
    to: '/'
  }, {
    label: 'Legislation',
    icon: 'i-heroicons-chart-bar',
    to: '/components/vertical-navigation'
  }, {
    label: 'Bills',
    icon: 'i-heroicons-command-line',
    to: '/components/command-palette'
  }, {
    label: 'Court Rulings',
    icon: 'i-heroicons-command-line',
    to: '/components/command-palette'
  }, {
    label: 'Executive Acts',
    icon: 'i-heroicons-command-line',
    to: '/components/command-palette'
  }]
]
</script>



<template>
    <div class="flex justify-between mx-10 mt-8">
        <div class="w-1/6 mt-1">

            
            <VerticalNav />

        </div> 


        <div class="w-5/6">
            <div class="flex justify-between">
                <div class="w-5/6 mr-10">
            <Search class="" /> 
            <slot />
        </div>

            <div class="w-1/6">
                <div class="flex justify-end">
        <JurisDictionDrop class="mr-5 mt-1 max-w-48" />

            <Avatar class="mt-1"/>
        </div>
        </div>
            </div>
        </div>
    </div>
</template>