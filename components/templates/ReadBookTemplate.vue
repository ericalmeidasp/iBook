<template>
  <div class="read-book-template">
    <ReadTitle :text="$book.title" />
    <BookRead />
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { books } from '@/store'

export default Vue.extend({
  computed: {
    $book() {
      return books.$single
    }
  }
})
</script>

<style scoped></style>
