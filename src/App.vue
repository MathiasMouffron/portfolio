<template>
  <main class="container">
    <!-- HEADER -->
    <section class="header">
      <h1>Bonjour, je suis <span class="highlight">Mathias</span></h1>
      <p>Développeur web junior - React.js / Vue.js & Node.js</p>
    </section>

    <!-- À PROPOS -->
    <section class="about">
      <h2>À propos</h2>
      <p>
        Passionné par le web, je me forme activement au développement fullstack.
        Je cherche à rejoindre une équipe motivée ou à contribuer à des projets concrets. 
      </p>
    </section>

    <!-- PROJETS -->
    <section class="projects">
      <h2>Projets</h2>

      <div v-for="(project, index) in projects" :key="index" class="accordion">
        <button @click="toggle(index)">
          {{ project.title }}
          <span>{{ activeIndex === index ? '▲' : '▼' }}</span>
        </button>

        <div v-show="activeIndex === index" class="content">
          <p>{{ project.description }}</p>
          <p v-if="project.link">
            <a :href="project.link" target="_blank">Voir le code sur GitHub</a>
          </p>
          <div class="screenshots">
            <img v-for="(img, i) in project.images" :key="i" :src="img" alt="screenshot" />
          </div>
          
        </div>
      </div>
    </section>

    <!-- CONTACT -->
    <section class="links">
      <h2>Me contacter</h2>
      <p>Email : <a href="mailto:mathias791@outlook.fr">mathias791@outlook.fr</a></p>
      <p>LinkedIn : <a href="https://www.linkedin.com/in/mathias-mouffron-458378328/" target="_blank">Profil LinkedIn</a></p>
      <p>GitHub : <a href="https://github.com/MathiasMouffron" target="_blank">github.com/MathiasMouffron</a></p>
    </section>
  </main>

  <footer class="footer">
    © 2025 Mathias - Portfolio personnel
  </footer>
</template>

<script setup>
import { ref } from 'vue'

const activeIndex = ref(null)

const toggle = (index) => {
  activeIndex.value = activeIndex.value === index ? null : index
}

const projects = [
  {
    title: 'Projet de stage - Interface d’administration',
    description: 'Application Vue.js + Node.js ',
    images: ['/images/image1.png','/images/image2.png','/images/image3.png'],
  },
  {
    title: 'Projet universitaire - Blog',
    description: 'Blog de jeux vidéo avec Symfony sur Docker.',
    images: ['/images/image4.png', '/images/image5.png', '/images/image6.png'],
    link: 'https://github.com/MathiasMouffron/Blog-Symfony'
  }
]
</script>

<style scoped>
.container {
  max-width: 900px;
  margin: 2rem auto;
  padding: 2rem;
  font-family: system-ui, sans-serif;
  color: #2c3e50;
  line-height: 1.6;
}

/* --- Sections principales --- */
.header {
  text-align: center;
  margin-bottom: 3rem;
}

.highlight {
  color: #42b883;
}

h1, h2 {
  margin-bottom: 0.5rem;
}

a {
  color: #42b883;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}

.footer {
  margin-top: 4rem;
  text-align: center;
  font-size: 0.9rem;
  color: #999;
}

/* --- Accordéon / Projets --- */
.accordion {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-top: 1.5rem;
}

.accordion button {
  all: unset;
  width: 95%;
  padding: 1rem 1.2rem;
  background: #f3f3f3;
  border-radius: 6px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-weight: 600;
  font-size: 1.05rem;
  color: #2c3e50;
  cursor: pointer;
  transition: background-color 0.2s ease;
}

.accordion button:hover {
  background-color: #e6e6e6;
}

.content {
  background: #fafafa;
  padding: 1rem 1.2rem;
  border-radius: 6px;
  box-shadow: 0 0 4px rgba(0,0,0,0.05);
  font-size: 0.95rem;
  color: #444;
  line-height: 1.5;
}

.screenshots img {
  max-width: 100%;
  height: auto;
  margin-top: 1rem;
  border-radius: 6px;
  box-shadow: 0 1px 4px rgba(0,0,0,0.1);
}
</style>

