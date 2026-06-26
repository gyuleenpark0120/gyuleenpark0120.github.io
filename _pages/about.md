---
layout: about
title: about
permalink: /
subtitle:

bio: |
  I am a scientist with a Ph.D. background in energy and environmental application systems, now working at the intersection of AI and scientific discovery. My recent work focuses on LLM-based agentic systems, scientific data pipelines, and AI-assisted R&D workflows.

  My long-term interest is building AI systems that help researchers turn complex scientific knowledge into better experimental and technical decisions. I'm excited to keep building at this intersection and contribute to more transparent, useful, and actionable AI for science.

profile:
  align: right
  image: prof_pic.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p style="font-size:0.82rem; margin:0; text-align:center; display:block; width:100%; overflow-wrap:break-word; word-break:break-word;">
    <em>Eiffel Tower, Paris, France, 2026</em>
    </p>

selected_papers: False
social: true

announcements:
  enabled: False
  scrollable: False
  limit: 5

latest_posts:
  enabled: False
  scrollable: False
  limit: 3
---

<div class="about-timeline">

  <div class="timeline-section tl-animate">
    <h3 class="timeline-heading"><i class="fa-solid fa-briefcase"></i> Experience</h3>
    <div class="timeline-card tl-animate">
      <span class="tl-date">2024 – Present</span>
      <div class="tl-title">Senior Scientist, Battery-AI Team</div>
      <div class="tl-place">LLM Team (Battery-AI)</div>
      <div class="tl-place">SES AI · Woburn, MA, USA</div>
    </div>
    <div class="timeline-card tl-animate">
      <span class="tl-date">2020 – 2024</span>
      <div class="tl-title">Graduate Researcher (Ph.D.)</div>
      <div class="tl-place">Multi-Scale Energy Science & Technology Laboratory</div>
      <div class="tl-place">Seoul National University · Seoul, South Korea</div>
    </div>
    <div class="timeline-card tl-animate">
      <span class="tl-date">2018 – 2020</span>
      <div class="tl-title">Graduate Researcher (M.S.)</div>
      <div class="tl-place">Water Environment & Energy Lab</div>
      <div class="tl-place">Seoul National University · Seoul, South Korea</div>
    </div>
  </div>

  <div class="timeline-section tl-animate">
    <h3 class="timeline-heading"><i class="fa-solid fa-graduation-cap"></i> Education</h3>
    <div class="timeline-card tl-animate">
      <span class="tl-date">2020 – 2024</span>
      <div class="tl-title">Ph.D. in Chemical and Biological Engineering</div>
      <div class="tl-place">Seoul National University</div>
      <div class="tl-place">P.I. Prof. Jang Wook Choi</div>
    </div>
    <div class="timeline-card tl-animate">
      <span class="tl-date">2018 – 2020</span>
      <div class="tl-title">M.S. in Chemical and Biological Engineering</div>
      <div class="tl-place">Seoul National University</div>
      <div class="tl-place">P.I. Prof. Jeyong Yoon</div>
    </div>
    <div class="timeline-card tl-animate">
      <span class="tl-date">2014 – 2018</span>
      <div class="tl-title">B.S. in Environmental and Civil Engineering</div>
      <div class="tl-place">Korea University <em>(Cum Laude)</em></div>
    </div>
  </div>

  <div class="timeline-section tl-animate">
    <h3 class="timeline-heading"><i class="fa-solid fa-code"></i> Skills</h3>
    <div class="timeline-card tl-animate">
      <div class="skills-grid">
        <div class="skill-category">
          <span class="skill-label">AI for Science</span>
          <div class="skill-tags">
            <span class="skill-tag">Agentic AI</span>
            <span class="skill-tag">LLM-as-a-Judge</span>
            <span class="skill-tag">Literature Mining</span>
            <span class="skill-tag">Knowledge Extraction</span>
          </div>
        </div>
        <div class="skill-category">
          <span class="skill-label">Scientific Data</span>
          <div class="skill-tags">
            <span class="skill-tag">Python</span>
            <span class="skill-tag">Data Pipelines</span>
            <span class="skill-tag">Dataset Curation</span>
          </div>
        </div>
        <div class="skill-category">
          <span class="skill-label">Materials & Chemistry</span>
          <div class="skill-tags">
            <span class="skill-tag">Li-ion/Metal Batteries</span>
            <span class="skill-tag">Electrolyte Design</span>
            <span class="skill-tag">Interphase Chemistry</span>
          </div>
        </div>
        <div class="skill-category">
          <span class="skill-label">Characterization</span>
          <div class="skill-tags">
            <span class="skill-tag">EIS</span>
            <span class="skill-tag">XPS</span>
            <span class="skill-tag">SEM</span>
            <span class="skill-tag">Raman</span>
            <span class="skill-tag">NMR</span>
            <span class="skill-tag">FT-IR</span>
            <span class="skill-tag">AFM</span>
            <span class="skill-tag">BET</span>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="timeline-section tl-animate">
    <h3 class="timeline-heading"><i class="fa-solid fa-certificate"></i> Certifications</h3>
    <div class="timeline-card tl-animate">
      <span class="tl-date">2025</span>
      <div class="tl-title">Applying Machine Learning to Engineering and Science</div>
      <div class="tl-place">Massachusetts Institute of Technology</div>
    </div>
    <div class="timeline-card tl-animate">
      <span class="tl-date">2025</span>
      <div class="tl-title">Machine Learning, Modeling, and Simulation Principles</div>
      <div class="tl-place">Massachusetts Institute of Technology</div>
    </div>
  </div>

</div>

<script>
document.addEventListener('DOMContentLoaded', function () {
  var items = document.querySelectorAll('.tl-animate');
  var observer = new IntersectionObserver(function (entries) {
    entries.forEach(function (entry) {
      if (entry.isIntersecting) {
        var siblings = entry.target.parentElement.querySelectorAll('.tl-animate');
        var idx = Array.prototype.indexOf.call(siblings, entry.target);
        entry.target.style.transitionDelay = (idx * 0.08) + 's';
        entry.target.classList.add('tl-visible');
        observer.unobserve(entry.target);
      }
    });
  }, { threshold: 0.12, rootMargin: '0px 0px -20px 0px' });
  items.forEach(function (el) { observer.observe(el); });
});
</script>
