<script setup lang="ts">
  import { ref } from 'vue'
  const props = defineProps({
    id: {
      type: [String, Number],
      default: null,
    },
  })
  const author_name = ref('')
  const author_email = ref('')
  const content = ref('')

  const isLoading = ref(false)
  const error = ref(null)
  const commentPosted = ref(null)

  const postComment = async () => {
    isLoading.value = true
    error.value = null
    commentPosted.value = null

    if (!props.id) {
      error.value = 'Missing post id'
      isLoading.value = false
      return
    }

    const username = 'admin'
    const appPass = 'rrs9 8L46 6iuN KIXY LonJ 6egQ'
    const token = btoa(`${username}:${appPass}`)

    try {
      const wordpressUrl: string = import.meta.env.VITE_WORDPRESS_URL

      const response = await fetch(`${wordpressUrl}/wp-json/wp/v2/comments`, {
        method: 'POST',
        headers: {
          'Content-Type': 'application/json',
          Authorization: `Basic ${token}`,
        },
        body: JSON.stringify({
          post: Number(props.id),
          author_name: author_name.value,
          author_email: author_email.value,
          content: content.value,
        }),
      })

      if (!response.ok) {
        throw new Error('Failed to post comment')
      }

      commentPosted.value = await response.json()
    } catch (err) {
      error.value = err.message
    } finally {
      isLoading.value = false
      author_name.value = ''
      author_email.value = ''
      content.value = ''
    }
  }
</script>
<template>
  <div class="space-y-8">
    <DisplayComments :id="props.id" :key="commentPosted" />
    <div class="mt-8">
      <!-- eslint-disable vue/html-self-closing -->
      <form @submit.prevent="postComment">
        <div class="mb-4 space-y-4">
          <input
            v-model="author_name"
            type="text"
            placeholder="John Doe"
            required
            class="w-full p-4 border border-gray-200 dark:border-gray-700 rounded-lg bg-white dark:bg-gray-800 text-gray-900 dark:text-white"
          />
          <input
            v-model="author_email"
            type="email"
            required
            placeholder="Your Email"
            class="w-full p-4 border border-gray-200 dark:border-gray-700 rounded-lg bg-white dark:bg-gray-800 text-gray-900 dark:text-white"
          />
        </div>
        <textarea
          v-model="content"
          class="w-full p-4 border border-gray-200 dark:border-gray-700 rounded-lg bg-white dark:bg-gray-800 text-gray-900 dark:text-white"
          placeholder="Add your comment..."
          rows="4"
        ></textarea>
        <button
          class="mt-4 px-6 py-2 bg-blue-600 text-white rounded-lg hover:bg-blue-700"
          type="submit"
          :disabled="isLoading"
        >
          Post Comment
        </button>
      </form>
      <p v-if="isLoading">Submitting your comment...</p>
      <p v-if="error" class="error">Error: {{ error }}</p>
    </div>
  </div>
</template>
