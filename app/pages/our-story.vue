<script setup lang="ts">
  definePageMeta({
    // layout: 'default',
    // name: 'our-story',
    // alias: 'our-story',
    title: 'Our Story',
    description: 'Our Story',
    // hidden: true,
    navOrder: '3',
    type: 'primary',
    icon: 'i-mdi-home',
    // ogImage: 'images/ogImage.png', // url or local images inside public folder, for eg, ~/public/images/ogImage.png
  })
</script>
<template>
  <div class="min-h-screen bg-white dark:bg-neutral-950">
    <div class="relative bg-slate-900">
      <div class="absolute inset-0">
        <img
          src="https://images.unsplash.com/photo-1496855631292-9259fb1a0341?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDZ8fHN1cmYlMjBhZXJpYWx8ZW58MHx8fHwxNzU4Mzc5OTIzfDA&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop"
          class="w-full h-full object-cover opacity-40"
          alt="Aerial view of waves"
        />
      </div>
      <div class="relative container mx-auto px-4 py-24">
        <h1 class="text-4xl md:text-6xl font-serif text-white text-center mb-6">
          Our Story
        </h1>
        <p class="text-lg md:text-xl text-white text-center max-w-3xl mx-auto">
          Riding waves and chasing dreams since 2010
        </p>
      </div>
    </div>
    <div class="container mx-auto px-4 py-16 md:py-24">
      <div class="grid md:grid-cols-2 gap-12 items-center">
        <div class="space-y-6">
          <h2
            class="text-3xl md:text-4xl font-serif text-slate-900 dark:text-neutral-100"
          >
            How It All Began
          </h2>
          <p class="text-slate-700 dark:text-slate-300">
            What started as a simple passion for surfing turned into a lifelong
            journey of discovery, adventure, and connection with the ocean. Our
            story begins on the sun-kissed shores of the Gold Coast, where every
            wave told a new tale.
          </p>
          <p class="text-slate-700 dark:text-slate-300">
            Through years of dawn patrols and sunset sessions, we've built more
            than just a blog - we've created a community of wave riders and
            ocean lovers who share our dedication to the surf lifestyle.
          </p>
        </div>
        <div class="relative h-[400px]">
          <img
            src="https://images.unsplash.com/photo-1634148161307-0bb497973f12?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDE5fHxzdXJmZXIlMjBzdW5zZXR8ZW58MHx8fHwxNzU4Mzc5OTIzfDA&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop"
            class="w-full h-full object-cover rounded-lg shadow-xl"
            alt="Surfer at sunset"
          />
        </div>
      </div>
    </div>
    <div class="bg-slate-50 dark:bg-neutral-900 py-16 md:py-24">
      <div class="container mx-auto px-4">
        <div class="grid md:grid-cols-3 gap-8">
          <div class="bg-white dark:bg-neutral-900 p-8 rounded-lg shadow-sm">
            <h3
              class="text-xl font-serif text-slate-900 dark:text-neutral-100 mb-4"
            >
              Our Mission
            </h3>
            <p class="text-slate-700 dark:text-slate-300">
              To share the stoke of surfing and inspire others to embrace the
              ocean's endless possibilities.
            </p>
          </div>
          <div class="bg-white dark:bg-neutral-900 p-8 rounded-lg shadow-sm">
            <h3
              class="text-xl font-serif text-slate-900 dark:text-neutral-100 mb-4"
            >
              Our Vision
            </h3>
            <p class="text-slate-700 dark:text-slate-300">
              Creating a global community of surfers connected through stories,
              experiences, and love for the waves.
            </p>
          </div>
          <div class="bg-white dark:bg-neutral-900 p-8 rounded-lg shadow-sm">
            <h3
              class="text-xl font-serif text-slate-900 dark:text-neutral-100 mb-4"
            >
              Our Values
            </h3>
            <p class="text-slate-700 dark:text-slate-300">
              Respect for the ocean, sustainability, authenticity, and the
              spirit of adventure.
            </p>
          </div>
        </div>
      </div>
    </div>
    <div class="container mx-auto px-4 py-16 md:py-24">
      <div class="max-w-3xl mx-auto text-center">
        <h2
          class="text-3xl md:text-4xl font-serif text-slate-900 dark:text-neutral-100 mb-8"
        >
          Join Our Journey
        </h2>
        <p class="text-slate-700 dark:text-slate-300 mb-8">
          Whether you're a seasoned surfer or just starting out, there's a place
          for you in our story. Follow along as we continue to explore the
          world's best waves and share the pure joy of surfing.
        </p>
        <NuxtLink
          to="/contact"
          class="inline-block bg-blue-600 text-white px-8 py-3 rounded-lg hover:bg-blue-700 transition-colors"
          >Connect With Us</NuxtLink
        >
      </div>
    </div>
  </div>
</template>
<style scoped></style>
