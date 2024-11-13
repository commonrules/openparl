<script setup lang="ts">
const items = [
  [{
    label: 'mibressler',
    slot: 'account',
    disabled: true
  }], [{
    slot: 'last',
    disabled: false,
    label1: 'GG',
    owner1: 'Bundestag',
    src1: 'https://avatars.githubusercontent.com/u/739984?v=4',
    label2: 'DDG',
    owner2: 'Bundestag',
    src2: 'https://avatars.githubusercontent.com/u/739984?v=4',
    label3: 'BayDiGWiki',
    owner3: 'mibressler',
    src3: 'https://avatars.githubusercontent.com/u/739984?v=4',

  }], [{
    label: 'My Profile',
    icon: 'i-heroicons-user'
  }],
   [{
    label: 'Settings',
    icon: 'i-heroicons-cog-8-tooth'
  }], [{
    label: 'Documentation',
    icon: 'i-heroicons-book-open'
  }, {
    label: 'Changelog',
    icon: 'i-heroicons-megaphone'
  }, {
    label: 'Status',
    icon: 'i-heroicons-signal'
  }], [{
    label: 'Sign out',
    icon: 'i-heroicons-arrow-left-on-rectangle'
  }]
]
</script>

<template>
  <UDropdown :items="items" :ui="{ item: { disabled: 'cursor-text select-text' } }" :popper="{ placement: 'bottom-start' }">
    <UAvatar src="https://avatars.githubusercontent.com/u/739984?v=4"  chip-color="blue"
    chip-text=""
    chip-position="top-right"/>

    <template #account="{ item }">
      <div class="text-left">
        <p>
          Signed in as
        </p>
        <p class="truncate font-medium text-gray-900 dark:text-white">
          {{ item.label }}
        </p>
      </div>
    </template>

    <template #last="{ item }">
      <div class="text-left text-gray-400">
        <p>
          Last accessed
        </p>
        <span>{{ item.owner1 }}</span> / <span class="font-semibold">{{ item.label1 }}</span><UAvatar :src="item.src1" class="" />
        <span>{{ item.owner2 }}</span> / <span class="font-semibold">{{ item.label2 }}</span><UAvatar :src="item.src2" />
        <span>{{ item.owner3 }}</span> / <span class="font-semibold">{{ item.label3 }}</span><UAvatar :src="item.src3" />

        
      </div>
    </template>

    <template #item="{ item }">
      <span class="truncate">{{ item.label }}</span>

      <UIcon :name="item.icon" class="flex-shrink-0 h-4 w-4 text-gray-400 dark:text-gray-500 ms-auto" />
    </template>
  </UDropdown>
</template>

