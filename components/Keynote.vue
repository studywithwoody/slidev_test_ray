<template>
  <div
    class="keynote border-l-4 border-blue-600 bg-blue-50 p-4 dark:bg-blue-900/20 my-4 text-left shadow-sm"
  >
    <div
      v-if="title"
      class="keynote-title text-blue-800 dark:text-blue-200 font-bold mb-2 text-lg"
    >
      {{ title }}
    </div>
    <div class="keynote-content">
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
.keynote :deep(p) {
  margin-bottom: 0.5rem;
}
.keynote :deep(p:last-child) {
  margin-bottom: 0;
}
.keynote :deep(ul) {
  list-style-type: disc;
  margin-left: 1.5rem;
}
.keynote :deep(strong) {
  color: inherit;
}
</style>
