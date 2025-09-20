<script setup lang="ts">
  const { isMobileMenuOpen } = useMobileMenu()

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
  <div>
    <div
      v-if="isMobileMenuOpen"
      class="sm:min-w-[220px] rounded-2xl shadow-lg border border-black/5 dark:border-white/10 bg-white/80 dark:bg-neutral-900/70 backdrop-blur text-neutral-900 dark:text-neutral-50 px-4 py-4 sm:p-5 z-10"
    >
      <div class="space-y-2">
        <BaseButton
          v-for="(nav, index) in navs"
          :key="index"
          :to="nav.to"
          :icon="nav.icon"
          variant="ghost"
          color="gray"
          block
          :class="[
            '!rounded-full whitespace-nowrap !px-5 !py-2 transition-all',
            nav.to === currentPath
              ? 'bg-gradient-to-r from-primary-500 to-emerald-500 text-white shadow'
              : 'text-neutral-700 dark:text-neutral-200 hover:bg-primary-50/60 dark:hover:bg-primary-950/50',
          ]"
          size="md"
          @click="isMobileMenuOpen = !isMobileMenuOpen"
        >
          <span class="w-full sm:text-center">{{ nav.title }}</span>
        </BaseButton>
      </div>
    </div>
  </div>
</template>
<style scoped></style>
