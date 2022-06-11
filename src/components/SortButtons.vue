<script setup>
import IconSortNumber from '@/assets/icons/sort-1-9.svg?component'
import IconSortAlpha from '@/assets/icons/sort-a-z.svg?component'

const emit = defineEmits(['sort-by'])
</script>

<template>
  <span class="mr-3">Order by:</span>
  <div class="inline-flex mb-8">
    <button
      class="bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded-l"
      @click="emit('sort-by', 'id')"
    >
      <IconSortNumber />
    </button>
    <button
      class="border-l border-gray-200 bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded-r"
      @click="emit('sort-by', 'name')"
    >
      <IconSortAlpha />
    </button>
  </div>
</template>
