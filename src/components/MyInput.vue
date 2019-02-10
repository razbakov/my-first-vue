<template>
  <div>
    <p>{{ label }}</p>
    <input type="text" :value="value" @input="$emit('input', $event.target.value)">
    <p>{{ value | count }} / {{ max }}</p>
  </div>
</template>

<script>
export default {
  name: 'MyInput',
  props: {
    label: {
      type: String,
      default: ''
    },
    value: {
      type: String,
      default: ''
    },
    max: {
      type: Number,
      default: 70
    },
  },
  filters: {
    count(value) {
      return value.length
    }
  }
}
</script>