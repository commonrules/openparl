<script setup lang="ts">
definePageMeta({
  layout: 'repo'
})


</script>

<template>



<div class="bg-slate-50">
  <div class="flex justify-center">
    <div class="w-1/2l">
    <RepoNavigation />
  </div>
</div>
</div>


<div class="flex justify-center max-w-screen-xl mx-auto">
  <!-- Left Sidebar -->
  <div class="hidden lg:block lg:w-1/5">
    <!-- Left sidebar content here -->
  </div>

  <!-- Center Content -->
  <div class="w-full lg:w-3/5 px-4">
    <!-- Main center content here -->

     <GesetzesText />
  </div>

  <!-- Right Sidebar -->
  <div class="hidden lg:block lg:w-1/5">
    <!-- Right sidebar content here -->
  </div>
</div>



</template>

<style scoped>
.no-border {
  border-bottom: none;
}

</style>