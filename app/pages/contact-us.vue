<script setup lang="ts">
  definePageMeta({
    // layout: 'default',
    // name: 'contact-us',
    // alias: 'contact-us',
    title: 'Contact Us',
    description: 'Contact Us',
    // hidden: true,
    navOrder: '4',
    type: 'primary',
    icon: 'i-mdi-home',
    // ogImage: 'images/ogImage.png', // url or local images inside public folder, for eg, ~/public/images/ogImage.png
  })
</script> 
<template> 
    <div class="min-h-screen bg-slate-50 dark:bg-neutral-950 py-12 px-4 sm:px-6 lg:px-8">
        <div class="max-w-3xl mx-auto">
            <div class="bg-white dark:bg-neutral-900 rounded-lg shadow-lg p-8">
                <h1 class="text-4xl font-serif text-primary-800 dark:text-primary-300 mb-8 text-center">
          Contact Us </h1>
                <p class="text-slate-600 dark:text-slate-400 mb-8 text-center">
          Have questions about surfing? Drop us a message! </p>
                <form class="space-y-6">
                    <div>
                        <label class="block text-sm font-medium text-slate-700 dark:text-slate-300 mb-2" for="name">Name</label>
                        <input id="name" type="text" class="w-full px-4 py-2 border border-slate-300 dark:border-slate-700 rounded-md bg-white dark:bg-neutral-800 text-gray-900 dark:text-white focus:ring-2 focus:ring-primary-500 focus:border-primary-500" required/>
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-700 dark:text-slate-300 mb-2" for="email">Email</label>
                        <input id="email" type="email" class="w-full px-4 py-2 border border-slate-300 dark:border-slate-700 rounded-md bg-white dark:bg-neutral-800 text-gray-900 dark:text-white focus:ring-2 focus:ring-primary-500 focus:border-primary-500" required/>
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-700 dark:text-slate-300 mb-2" for="subject">Subject</label>
                        <input id="subject" type="text" class="w-full px-4 py-2 border border-slate-300 dark:border-slate-700 rounded-md bg-white dark:bg-neutral-800 text-gray-900 dark:text-white focus:ring-2 focus:ring-primary-500 focus:border-primary-500" required/>
                    </div>
                    <div>
                        <label class="block text-sm font-medium text-slate-700 dark:text-slate-300 mb-2" for="message">Message</label>
                        <textarea id="message" rows="6" class="w-full px-4 py-2 border border-slate-300 dark:border-slate-700 rounded-md bg-white dark:bg-neutral-800 text-gray-900 dark:text-white focus:ring-2 focus:ring-primary-500 focus:border-primary-500" required></textarea>
                    </div>
                    <div class="flex justify-center">
                        <button type="submit" class="bg-primary-600 text-white px-8 py-3 rounded-md hover:bg-primary-700 transition duration-300">
                            Send Message
</button>
                    </div>
                </form>
                <div class="mt-12 grid grid-cols-1 md:grid-cols-3 gap-8">
                    <div class="text-center">
                        <div class="text-primary-600 dark:text-primary-400 mb-3">
                            <svg class="w-8 h-8 mx-auto" fill="none" stroke="currentColor" viewBox="0 0 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"/>
                            </svg>
                        </div>
                        <h3 class="font-medium text-slate-900 dark:text-white">Phone</h3>
                        <p class="mt-2 text-slate-600 dark:text-slate-400">
              +1 (555) 123-4567 </p>
                    </div>
                    <div class="text-center">
                        <div class="text-primary-600 dark:text-primary-400 mb-3">
                            <svg class="w-8 h-8 mx-auto" fill="none" stroke="currentColor" viewBox="0 0 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"/>
                            </svg>
                        </div>
                        <h3 class="font-medium text-slate-900 dark:text-white">Email</h3>
                        <p class="mt-2 text-slate-600 dark:text-slate-400">
              info@surfersparadise.com </p>
                    </div>
                    <div class="text-center">
                        <div class="text-primary-600 dark:text-primary-400 mb-3">
                            <svg class="w-8 h-8 mx-auto" fill="none" stroke="currentColor" viewBox="0 0 24 24" version="1.1" xmlns="http://www.w3.org/2000/svg">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"/>
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"/>
                            </svg>
                        </div>
                        <h3 class="font-medium text-slate-900 dark:text-white">Location</h3>
                        <p class="mt-2 text-slate-600 dark:text-slate-400">
              123 Surf Street<br/>Beach City, BC 12345 </p>
                    </div>
                </div>
            </div>
        </div>
    </div>     
</template> 
<style scoped></style>
