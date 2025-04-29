<template>
  <div class="bg-image min-h-screen bg-color-gray-400">
    <nav class="">
      <div class="max w-7x1 mx-auto my-auto  px-4 ">
       
        <div class="flex justify-between items-center">
          <div class="flex items-center">
            <router-link to="/" class="text-black  px-2 mx-10 mt-10 text-4xl font-extrabold hover:text-gray-900">IR</router-link>
          </div>
          
          
          <div class="flex items-center">
            <router-link to="/about" class="text-white  px-2 mx-10 mt-8 text-xl hover:text-gray-400">About me</router-link>
            <router-link to="/skills" class="text-white  px-2 mx-10 mt-8 text-xl hover:text-gray-400">Skills</router-link>
            <router-link to="/projects" class="text-white  px-2 mx-10 mt-8 text-xl hover:text-gray-400">Projects</router-link>
            <router-link to="/contact" class="rounded-3xl bg-gray-200 text-black text-xl py-1 px-3 mx-10 mt-8 hover:bg-white hover:text-gray-400">Contact me</router-link>
          </div>
      </div>
      </div>
    </nav>
    <router-view />
  </div>
</template>
  
<script setup>

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