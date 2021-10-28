<template>
  <div>
    <label>{{ label }}</label>
    <input
      v-bind="{
        ...$attrs,
        onInput: (event) => $emit('update:modelValue', event.target.value)
        }"
      :value="modelValue"
    />
  </div>
</template>

<script lang="ts">
export default {
  inheritAttrs: false,
  props: {
    modelValue: {
      type: [String, Number],
      default: '',
    },
    label: {
      type: String,
      default: null,
    },
  },
}
</script>
