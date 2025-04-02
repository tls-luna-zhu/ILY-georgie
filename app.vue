<template>
  <div class="min-h-screen pixel-bg">
    <div class="container mx-auto px-4 py-16">
      <div class="pixel-container bg-white/90 backdrop-blur-sm max-w-2xl mx-auto p-8 rounded-lg">
        <h1 class="text-3xl text-center mb-8 text-pink-400">
          Luna's Space
        </h1>
        
        <div class="grid grid-cols-1 md:grid-cols-3 gap-6 mb-8">
          <div class="pixel-button flex items-center justify-center gap-2 bg-purple-200 hover:bg-pink-300 text-gray-700 rounded-lg">
            <a href="https://blog.lunazhu.top" target="_blank" class="block text-center">
              <svg class="w-24 h-24 mx-auto mb-4" viewBox="0 0 32 32">
                <rect x="8" y="6" width="16" height="20" fill="#ff69b4"/>
                <rect x="10" y="8" width="12" height="2" fill="white"/>
                <rect x="10" y="12" width="12" height="2" fill="white"/>
                <rect x="10" y="16" width="12" height="2" fill="white"/>
                <rect x="10" y="20" width="8" height="2" fill="white"/>
              </svg>
              <h2 class="text-lg text-pink-600 mb-2">Luna's Blog</h2>
              <p class="text-xs text-pink-700">My thoughts and stories</p>
            </a>
          </div>
          
          <div class="pixel-button flex items-center justify-center gap-2 bg-blue-200 hover:bg-pink-300 text-gray-700 rounded-lg">
            <a href="https://estropad.lunazhu.top" target="_blank" class="block text-center">
              <svg class="w-24 h-24 mx-auto mb-4" viewBox="0 0 32 32">
                <rect x="6" y="6" width="20" height="20" fill="#4a9eff"/>
                <rect x="8" y="4" width="4" height="4" fill="#ff69b4"/>
                <rect x="20" y="4" width="4" height="4" fill="#ff69b4"/>
                <rect x="8" y="12" width="4" height="4" fill="white"/>
                <rect x="14" y="12" width="4" height="4" fill="white"/>
                <rect x="20" y="12" width="4" height="4" fill="white"/>
                <rect x="8" y="18" width="4" height="4" fill="white"/>
                <rect x="14" y="18" width="4" height="4" fill="white"/>
                <rect x="20" y="18" width="4" height="4" fill="white"/>
              </svg>
              <h2 class="text-lg text-blue-600 mb-2">Estropad Tracker</h2>
              <p class="text-xs text-blue-700">Track your schedule</p>
            </a>
          </div>
          
          <div class="pixel-button flex items-center justify-center gap-2 bg-purple-200 hover:bg-pink-300 text-gray-700 rounded-lg">
            <a href="https://todo.lunazhu.top" target="_blank" class="block text-center">
              <svg class="w-24 h-24 mx-auto mb-4" viewBox="0 0 32 32">
                <rect x="6" y="6" width="20" height="20" fill="#9c27b0"/>
                <rect x="8" y="8" width="12" height="3" fill="white"/>
                <rect x="22" y="8" width="3" height="3" fill="#4caf50"/>
                <rect x="8" y="14" width="12" height="3" fill="white"/>
                <rect x="22" y="14" width="3" height="3" fill="#4caf50"/>
                <rect x="8" y="20" width="12" height="3" fill="white"/>
                <rect x="22" y="20" width="3" height="3" fill="#4caf50"/>
              </svg>
              <h2 class="text-lg text-purple-600 mb-2">Todo List</h2>
              <p class="text-xs text-purple-700">Stay organized</p>
            </a>
          </div>
        </div>

        <div class="mt-8 pt-4 border-t-4 border-dotted border-gray-200">
          <a href="https://github.com/tls-luna-zhu" target="_blank"
             class="pixel-button flex items-center justify-center gap-2 bg-gray-200 hover:bg-gray-300 text-gray-700 rounded-lg">
            <svg class="w-5 h-5" viewBox="0 0 16 16">
              <path fill="currentColor" d="M8 0C3.58 0 0 3.58 0 8c0 3.54 2.29 6.53 5.47 7.59.4.07.55-.17.55-.38 0-.19-.01-.82-.01-1.49-2.01.37-2.53-.49-2.69-.94-.09-.23-.48-.94-.82-1.13-.28-.15-.68-.52-.01-.53.63-.01 1.08.58 1.23.82.72 1.21 1.87.87 2.33.66.07-.52.28-.87.51-1.07-1.78-.2-3.64-.89-3.64-3.95 0-.87.31-1.59.82-2.15-.08-.2-.36-1.02.08-2.12 0 0 .67-.21 2.2.82.64-.18 1.32-.27 2-.27.68 0 1.36.09 2 .27 1.53-1.04 2.2-.82 2.2-.82.44 1.1.16 1.92.08 2.12.51.56.82 1.27.82 2.15 0 3.07-1.87 3.75-3.65 3.95.29.25.54.73.54 1.48 0 1.07-.01 1.93-.01 2.2 0 .21.15.46.55.38A8.013 8.013 0 0016 8c0-4.42-3.58-8-8-8z"/>
            </svg>
            <span class="text-xs">Find me on GitHub</span>
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { onMounted } from 'vue'
import { gsap } from 'gsap'

onMounted(() => {
  gsap.from('.pixel-container', {
    y: 50,
    opacity: 0,
    duration: 1,
    ease: 'power2.out'
  })

  gsap.from('.bg-pink-200, .bg-blue-200, .bg-purple-200', {
    scale: 0.8,
    opacity: 0,
    duration: 0.6,
    stagger: 0.2,
    ease: 'back.out'
  })

  gsap.from('.border-t-4', {
    width: 0,
    opacity: 0,
    duration: 1,
    delay: 1,
    ease: 'power2.out'
  })
})
</script>
