<template>
    <div class="projects-container animate-fa">
      <div class="iframe-wrapper">
        <iframe 
          :src="currentWebsite"
          :title="currentTitle"
          class="website-frame"
          ref="frame"
          allowfullscreen>
        </iframe>
      </div>
      <div class="website-controls">
        <button 
          v-for="site in websites" 
          :key="site.url"
          @click="loadWebsite(site)"
          :class="{ active: currentWebsite === site.url }">
          {{ site.title }}
        </button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        currentWebsite: '',
        currentTitle: '',
        websites: [
          {
            title: 'Barbers Unity',
            url: 'https://barbersunity.com/'
          },
        //   {
        //     title: 'My Blog',
        //     url: 'https://yourblog.com'
        //   },
          // Add more websites as needed
        ]
      }
    },
    methods: {
      loadWebsite(site) {
        this.currentWebsite = site.url
        this.currentTitle = site.title
      }
    },
    mounted() {
      if (this.websites.length > 0) {
        this.loadWebsite(this.websites[0])
      }
    }
  }
  </script>
  
  <style scoped>
  .projects-container {
    width: 100%;
    height: 100vh;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    padding: 1rem;
  }
  
  .iframe-wrapper {
    flex: 1;
    width: 100%;
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  .website-frame {
    width: 100%;
    height: 100%;
    border: none;
  }
  
  .website-controls {
    display: flex;
    gap: 1rem;
    justify-content: center;
    padding: 1rem;
  }
  
  .website-controls button {
    padding: 0.5rem 1rem;
    border: none;
    border-radius: 4px;
    background: #f0f0f0;
    cursor: pointer;
    transition: all 0.3s ease;
  }
  
  .website-controls button.active {
    background: #007bff;
    color: white;
  }
  
  .website-controls button:hover {
    transform: translateY(-2px);
  }
  </style>