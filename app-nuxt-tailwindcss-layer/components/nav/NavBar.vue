<script setup lang="ts">
  const { allNavs, navsPrimary, navsSecondary, currentPath } = useNavMenu()
</script>
<template>
  <div class="w-full">
    <nav>
      <div class="container mx-auto px-4 sm:px-6">
        <div class="flex h-24 items-center justify-between">
          <!-- Left: Logo -->
          <div class="flex items-center gap-4 min-w-0">
            <TheLogo />
          </div>
          <!-- Center: Primary nav in a glass pill -->
          <div class="hidden sm:flex items-center justify-center flex-1 px-4">
            <div
              class="hidden sm:flex items-center gap-2 px-3 py-2 rounded-full bg-white/70 dark:bg-neutral-900/60 backdrop-blur supports-[backdrop-filter]:bg-white/60 supports-[backdrop-filter]:dark:bg-neutral-900/50"
            >
              <NavPrimary
                :navs="navsPrimary"
                :current-path="currentPath"
                class="sm:flex"
              />
            </div>
          </div>
          <!-- Right: Theme + Menus -->
          <div class="flex items-center gap-2 relative">
            <DarkModeSwitch class="hidden md:block" />
            <!-- Secondary (desktop) -->
            <NavHamburger
              v-if="navsSecondary?.length"
              class="hidden sm:block"
            />
            <!-- All (mobile) -->
            <NavHamburger v-if="allNavs.length" class="sm:hidden" />
            <NavSecondary
              v-if="navsSecondary?.length"
              class="hidden sm:flex sm:justify-end absolute right-0 mt-4"
              :navs="navsSecondary"
              :current-path="currentPath"
            />
          </div>
        </div>
      </div>
      <!-- Mobile full menu below bar -->
      <NavSecondary
        class="sm:hidden"
        :navs="allNavs"
        :current-path="currentPath"
      />
    </nav>
  </div>
</template>
<style scoped></style>
