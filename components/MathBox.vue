<template>
  <div
    class="math-box border-l-4 border-red-600 bg-red-50 p-4 dark:bg-red-900/20 my-4 text-left shadow-sm"
  >
    <div
      v-if="title"
      class="math-box-title text-red-800 dark:text-red-200 font-bold mb-2 text-lg"
    >
      {{ title }}
    </div>
    <div class="math-box-content">
      <slot />
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: String,
});
</script>

<style scoped>
.math-box :deep(p) {
  margin-bottom: 0.5rem;
}
.math-box :deep(p:last-child) {
  margin-bottom: 0;
}
.math-box :deep(ul) {
  list-style-type: disc;
  margin-left: 1.5rem;
}
</style>
