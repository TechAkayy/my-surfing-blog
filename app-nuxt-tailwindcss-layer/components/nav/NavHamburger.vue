<script setup lang="ts">
  const { isMobileMenuOpen, openMobileMenu } = useMobileMenu()
</script>
<template>
  <BaseButton
    size="xl"
    :icon="
      isMobileMenuOpen ? 'i-material-symbols-close' : 'i-material-symbols-menu'
    "
    class="!py-2 !rounded-full leading-none bg-white/70 dark:bg-neutral-900/60 backdrop-blur border border-black/5 dark:border-white/10 shadow"
    @click="openMobileMenu"
  >
    <span class="sr-only">Open main menu</span>
  </BaseButton>
</template>
<style scoped></style>
