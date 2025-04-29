<template>
    <div class="projects-container">
      <div class="projects-grid">
        <div v-for="project in projects" :key="project.id" class="project-card">
          <img :src="project.image" :alt="project.title">
          <div class="project-content">
            <h3>{{ project.title }}</h3>
            <p>{{ project.description }}</p>
            <div class="project-tech">
              <span v-for="tech in project.technologies" :key="tech" class="tech-tag">
                {{ tech }}
              </span>
            </div>
            <div class="project-links">
              <a :href="project.github" target="_blank">GitHub</a>
              <a :href="project.demo" target="_blank">Live Demo</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        projects: [
          {
            id: 1,
            title: 'Project Name',
            description: 'Brief description of the project',
            image: '/path/to/image.jpg',
            technologies: ['Vue.js', 'Node.js', 'MongoDB'],
            github: 'https://github.com/username/project',
            demo: 'https://demo-link.com'
          },
          // Add more projects here
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .projects-container {
    padding: 2rem;
  }
  
  .projects-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
    gap: 2rem;
  }
  
  .project-card {
    border-radius: 8px;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    transition: transform 0.3s ease;
  }
  
  .project-card:hover {
    transform: translateY(-5px);
  }
  
  .project-card img {
    width: 100%;
    height: 200px;
    object-fit: cover;
  }
  
  .project-content {
    padding: 1.5rem;
  }
  
  .tech-tag {
    display: inline-block;
    padding: 0.25rem 0.75rem;
    margin: 0.25rem;
    background-color: #e9ecef;
    border-radius: 15px;
    font-size: 0.875rem;
  }
  
  .project-links {
    margin-top: 1rem;
  }
  
  .project-links a {
    margin-right: 1rem;
    text-decoration: none;
    color: #007bff;
  }
  </style>