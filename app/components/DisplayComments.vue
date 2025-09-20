<script setup lang="ts">
  const props = defineProps({
    id: {
      type: [String, Number],
      default: null,
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
  const { getPgWordpressComments } = usePgWordpressData()
  const pgData: any = {
    pgWordpressData: {},
  }

  const pgCommentsArgs = {
    comments: { filters: { _embed: 'true', post: props.id } },
  }

  pgData.pgWordpressData.comments = {
    ...pgCommentsArgs.comments,
    data: await getPgWordpressComments(pgCommentsArgs.comments),
  }

  const pgComments = pgData.pgWordpressData.comments.data
  /* Auto-generated logic by Vue Designer Headless Wordpress 6.7 ends */
</script>
<template>
  <div data-pg-comments>
    <div
      v-for="(pgComment, index) in pgComments"
      :key="index"
      class="flex gap-4 p-6 bg-gray-50 dark:bg-gray-800 rounded-lg"
    >
      <img
        src="https://images.unsplash.com/photo-1585556001514-a062c3e4f3f3?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDE4fHxzdXJmZXIlMjBwcm9maWxlfGVufDB8fHx8MTc1ODM3MTA5OHww&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop"
        alt="Profile"
        class="w-12 h-12 rounded-full object-cover"
      />
      <div class="flex-1">
        <div class="flex items-center gap-2 mb-2">
          <h3
            class="font-bold text-gray-900 dark:text-white"
            v-html="pgComment.author_name"
          ></h3>
          <span class="text-sm text-gray-600 dark:text-gray-400"
            >2 days ago</span
          >
        </div>
        <div
          class="text-gray-700 dark:text-gray-300"
          v-html="pgComment.content.rendered"
        ></div>
      </div>
    </div>
  </div>
</template>
<style scoped></style>
