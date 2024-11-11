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
  <div class="w-full lg:w-3/5 px-4">
    <!-- Main center content here -->

     <GesetzesText />
  </div>

  <!-- Right Sidebar -->
  <div class="hidden lg:block lg:w-2/5">
    <!-- Right sidebar content here -->
    <div class="bg-slate-50 rounded-lg mt-10">
    <div class="flex justify-start p-8">

      
  <UAvatar
      size="xs"
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b5/Deutscher_Bundestag_logo.svg/800px-Deutscher_Bundestag_logo.svg.png"
      alt="Avatar"
    />
  <div class="mx-4">Deutscher Bundestag</div>
</div>

</div>
  </div>
</div>



</template>

<style scoped>
.no-border {
  border-bottom: none;
}

</style>