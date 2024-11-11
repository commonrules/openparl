<script setup lang="ts">
definePageMeta({
  layout: 'repo'
})


</script>

<template>



<div class="bg-slate-50">

    <RepoNavigation />

</div>


<div class="border border-slate-100 rounded-2xl">
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
     <table>
  <tr>
    <td><UIcon name="i-heroicons-folder-solid" class="w-3 h-3" /></td>
    <td>Forschungsbericht.pdf</td>
    <td>27 Days ago</td>
  </tr>
  <tr>
    <td><UIcon name="i-heroicons-document" class="w-3 h-3" /></td>
    <td>Stellungnahme.pdf</td>
    <td>27 Days ago</td>
  </tr>
  <tr>
    <td><UIcon name="i-heroicons-document" class="w-3 h-3" /></td>
    <td>README.md</td>
    <td>27 Days ago</td>
  </tr>
     </table>
    </div>
  


    


  <div></div>






</template>

<style scoped>
.no-border {
  border-bottom: none;
}

</style>