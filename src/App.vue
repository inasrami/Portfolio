<template>
  <div class="bg-image min-h-screen bg-color-gray-400">
    <nav class="realtive">
      <div class="max w-7x1 mx-auto my-auto  px-4 ">
       
        <div class="flex justify-between items-center">
          <div class="flex items-center">
            <router-link to="/" class="text-black  px-2 mx-10 mt-10 text-4xl font-extrabold hover:text-gray-900">IR</router-link>
          </div>
          
           <!-- Mobile menu button -->
           <button @click="toggleMenu" class="md:hidden mt-8 text-white focus:outline-none">
            <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path v-if="!isMenuOpen" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16"/>
              <path v-else stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12"/>
            </svg>
          </button>

          <div class="hidden md:flex items-center">
            <router-link to="/about" class="text-white  px-2 mx-10 mt-8 text-xl md:text-xl hover:text-gray-400">About me</router-link>
            <router-link to="/skills" class="text-white  px-2 mx-10 mt-8 text-xl md:text-xl hover:text-gray-400">Skills</router-link>
            <router-link to="/projects" class="text-white  px-2 mx-10 mt-8 text-xl md:text-xl hover:text-gray-400">Projects</router-link>
            <router-link to="/contact" class="rounded-3xl bg-gray-200 text-black md:text-xl text-xl py-1 px-3 mx-10 mt-8 hover:bg-white hover:text-gray-400">Contact me</router-link>
          </div>
      </div>
      <div v-show="isMenuOpen" class="md:hidden">
          <div class="flex flex-col items-center py-4 bg-gray-800 rounded-lg mt-4">
            <router-link @click="closeMenu" to="/about" class="text-white py-2 hover:text-gray-400">About me</router-link>
            <router-link @click="closeMenu" to="/skills" class="text-white py-2 hover:text-gray-400">Skills</router-link>
            <router-link @click="closeMenu" to="/projects" class="text-white py-2 hover:text-gray-400">Projects</router-link>
            <router-link @click="closeMenu" to="/contact" class="text-white py-2 hover:text-gray-400">Contact me</router-link>
          </div>
        </div>
      </div>
    </nav>
    <router-view />
  </div>
</template>
  
<script setup>
import { ref } from 'vue'

const isMenuOpen = ref(false)

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

const closeMenu = () => {
  isMenuOpen.value = false
}
</script>
<style>
.bg-image {
  background-image: URL('@/assets/bg.png');
  background-position: right;
  background-repeat: no-repeat;
  background-size: 55% 100%;
  background-color: rgb(160, 160, 160);
}




</style>