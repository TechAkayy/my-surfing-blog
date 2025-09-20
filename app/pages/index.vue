<script setup lang="ts">
  import { heroImageUrl } from '@/utils/hero'
  const heroCaption = 'Welcome To'
  const heroTitle = 'Vue Designer'
  const heroDescription =
    'A desktop drag-and-drop editor for Mac, Windows and Linux that lets you visually design your Vue apps.'

  definePageMeta({
    // layout: 'default',
    // name: 'index',
    // alias: 'index',
    title: 'Home',
    description: 'Sip, Savor, and Spark Ideas at Cafe Bella Vista!',
    navOrder: 1,
    type: 'primary',
    icon: 'i-mdi-home',
    // ogImage: 'images/ogImage.png', // url or local images inside public folder, for eg, ~/public/images/ogImage.png
  })
</script>
<template>
    <div>
        <HeroSection/>
        <section class="py-16 px-4 md:px-8 bg-gray-100">
            <div class="max-w-6xl mx-auto">
                <h2 class="text-3xl md:text-4xl font-serif text-gray-800 text-center mb-12">Capturing the Perfect Wave</h2>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                    <div class="group relative overflow-hidden rounded-lg">
                        <img src="https://images.unsplash.com/photo-1603802244525-b873d7d653ad?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDE2fHxzdXJmJTIwYWN0aW9ufGVufDB8fHx8MTc1ODMyNTA5NHww&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop" alt="Dynamic surf action" class="w-full h-64 object-cover transition duration-300 group-hover:scale-105"/>
                        <div class="absolute bottom-0 left-0 right-0 bg-black/50 p-4 transition duration-300 opacity-0 group-hover:opacity-100">
                            <p class="text-white font-sans text-sm">Pipeline Dreams: Perfect Barrel at Sunset</p>
                        </div>
                    </div>
                    <div class="group relative overflow-hidden rounded-lg">
                        <img src="https://images.unsplash.com/photo-1677440952178-deb659bc14f4?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDExfHx3YXZlJTIwYWVyaWFsfGVufDB8fHx8MTc1ODMyNTA5NXww&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop" alt="Aerial wave view" class="w-full h-64 object-cover transition duration-300 group-hover:scale-105"/>
                        <div class="absolute bottom-0 left-0 right-0 bg-black/50 p-4 transition duration-300 opacity-0 group-hover:opacity-100">
                            <p class="text-white font-sans text-sm">Bird's Eye View: Ocean's Power</p>
                        </div>
                    </div>
                    <div class="group relative overflow-hidden rounded-lg">
                        <img src="https://images.unsplash.com/photo-1552842256-2b5a9e2d3659?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDE2fHxzdXJmZXIlMjBzaWxob3VldHRlfGVufDB8fHx8MTc1ODMyNTA5Nnww&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop" alt="Surfer silhouette" class="w-full h-64 object-cover transition duration-300 group-hover:scale-105"/>
                        <div class="absolute bottom-0 left-0 right-0 bg-black/50 p-4 transition duration-300 opacity-0 group-hover:opacity-100">
                            <p class="text-white font-sans text-sm">Golden Hour: Chasing the Last Wave</p>
                        </div>
                    </div>
                    <div class="group relative overflow-hidden rounded-lg">
                        <img src="https://images.unsplash.com/photo-1753013988902-98dad300522d?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDN8fGJlYWNoJTIwbGlmZXN0eWxlfGVufDB8fHx8MTc1ODMyNTA5Nnww&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop" alt="Beach lifestyle" class="w-full h-64 object-cover transition duration-300 group-hover:scale-105"/>
                        <div class="absolute bottom-0 left-0 right-0 bg-black/50 p-4 transition duration-300 opacity-0 group-hover:opacity-100">
                            <p class="text-white font-sans text-sm">Life's a Beach: Morning Preparation</p>
                        </div>
                    </div>
                    <div class="group relative overflow-hidden rounded-lg">
                        <img src="https://images.unsplash.com/photo-1580610448530-df1cb919b85a?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDEwfHx3YXZlJTIwY2xvc2V1cHxlbnwwfHx8fDE3NTgzMjUwOTd8MA&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop" alt="Wave closeup" class="w-full h-64 object-cover transition duration-300 group-hover:scale-105"/>
                        <div class="absolute bottom-0 left-0 right-0 bg-black/50 p-4 transition duration-300 opacity-0 group-hover:opacity-100">
                            <p class="text-white font-sans text-sm">Nature's Canvas: The Perfect Wave</p>
                        </div>
                    </div>
                    <div class="group relative overflow-hidden rounded-lg">
                        <img src="https://images.unsplash.com/photo-1645484013624-2b6a6782b5ce?ixid=M3wyMDkyMnwwfDF8c2VhcmNofDh8fHN1cmYlMjBsaWZlc3R5bGV8ZW58MHx8fHwxNzU4MzI1MDk3fDA&ixlib=rb-4.1.0q=85&fm=jpg&crop=faces&cs=srgb&w=1200&h=800&fit=crop" alt="Surf lifestyle" class="w-full h-64 object-cover transition duration-300 group-hover:scale-105"/>
                        <div class="absolute bottom-0 left-0 right-0 bg-black/50 p-4 transition duration-300 opacity-0 group-hover:opacity-100">
                            <p class="text-white font-sans text-sm">Living the Dream: Sunset Session</p>
                        </div>
                    </div>
                </div>
            </div>
        </section>
        <BlogPosts/>
    </div>
</template>
<style scoped></style>
