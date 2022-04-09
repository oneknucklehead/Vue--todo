<template>
  <button v-on:click="clickFunc()" :style="{ background: color }" class="btn">
    {{ text }}
  </button>
</template>

<script>
export default {
  name: 'Button',
  props: {
    text: String,
    color: String,
  },
  methods: {
    clickFunc() {
      this.$emit('btn-click')
    },
  },
}
</script>
