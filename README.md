# selectBox.vue
Simple custom selectBox component with tailwind css for Vue.js/Nuxt.js, compatible with v-model.

<select :value="getValue" @change="$emit('change', $event.target.value)" ...
        
computed: {
  getValue() {
    return this.modelValue
  }
}
