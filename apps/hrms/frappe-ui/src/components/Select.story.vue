<script setup lang="ts">
import { ref } from 'vue'
import Select from './Select.vue'

const value = ref('')
const options = [
  { label: 'John Doe', value: 'john-doe' },
  { label: 'Jane Doe', value: 'jane-doe' },
  { label: 'John Smith', value: 'john-smith' },
  { label: 'Jane Smith', value: 'jane-smith', disabled: true },
  { label: 'John Wayne', value: 'john-wayne' },
  { label: 'Jane Wayne', value: 'jane-wayne' },
]
</script>
<template>
  <Story :layout="{ width: 500, type: 'grid' }">
    <div class="p-2">
      <Select :options="options" v-model="value" />
    </div>
  </Story>
</template>
