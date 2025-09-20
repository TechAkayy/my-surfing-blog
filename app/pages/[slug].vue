<script setup lang="ts">
  import { computed } from 'vue'

  const route = useRoute()

  const slug = route.params.slug

  definePageMeta({
    // layout: 'default',
    // name: 'slug',
    // alias: 'slug',
    title: 'Slug',
    description: 'Slug',
    // hidden: true,
    navOrder: '2',
    type: 'primary',
    icon: 'i-mdi-home',
    // ogImage: 'images/ogImage.png', // url or local images inside public folder, for eg, ~/public/images/ogImage.png
  })

  /* Auto-generated logic by Vue Designer Headless Wordpress 6.7 begins */
  const { getPgWordpressPost } = usePgWordpressData()
  const pgData: any = {
    pgWordpressData: {},
  }

  const pgPostArgs = {
    post: { filters: { id: route.query.id, _embed: 'true' } },
  }

  pgData.pgWordpressData.post = {
    ...pgPostArgs.post,
    data: await getPgWordpressPost(pgPostArgs.post),
  }

  const pgPost = pgData.pgWordpressData.post.data
  /* Auto-generated logic by Vue Designer Headless Wordpress 6.7 ends */

  const capitalize = (s) => (s && s[0].toUpperCase() + s.slice(1)) || ''
  useServerSeoMeta({
    description: () => capitalize(pgPost.value?.excerpt?.rendered || ''), // Example using post excerpt as description
  })
  useHead({
    title: () => capitalize(pgPost.value?.title?.rendered || ''),
  })
</script>
<template layout="default">
  <div>
    <article class="max-w-4xl mx-auto px-4 py-12 md:py-16" data-pg-post>
      <div class="space-y-8">
        <img
          alt="Surfing the Perfect Wave"
          class="w-full h-[500px] object-cover rounded-lg shadow-lg"
          :src="
            pgPost?._embedded?.['wp:featuredmedia']?.[0]?.source_url ||
            'https://images.unsplash.com/photo-1633297345330-261df10cf6a6?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDJ8fHN1cmZpbmclMjBoZXJvfGVufDB8fHx8MTc1ODMyNTA1MXww&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop'
          "
        />
        <div class="space-y-4">
          <div class="flex items-center gap-4 text-gray-600">
            <span>June 15, 2023</span><span>•</span>
            <div>
              <span>By</span> <span>{{ pgPost._embedded.author[0].name }}</span>
            </div>
          </div>
          <h1
            class="text-4xl md:text-5xl font-serif font-bold text-gray-900"
            v-html="pgPost.title.rendered"
          ></h1>
          <div class="flex flex-wrap gap-2">
            <span
              class="px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm"
              >Adventure</span
            ><span
              class="px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm"
              >Surfing</span
            ><span
              class="px-3 py-1 bg-blue-100 text-blue-800 rounded-full text-sm"
              >Ocean Life</span
            >
          </div>
          <div class="prose prose-lg text-gray-700">
            <div v-html="pgPost.content.rendered"></div>
          </div>
          <div class="flex items-center gap-4 pt-8 border-t border-gray-200">
            <img
              src="https://images.unsplash.com/photo-1704784191190-a228b02fbf68?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDE1fHxhdXRob3IlMjBzYXJhaHxlbnwwfHx8fDE3NTgzMjc0ODJ8MA&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop"
              alt="Sarah Waters"
              class="w-12 h-12 rounded-full object-cover"
            />
            <div>
              <h3
                class="font-bold text-gray-900"
                v-html="pgPost._embedded.author[0].name"
              ></h3>
              <p class="text-gray-600">
                {{
                  pgPost._embedded.author[0].description ||
                  'One who loves surfing'
                }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </article>
  </div>
</template>
<style scoped></style>
