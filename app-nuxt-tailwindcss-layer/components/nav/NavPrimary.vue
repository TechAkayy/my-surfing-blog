<script setup lang="ts">
  defineProps({
    navs: {
      type: Array,
      default() {
        return []
      },
    },
    currentPath: {
      type: String,
      default: '/',
    },
  })
</script>
<template>
  <div class="h-full items-center">
    <div class="flex h-full gap-1.5">
      <BaseButton
        v-for="(nav, index) in navs"
        :key="index"
        :to="nav.to"
        :label="nav.title"
        :icon="nav.icon"
        size="lg"
        variant="ghost"
        color="gray"
        :class="[
          '!rounded-full !px-5 !py-2 transition-all',
          nav.to === currentPath
            ? 'bg-gradient-to-r from-primary-500 to-emerald-500 text-white shadow-md ring-1 ring-white/20 dark:ring-white/10'
            : 'text-neutral-700 dark:text-neutral-200 hover:bg-primary-50/60 dark:hover:bg-primary-950/50',
        ]"
      />
    </div>
  </div>
</template>
<style scoped></style>
