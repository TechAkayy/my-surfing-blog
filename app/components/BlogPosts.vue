<script setup lang="ts">
  const { name } = defineProps({
    name: {
      type: String,
      default: 'BlogPosts',
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
  const { getPgWordpressPosts } = usePgWordpressData()
  const pgData: any = {
    pgWordpressData: {},
  }

  const pgPostsArgs = { posts: { filters: { _embed: 'true' } } }

  pgData.pgWordpressData.posts = {
    ...pgPostsArgs.posts,
    data: await getPgWordpressPosts(pgPostsArgs.posts),
  }

  const pgPosts = pgData.pgWordpressData.posts.data
  /* Auto-generated logic by Vue Designer Headless Wordpress 6.7 ends */
</script>
<template>
  <section class="py-16 px-4 md:px-8 bg-white dark:bg-neutral-950">
    <div class="max-w-6xl mx-auto">
      <h2
        class="text-3xl md:text-4xl font-serif text-gray-800 dark:text-neutral-100 text-center mb-12"
      >
        Latest Surf Stories
      </h2>
      <div
        class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8"
        data-pg-posts
      >
        <article
          v-for="(pgPost, index) in pgPosts"
          :key="index"
          class="bg-gray-50 dark:bg-neutral-900 rounded-lg overflow-hidden shadow-md"
        >
          <img
            alt="Surfing tips"
            class="w-full h-48 object-cover"
            style="
              background-image: url('https://images.unsplash.com/photo-1633297345330-261df10cf6a6?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDJ8fHN1cmZpbmclMjBoZXJvfGVufDB8fHx8MTc1ODMyNTA1MXww&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop');
              background-size: cover;
              background-position: center;
            "
            :src="
              pgPost?._embedded?.['wp:featuredmedia']?.[0]?.source_url ||
              'https://images.unsplash.com/photo-1633297345330-261df10cf6a6?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDJ8fHN1cmZpbmclMjBoZXJvfGVufDB8fHx8MTc1ODMyNTA1MXww&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop'
            "
          />
          <div class="p-6">
            <p class="text-blue-600 dark:text-blue-400 text-sm font-sans mb-2">
              March 15, 2024
            </p>
            <h3
              class="text-xl font-serif text-gray-800 dark:text-neutral-100 mb-3"
              v-html="pgPost?.title?.rendered"
            ></h3>
            <div
              class="text-gray-600 dark:text-gray-400 font-sans mb-4 line-clamp-3"
              v-html="pgPost?.excerpt?.rendered"
            ></div>
            <NuxtLink
              class="text-blue-600 dark:text-blue-400 font-sans hover:text-blue-700 dark:hover:text-blue-300 inline-flex items-center"
              :to="`/blog/${pgPost.slug}/${pgPost.id}`"
              >Read More <span class="ml-2">→</span>
            </NuxtLink>
          </div>
        </article>
      </div>
    </div>
  </section>
</template>
<style scoped></style>
