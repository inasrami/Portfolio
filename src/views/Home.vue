<template>
  <div class="flex justify-between items-center h-[calc(100vh-80px)] px-20 overflow-hidden">
    <!-- Left side content -->
    
    <div  class="flex flex-col space-y-4 animate-slide-in-left">
      <div class="flex flex-col">
        <h1 class="text-2xl font-bold text-gray-800">My name is</h1>
        <h2 class="text-7xl font-bold text-gray-800">Inas Rami</h2>
        <h3 class="text-2xl font-extralight text-gray-700">I am a Frontend Developer</h3>
      </div>
      
      <!-- Social links -->
      
      <div class="flex space-x-4 mt-6 ">
        <a href="https://www.instagram.com/inas_rami/" class="text-3xl text-gray-800 hover:text-red-500 hover:scale-125 transition-all duration-300">
          <i class="fa-brands fa-instagram"></i>
        </a>
        <a href="https://www.linkedin.com/in/inas-rami-a72709200/" class="text-3xl text-gray-800 hover:text-blue-500 hover:scale-125 transition-all duration-300">
          <i class="fa-brands fa-linkedin"></i>
        </a>
        <a href="https://github.com/inasrami" class="text-3xl text-gray-800 hover:text-gray-600 hover:scale-125 transition-all duration-300">
          <i class="fa-brands fa-github"></i>
        </a>
        <a href="https://www.facebook.com/Inkoo.ll" class="text-3xl text-gray-800 hover:text-blue-700 hover:scale-125 transition-all duration-300">
          <i class="fa-brands fa-facebook"></i>
        </a>
      </div>
    </div>

    <!-- Right side image -->
    <div class="flex items-end h-full animate-slide-in-right">
      <img 
        src="../assets/inas.png" 
        alt="Inas Rami" 
        class="w-[450px] h-auto object-cover"
      >
    </div>
  </div>
</template>
  <style >
  .slide-enter-active, .slide-leave-active {
  transition: all 0.4s ease;
}
.slide-enter-from {
  transform: translateX(-100%);
}
.slide-leave-to {
  transform: translateX(-100%);
}
  </style>
  <script setup>
  </script>