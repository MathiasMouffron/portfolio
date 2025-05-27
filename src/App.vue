<template>
  <main class="container">
    <section class="header">
      <h1>Bonjour, je suis <span class="highlight">Mathias</span></h1>
      <p>Développeur web junior - Angular.js/Vue.js & Node.js/Express</p>
    </section>

    <section class="about">
      <h2>À propos</h2>
      <p>
        Passionné par le développement web fullstack, je me forme activement sur la stack MERN.
        Je cherche à rejoindre une équipe motivée ou à contribuer à des projets concrets.
      </p>
    </section>

    <section class="projects">
      <h2>Projets</h2>
      <ul>
        <li>Aucun projet publié pour le moment - en cours de construction !</li>
      </ul>
    </section>

    <section class="links">
      <h2>Me contacter</h2>
      <p>Mon GitHub : <a href="https://github.com/MathiasMouffron" target="_blank">github.com/MathiasMouffron</a></p>
      <!-- Formulaire de contact à ajouter plus tard -->
    </section>
  </main>
  <footer style="margin-top: 4rem; text-align: center; font-size: 0.9rem; color: #999;">
    © 2025 Mathias — Portfolio personnel
  </footer>
</template>

<style scoped>
.container {
  max-width: 800px;
  margin: 2rem auto;
  padding: 2rem;
  font-family: system-ui, sans-serif;
  line-height: 1.6;
  color: #2c3e50;
}

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

ul {
  list-style: disc;
  padding-left: 1.5rem;
}

.footer {
  margin-top: 4rem;
  text-align: center;
  font-size: 0.9rem;
  color: #999;
}
</style>
