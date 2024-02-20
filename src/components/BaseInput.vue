<script setup>
import { computed } from 'vue'

const props = defineProps({
  modeValue: {
    type: String,
    default: ''
  }
})

const emit = defineEmits(['update:modeValue'])

const localValue = computed({
  get() {
    return props.modelValue
  },
  set(newValue) {
    emit('update:modeValue', newValue)
  }
})
</script>

<template>
  <input v-model="localValue" />
</template>

<style scoped></style>
