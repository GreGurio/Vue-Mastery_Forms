<template>
  <component
    :is="vertical ? 'div' : 'span'"
    v-for="option in options"
    :key="option.value"
    :class="{
        horizontal: !vertical
    }"
  >
    <BaseRadio 
        :label="option.label"
        :value="option.value"
        :name="name"
        :modelValue="modelVaue"
        @update:modelValue="$emit('update:modelValue', $event)"
    />
  </component>
</template>

<script>
  export default {
    props: {
      options: {
        type: Array,
        required: true,
      },
      name: {
        type: String,
        required: true,
      },
      modelValue: {
        type: [String, Number],
        required: true,
      },
      vertical: {
        type: Boolean,
        default: false,
      },
    },
}
</script>

<style scoped>
.horizontal {
  margin-right: 20px;
}
</style>