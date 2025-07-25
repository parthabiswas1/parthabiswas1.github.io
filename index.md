---
layout: default
title: Home
---
<link rel="stylesheet" href="/assets/css/style.css">

<!-- Sticky Navigation Bar -->
<nav class="top-nav">
  <div class="nav-container">
    <a class="nav-brand" href="{{ '/' | relative_url }}">Partha Biswas</a>
    <div class="nav-links">
      <a href="{{ '/' | relative_url }}">Home</a>
      <a href="{{ '/projects/' | relative_url }}">Projects</a>
      <a href="#about-me">About</a>
      <a href="#contact">Contact</a>
    </div>
  </div>
</nav>

# Partha Biswas
*AI • ML • Agentic AI Engineer*

---

<!-- About Me Section -->
<section id="about-me" class="about-me">
  <div class="about-container">
    <div class="about-image">
      <img src="/assets/images/profile.jpg" alt="Partha Biswas">
    </div>
    <div class="about-text">
      <p>
        I’m passionate about designing cutting-edge AI/ML solutions and developing
        autonomous, agentic AI systems. With expertise in data science, model optimization,
        and real-world deployment, I strive to deliver intelligent and impactful products.
      </p>
      <p>
        <a href="https://linkedin.com/in/YOUR-LINKEDIN" target="_blank">LinkedIn</a> |
        <a href="https://github.com/parthabiswas1" target="_blank">GitHub</a> |
        <a href="mailto:YOUR-EMAIL">Email Me</a>
      </p>
    </div>
  </div>
</section>

---

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

