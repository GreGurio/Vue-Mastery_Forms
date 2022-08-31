<template>
  <input
    type="checkbox"
    :checked="modelValue"
    @change="$emit('update:modelValue', $event.target.checked)"
    class="field"
  />
  <label v-if="label">{{ label }}</label>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: '',
    },
    modelValue: {
      type: Boolean,
      default: false,
    },
  },
}
</script>

<style scoped>
label {
  margin-left: 30px;
}
.field {
  font-size: 20px;
  margin: 10px 0;
}
</style>
