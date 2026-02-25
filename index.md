---
layout: default
permalink: /
---

<div class="about-section">
  <img src="{{ '/profile.png' | relative_url }}" alt="Eireann Coelho" class="profile-image">
  <div class="about-text">
    <h1>Hi, I'm Eireann</h1>
    <p>I'm a senior at the University of Oregon, pursuing a Bachelor's in Computer Science with minors in Multimedia and Dance. My academic journey has led me to discover passions for technology, creativity, and movement. I'm excited to find opportunities that allow me to merge these interests in unique and innovative ways. I thrive at the intersection of logic and artistry—whether it's solving complex coding problems or expressing myself through dance.</p>
    <p>I have a deep interest in software development, multimedia design, and how technology can elevate artistic expression. My coursework has given me hands-on experience in coding, web development, UX/UI design, and visual storytelling. Additionally, my background in dance has taught me discipline, collaboration, and how to think outside the box—skills I bring into every project I work on.</p>
    <p>As I continue my studies with an additional year, I'm actively seeking 2025 internship opportunities that will allow me to bridge the gap between technology and creativity. I'm particularly interested in roles where I can contribute to innovative tech solutions while incorporating elements of multimedia design or performance arts.</p>
  </div>
</div>

<section class="recent-posts">
  <h2>Recent Posts</h2>
  <ul class="post-list">
    {% for post in site.posts limit:10 %}
    <li>
      <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
      <div class="post-meta">{{ post.date | date: "%B %d, %Y" }}</div>
    </li>
    {% else %}
    <li><em>No posts yet. Check back soon!</em></li>
    {% endfor %}
  </ul>
</section>
