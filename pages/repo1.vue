<script setup lang="ts">
definePageMeta({
  layout: 'repo'
})


</script>

<template>



<div class="bg-slate-50">

    <RepoNavigation />

</div>


<div class="flex justify-center max-w-screen-xl mx-auto">
  <!-- Left Sidebar -->
  <div class="hidden lg:block lg:w-1/5">
    <!-- Left sidebar content here -->
  </div>

  <!-- Center Content -->
  <div class="w-full xl:w-3/5 px-4">
    <!-- Main center content here -->
    <div class="border border-slate-100 rounded-xl mt-5">
     <GesetzesText />
    </div>
  </div>

  <!-- Right Sidebar -->
  <div class="hidden lg:block lg:w-1/5">
    <!-- Right sidebar content here -->
    


  <div></div>


</div>
  </div>




</template>

<style scoped>
.no-border {
  border-bottom: none;
}

</style>