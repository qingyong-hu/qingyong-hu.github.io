---
layout: archive
title: "CV"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

<div class="cv-buttons">
  <a href="/files/cv.pdf" class="btn btn--primary" target="_blank">Download CV as PDF</a>
  <a href="#" class="btn" id="toggle-pdf-view">Toggle PDF View</a>
</div>

<div id="pdf-view" style="display: none;">
  {% include pdf-viewer.html pdf_url="https://qingyong-hu.github.io/files/cv/Qingyong_CV_latest.pdf" %}
</div>

<div id="cv-content">
  <!-- Your existing CV content here -->
  {% include cv-content.html %}
</div>

<script>
  document.getElementById('toggle-pdf-view').addEventListener('click', function(e) {
    e.preventDefault();
    var pdfView = document.getElementById('pdf-view');
    var cvContent = document.getElementById('cv-content');
    
    if (pdfView.style.display === 'none') {
      pdfView.style.display = 'block';
      cvContent.style.display = 'none';
      this.textContent = 'Show HTML Version';
    } else {
      pdfView.style.display = 'none';
      cvContent.style.display = 'block';
      this.textContent = 'Toggle PDF View';
    }
  });
</script>

<!-- {% include base_path %}

Education
======
* Ph.D in Version Control Theory, GitHub University, 2018 (expected)
* M.S. in Jekyll, GitHub University, 2014
* B.S. in GitHub, GitHub University, 2012

Work experience
======
* Spring 2024: Academic Pages Collaborator
  * GitHub University
  * Duties includes: Updates and improvements to template
  * Supervisor: The Users

* Fall 2015: Research Assistant
  * GitHub University
  * Duties included: Merging pull requests
  * Supervisor: Professor Hub

* Summer 2015: Research Assistant
  * GitHub University
  * Duties included: Tagging issues
  * Supervisor: Professor Git
  
Skills
======
* Skill 1
* Skill 2
  * Sub-skill 2.1
  * Sub-skill 2.2
  * Sub-skill 2.3
* Skill 3

Publications
======
  <ul>{% for post in site.publications reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Talks
======
  <ul>{% for post in site.talks reversed %}
    {% include archive-single-talk-cv.html  %}
  {% endfor %}</ul>
  
Teaching
======
  <ul>{% for post in site.teaching reversed %}
    {% include archive-single-cv.html %}
  {% endfor %}</ul>
  
Service and leadership
======
* Currently signed in to 43 different slack teams -->
