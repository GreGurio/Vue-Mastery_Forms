<template>
  <label>{{ label }}</label>
  <input
    class="field"
    :placeholder="label"
    :value="modelValue"
    @input="$emit('update:modelValue', $event.target.value)"
    v-bind="$attrs"
  />
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: '',
    },
    modelValue: {
      type: [String, Number],
      default: '',
    },
  },
}
</script>

<style scoped>
label {
  display: block;
  font-size: 18px;
  color: #151515;
  padding: 10px;
  text-align: left;
  width: 500px;
  margin: 0 auto;
}
.field {
  padding: 20px;
  font-size: 20px;
  width: 500px;
}
</style>
