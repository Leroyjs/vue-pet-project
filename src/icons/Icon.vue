<template>
  <component :is="name"></component>
</template>

<script>
import * as icon from './variants'

export default {
  name: 'Icon',
  components: { ...icon },
  props: {
    name: {
      type: String,
      required: true,
      validator (value) {
        return Object.keys(icon).includes(value)
      }
    }
  }
}
</script>
