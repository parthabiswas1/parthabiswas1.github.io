---
layout: default
title: Home
---

<!-- Sticky Navigation Bar -->
<nav class="top-nav">
  <div class="nav-container">
    <a class="nav-brand" href="{{ '/' | relative_url }}">Machine Learning (ML) & Artificial Intelligence (AI) - University of California, Berkeley</a>
    <div class="nav-links">
      <a href="{{ '/' | relative_url }}">Home</a>
      <a href="{{ '/projects/' | relative_url }}">Projects</a>
      <a href="#about-me">About</a>
      <a href="#contact">Contact</a>
    </div>
  </div>
</nav>

<style>
.top-nav {
  position: sticky;
  top: 0;
  z-index: 1000;
  background: #fff;
  border-bottom: 1px solid #ddd;
  padding: 10px 20px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.05);
}
.nav-container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.nav-brand {
  font-weight: bold;
  font-size: 1.2em;
  color: #0366d6;
  text-decoration: none;
}
.nav-links a {
  margin-left: 15px;
  text-decoration: none;
  color: #333;
  font-size: 0.95em;
}
.nav-links a:hover {
  color: #0366d6;
}
</style>

<!-- About Me Section -->
<section id="about-me" class="about-me">
  <div class="about-container">
    <div class="about-image">
      <img src="/assets/images/partha.jpeg" alt="Partha Biswas">
    </div>
    <div class="about-text">
      <p>
        I’m passionate about technology. I manage technical programs and projects and make sure that I keep upto-date about the latest in technology. Below I would like to showcase data analysis using Pandas, Dataframe, Numpy, Matplotlib, Seaborn, Potly.  I will continue to add projects on Models and Agentic AI systems.  With expertise in data science, model optimization, Agentic AI and real-world deployment, I strive to manage and deliver intelligent and impactful products.
      </p>
      <p>
        <a href="https://linkedin.com/parthapratimbiswas/" target="_blank">LinkedIn</a> |
        <a href="https://github.com/parthabiswas1" target="_blank">GitHub</a> |
        <a href="mailto:YOUR-EMAIL">Email Me</a>
      </p>
    </div>
  </div>
</section>

<style>
.about-me {
  background: #f9f9f9;
  padding: 20px;
  border-radius: 10px;
  margin-bottom: 30px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
}
.about-container {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 20px;
}
.about-image img {
  width: 140px;
  height: 140px;
  object-fit: cover;
  border-radius: 50%;
  border: 2px solid #ddd;
}
.about-text {
  flex: 1;
  font-size: 1em;
  line-height: 1.6;
}
.about-text a {
  text-decoration: none;
  color: #0366d6;
}
.about-text a:hover {
  text-decoration: underline;
}
</style>

<!-- Featured Project Section -->
{% assign featured = site.projects | first %}
{% if featured %}
<section class="featured-project">
  <div class="featured-image">
    {% if featured.image %}
      <img src="{{ featured.image }}" alt="{{ featured.title }}">
    {% endif %}
  </div>
  <div class="featured-content">
    <h2>Featured Project: <a href="{{ featured.url }}">{{ featured.title }}</a></h2>
    <p>{{ featured.description }}</p>
    <div class="featured-links">
      <a href="{{ featured.github }}" target="_blank">View Repo</a>
      {% if featured.colab %}
        <a href="{{ featured.colab }}" target="_blank">Notebook</a>
      {% endif %}
    </div>
  </div>
</section>
{% endif %}

<style>
.featured-project {
  display: flex;
  flex-direction: column;
  align-items: center;
  background: #f9f9f9;
  padding: 20px;
  border-radius: 10px;
  margin-bottom: 30px;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
}
.featured-image img {
  width: 100%;
  max-width: 500px;
  border-radius: 10px;
  margin-bottom: 15px;
}
.featured-content h2 {
  margin: 0 0 10px;
}
.featured-links a {
  display: inline-block;
  margin-right: 10px;
  padding: 6px 10px;
  background: #0366d6;
  color: #fff !important;
  border-radius: 5px;
  text-decoration: none;
  font-size: 0.9em;
}
.featured-links a:hover {
  background: #024a9a;
}
</style>

---

## All Projects
<div class="project-grid">
{% for project in site.projects %}
  <div class="project-card">
    {% if project.image %}
      <img src="{{ project.image }}" alt="{{ project.title }}">
    {% endif %}
    <h3><a href="{{ project.url }}">{{ project.title }}</a></h3>
    <p>{{ project.description }}</p>
    <div class="project-links">
      <a href="{{ project.github }}" target="_blank">View Repo</a>
      {% if project.colab %}
        <a href="{{ project.colab }}" target="_blank">Notebook</a>
      {% endif %}
    </div>
  </div>
{% endfor %}
</div>

---

[View All Projects →](/projects/)

<style>
.project-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  margin-top: 20px;
}
.project-card {
  background: #fff;
  border: 1px solid #ddd;
  border-radius: 10px;
  padding: 15px;
  box-shadow: 0 2px 6px rgba(0,0,0,0.05);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
  display: flex;
  flex-direction: column;
}
.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}
.project-card img {
  width: 100%;
  border-radius: 8px;
  margin-bottom: 10px;
  object-fit: cover;
  max-height: 160px;
}
.project-card h3 {
  margin: 0 0 10px;
  font-size: 1.2em;
}
.project-links a {
  display: inline-block;
  margin-right: 10px;
  padding: 6px 10px;
  background: #0366d6;
  color: #fff !important;
  border-radius: 5px;
  text-decoration: none;
  font-size: 0.9em;
}
.project-links a:hover {
  background: #024a9a;
}
</style>

---

<!-- Contact Section -->
<section id="contact" class="contact-section">
  <h2>Contact Me</h2>
  <p>If you'd like to collaborate, discuss projects, or have opportunities, feel free to reach out!</p>
  <p>
    <a href="mailto:YOUR-EMAIL" class="contact-btn">Email Me</a>
    <!-- Optionally link to Google Form -->
    <!-- <a href="YOUR-GOOGLE-FORM-LINK" class="contact-btn" target="_blank">Contact Form</a> -->
  </p>
</section>

<style>
.contact-section {
  background: #f9f9f9;
  padding: 20px;
  border-radius: 10px;
  margin-top: 40px;
  text-align: center;
  box-shadow: 0 2px 8px rgba(0, 0, 0, 0.05);
}
.contact-btn {
  display: inline-block;
  margin: 10px;
  padding: 10px 15px;
  background: #0366d6;
  color: #fff !important;
  border-radius: 5px;
  text-decoration: none;
  font-size: 1em;
}
.contact-btn:hover {
  background: #024a9a;
}
</style>
