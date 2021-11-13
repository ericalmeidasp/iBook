<template>
  <h1 class="read-title">
    {{ text }}
  </h1>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    text: {
      type: String,
      required: true
    }
  }
})
</script>

<style lang="scss" scoped>
.read-title {
  text-align: center;
  font-size: 2.5rem;
  font-weight: 500;
  @include screen('small', 'medium') {
    grid-template-columns: 1fr;
    font-size: 1.8rem;
  }
}
</style>
