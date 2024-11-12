<script setup lang="ts">
definePageMeta({
  layout: 'repo'
})


</script>

<template>



<div class="bg-slate-50 dark:bg-gray-800">

    <RepoNavigationMult />

</div>

<div class="flex justify-center">

<div class="w-full">

<div class="border border-slate-100">
      <div class="flex justify-start bg-slate-100 dark:bg-gray-800 text-sm pl-5 py-3"> 

    <span class="font-semibold pr-4 ml-0"><span class="mr-2"><UIcon name="i-heroicons-arrow-path" class="w-4 h-4" /></span>20 Open</span>
    15 Closed<span class="pl-5 text-slate-400">27 Days ago</span>
  
<span class="pl-5"><UIcon name="i-heroicons-arrow-path" class="w-4 h-4" /></span><span class="pl-2 font-semibold">53 Gesetzesänderungen</span></div>

    </div>

    <div class="overflow-x-auto text-sm">
  <table class="min-w-full border-collapse border border-slate-100">
    <tbody>
      <tr class="border-t border-slate-100">
        <td class="pl-5 py-3">
          <UIcon name="i-heroicons-chevron-right" class="w-4 h-4" />
        </td>
        <td class="py-3">
          <UIcon name="i-heroicons-folder" class="w-4 h-4" />
        </td>
        <td class="font-semibold pr-4 ml-4 py-3">Drafts</td>
        <td class="ml-10 py-3">Rentenreform zur Beschleunigu..</td>
        <td class="pl-5 text-slate-400 py-3">27 Days ago</td>
      </tr>
      <tr class="border-t border-slate-100">
        <td class="pl-5 py-3">
          
        </td>
        <td class="py-3">
          <UIcon name="i-heroicons-document" class="w-4 h-4" />
        </td>
        <td class="font-semibold pr-4 ml-4 py-3">CurrentDraft.md</td>
        <td class="ml-10 py-3">Rentenreform zur Beschleunigu..</td>
        <td class="pl-5 text-slate-400 py-3">27 Days ago</td>
      </tr>
      <tr class="border-t border-slate-100 bg-gray-600 text-white">
        <td class="pl-5 py-3">
          
        </td>
        <td class="py-3">
          <UIcon name="i-heroicons-document" class="w-4 h-4" />
        </td>
        <td class="font-semibold pr-4 ml-4 py-3">README.md</td>
        <td class="ml-10 py-3">Rentenreform zur Beschleunigu..</td>
        <td class="pl-5 text-slate-400 py-3">27 Days ago</td>
      </tr>
    </tbody>
  </table>
</div>





</div>
    
</div>





</template>

<style scoped>
.no-border {
  border-bottom: none;
}

</style>