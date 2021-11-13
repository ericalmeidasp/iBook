<template>
  <div class="book-slide-main">
    <div class="track">
      <ul class="slides">
        <transition name="fade" mode="out-in">
          <li
            v-for="i in [currentIndex]"
            :key="i"
            class="slide"
            v-html="$pages[i].text"
          ></li>
        </transition>
      </ul>
      <button class="prev" @click="prev">&#10094; Previous</button>
      <button class="next" @click="next">&#10095; Next</button>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { books } from '@/store'

export default Vue.extend({
  data() {
    return {
      currentIndex: 0 as number
    }
  },
  computed: {
    $book(): any {
      return books.$single
    },
    $pages(): any {
      return this.$book.pages
    },
    $maxIndex(): any {
      return this.$pages.length - 1
    }
  },
  methods: {
    next() {
      if (this.currentIndex >= 0 && this.currentIndex < this.$maxIndex) {
        this.currentIndex += 1
        console.log(this.$maxIndex)
      }
    },
    prev() {
      if (this.currentIndex > 0 && this.currentIndex <= this.$maxIndex) {
        this.currentIndex -= 1
      }
    }
  }
})
</script>

<style lang="scss" scoped>
.fade-enter-active,
.fade-leave-active {
  transition: all 0.2s ease;
  overflow: hidden;
  width: 100%;
  opacity: 1;
}

.fade-enter,
.fade-leave-to {
  width: 100%;
  opacity: 0;
}
.prev,
.next {
  cursor: pointer;
  width: auto;
  padding: 16px;
  font-weight: bold;
  font-size: 18px;
  transition: 0.7s ease;
  border-radius: 0 4px 4px 0;
  text-decoration: none;
  user-select: none;
}

.slides {
  border: solid 1px;
  padding: 1rem;
}
</style>
