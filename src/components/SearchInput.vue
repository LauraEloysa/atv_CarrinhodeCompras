<script setup>
import { defineProps, defineEmits } from 'vue'

const props = defineProps({
  modelValue: String
})

const emit = defineEmits(['update:modelValue'])

function onInput(event) {
  emit('update:modelValue', event.target.value)
}
</script>

<template>
  <input
    type="text"
    :value="modelValue"
    @input="onInput"
    placeholder="Pesquisar"
  />
</template>
