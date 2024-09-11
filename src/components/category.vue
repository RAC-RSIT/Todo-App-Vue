<script setup>
const props = defineProps({
  modelValue: {
    type: String,
    default: "",
  },
  value: {
    type: String,
    default: "",
  },
});
</script>

<template>
  <label>
    <input
      type="radio"
      name="category"
      :value="value"
      @input="$emit('update:modelValue', value)"
    />
    <span :class="['bubble', value]"></span>
    <div>{{ value }}</div>
  </label>
</template>
