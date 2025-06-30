<template>
  <main class="container">
    <!-- HEADER -->
    <section class="header">
      <h1>Bonjour, je suis <span class="highlight">Mathias</span></h1>
      <p>Développeur web junior — React.js / Vue.js & Node.js</p>
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
      <h4>Exemples de projets réalisés en stage</h4>
      <div class="project-gallery">
        <div class="project">
          <img src="/images/image1.png" alt="Image projet 1" />
          <p>Interface d’administration - Vue.js + Node.js</p>
        </div>
        <div class="project">
          <img src="/images/image2.png" alt="Image projet 2" />
          <img src="/images/image3.png" alt="Image projet 3" />
          <p>Interface utilisateur pour l'utilisation d'une API - Vue.js + python</p>
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
    © 2025 Mathias — Portfolio personnel
  </footer>
</template>


<style scoped>
.container {
  max-width: 900px;
  margin: 2rem auto;
  padding: 2rem;
  font-family: system-ui, sans-serif;
  color: #2c3e50;
  line-height: 1.6;
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

.projects h4 {
  margin-top: 0.5rem;
  margin-bottom: 1.5rem;
  font-weight: 500;
  color: #555;
}

.project-gallery {
  display: flex;
  flex-direction: column;
  gap: 2rem;
  align-items: center;
}

.project {
  max-width: 700px;
  width: 100%;
  text-align: center;
}

.project img {
  width: 100%;
  height: auto;
  border-radius: 8px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.1);
  transition: transform 0.2s ease;
}



.footer {
  margin-top: 4rem;
  text-align: center;
  font-size: 0.9rem;
  color: #999;
}
</style>

