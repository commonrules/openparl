<script setup lang="ts">
definePageMeta({
  layout: 'repo'
})


</script>

<template>



<div class="bg-slate-50">

    <RepoNavigation />

</div>

<div class="flex justify-between">

<div class="w-1/3">

<div class="border border-slate-100">
      <div class="flex justify-start bg-slate-100 text-sm pl-5 py-3"> 
        <UAvatar
      size="3xs"
      src="https://upload.wikimedia.org/wikipedia/commons/thumb/b/b5/Deutscher_Bundestag_logo.svg/800px-Deutscher_Bundestag_logo.svg.png"
      alt="Avatar"
      class="pt-1"
    />
    <span class="font-semibold pr-4 ml-4">Bundestag</span>
    Rentenreform zur Beschleunigung der viele..<span class="pl-5 text-slate-400">27 Days ago</span>
  
<span class="pl-5"><UIcon name="i-heroicons-arrow-path" class="w-3 h-3" /></span><span class="pl-2 font-semibold">53 Gesetzesänderungen</span></div>

    </div>

    <div class="border border-slate-100">
      <div class="flex justify-start text-sm pl-5 py-3"> 
        <UIcon name="i-heroicons-chevron-right" class="w-4 h-4" /><UIcon name="i-heroicons-folder" class="w-4 h-4" />
    <span class="font-semibold pr-4 ml-4">FileSampleVeryLargeTBH_Final.md</span><span class="ml-10">
    Rentenreform zur Beschleunigung der vielen guten Di..</span><span class="pl-5 text-slate-400">27 Days ago</span>
</div>
    </div>

    <div class="border border-slate-100">
      <div class="flex justify-start text-sm pl-5 py-3"> 
        <UIcon name="i-heroicons-document" class="w-4 h-4" />
    <span class="font-semibold pr-4 ml-4">FileSampleVeryLargeTBH_Final.md</span><span class="ml-10">
    Rentenreform zur Beschleunigung der vielen guten Di..</span><span class="pl-5 text-slate-400">27 Days ago</span>
</div>
    </div>

    <div class="border border-slate-100">
      <div class="flex justify-start text-sm pl-5 py-3"> 
        <UIcon name="i-heroicons-document" class="w-4 h-4" />
    <span class="font-semibold pr-4 ml-4">FileSampleVeryLargeTBH_Final.md</span><span class="ml-10">
    Rentenreform zur Beschleunigung der vielen guten Di..</span><span class="pl-5 text-slate-400">27 Days ago</span>
</div>
    </div>




    
    
  </div>


  <div class="w-2/3">
    <div>README</div>
  </div>

  </div>






</template>

<style scoped>
.no-border {
  border-bottom: none;
}

</style>