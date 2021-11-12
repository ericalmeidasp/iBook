<template>
  <HomeTemplate />
</template>

<script lang="ts">
import Vue from 'vue'
import { books } from '@/store'
import { Book } from '@/models'

export default Vue.extend({
  layout: 'ibook',
  async asyncData() {
    await books.index()
  },
  computed: {
    $books(): Book[] {
      return books.$all
    }
  },


  methods: {
    
    show() {
      console.log(this.$books)
    }
  }
})
</script>

<style scoped></style>
