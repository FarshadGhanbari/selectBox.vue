<template>
  <select :value="getValue" @change="$emit('change', $event.target.value)" class="transition-all cursor-pointer bg-white dark:bg-neutral-700 border border-gray-200 focus:border-gray-400 dark:border-neutral-800 dark:focus:border-neutral-900 dark:text-neutral-300 focus:ring-0 focus:ring-transparent p-3 ring-0 text-sm text-gray-600 dark:text-gray-400 rounded-md">
    <slot/>
  </select>
</template>
<script>
export default {
  model: {
    prop: "modelValue",
    event: "change"
  },
  props: {
    value: {
      type: String
    },
    modelValue: {
      default: ""
    }
  },
  computed: {
    getValue() {
      return this.modelValue
    }
  }
}
</script>
