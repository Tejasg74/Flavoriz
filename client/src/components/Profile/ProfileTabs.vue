<script setup lang="ts">
import RecipeTab from './RecipeTab.vue'
import BookmarkTab from './BookmarkTab.vue'
import { ref } from 'vue'
const selectedTab = ref('RecipeTab')
</script>
<template>
  <div class="flex w-11/12 flex-col gap-5 overflow-hidden xl:w-10/12">
    <div class="flex flex-1">
      <div
        @click="selectedTab = 'RecipeTab'"
        class="border-b-hover relative flex-1 cursor-pointer border-b py-2 text-center text-lg font-medium"
      >
        My Recipes
      </div>

      <div
        @click="selectedTab = 'BookmarkTab'"
        class="border-b-hover relative flex-1 cursor-pointer border-b py-2 text-center text-lg font-medium"
      >
        Favourites
      </div>
    </div>
    <transition name="fade" mode="out-in">
      <RecipeTab v-if="selectedTab === 'RecipeTab'" key="RecipeTab" />
      <BookmarkTab v-else key="BookmarkTab" />
    </transition>
  </div>
</template>

<style>
.border-b-hover::after {
  content: '';
  display: block;
  position: absolute;
  bottom: 0;
  width: 0;
  height: 2px;
  background: currentColor;
  transition: width 0.2s ease-in-out;
}
.border-b-hover:hover::after {
  width: 100%;
}
.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.25s ease;
}
.fade-enter-from, .fade-leave-to /* .fade-leave-active in <2.1.8 */ {
  opacity: 0;
}
</style>
