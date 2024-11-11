<script setup lang="ts">
definePageMeta({
  layout: 'repo'
})


</script>

<template>




<div class="flex justify-center">

</div>

<RepoNavigation />
<div class="flex justify-center">
  <!-- Left Sidebar -->
  <div class="w-1/4 lg:w-1/5 hidden md:block"> <!-- Adjust width as needed -->
    <!-- Left sidebar content here -->
     
  </div>

  <!-- Center Content -->
  <div class="w-full md:w-2/4 lg:w-3/5 px-4">
    <!-- Main center content here -->

    <GesetzesText />
  </div>

  <!-- Right Sidebar -->
  <div class="w-1/4 lg:w-1/5 hidden md:block">
    <!-- Right sidebar content here -->
  </div>
</div>

</template>

<style scoped>
.no-border {
  border-bottom: none;
}

</style>