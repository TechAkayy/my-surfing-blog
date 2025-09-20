<script setup lang="ts">
  const { name } = defineProps({
    name: {
      type: String,
      default: 'HeroSection',
    },
  })

  // const emit = defineEmits(['addToCart'])

  // // Use the addToCart function like this:
  // // Eg-1: addToCart('pizza', 10)
  // // Eg-2: (event) => addToCart('pizza', 10, event)
  // const addToCart = (item, quantity /*, event*/) => {
  // 	emit('addToCart', { item, quantity })
  // }

  /* Auto-generated logic by Vue Designer Headless Wordpress 6.7 begins */
  const { getPgWordpressSiteinfo } = usePgWordpressData()
  const pgData: any = {
    pgWordpressData: {},
  }

  const pgSiteinfoArgs = { siteinfo: {} }

  pgData.pgWordpressData.siteinfo = {
    ...pgSiteinfoArgs.siteinfo,
    data: await getPgWordpressSiteinfo(pgSiteinfoArgs.siteinfo),
  }

  const pgSiteinfo = pgData.pgWordpressData.siteinfo.data
  /* Auto-generated logic by Vue Designer Headless Wordpress 6.7 ends */
</script>
<template>
    <header class="relative h-screen text-white" style="
      background-image: url('https://images.unsplash.com/photo-1633297345330-261df10cf6a6?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDJ8fHN1cmZpbmclMjBoZXJvfGVufDB8fHx8MTc1ODMyNTA1MXww&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop');
      background-size: cover;
      background-position: center;
    ">
        <div class="absolute bg-inherit/40 inset-0"></div>
        <div class="relative z-10 container mx-auto h-full px-4 md:px-8">
            <div class="grid grid-cols-1 md:grid-cols-2 h-full">
                <!-- Left half intentionally empty to keep focus on right -->
                <div class="hidden md:block"></div>
                <!-- Right half: squared panel -->
                <div class="flex items-center justify-center md:justify-end py-16">
                    <div class="w-full max-w-md p-6 md:p-8 bg-white/85 dark:bg-neutral-900/70 backdrop-blur-sm shadow-sm text-neutral-900 dark:text-neutral-50">
                        <h2 class="text-lg md:text-xl mb-2 font-mono tracking-wider text-left">
              Ride the Waves </h2>
                        <h1 class="text-4xl md:text-6xl font-serif mb-6 text-left">
              Surfers Paradise </h1>
                        <p class="text-lg md:text-xl mb-8 font-sans text-left" data-pg-siteinfo>
              {{ pgSiteinfo.description }} </p>
                        <NuxtLink to="/stories" class="inline-block bg-blue-600 hover:bg-blue-700 text-white font-sans py-3 px-8 transition duration-300 rounded-none">
                            Read Our Stories
</NuxtLink>
                    </div>
                </div>
            </div>
        </div>
    </header>
</template>
<style scoped></style>
