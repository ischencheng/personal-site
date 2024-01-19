---
layout: page
title: "Home"
class: home
---

# Hi, I'm Chen Cheng

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I'm a senior undergraduate at the [School of Information Science and Technology](https://sist.shanghaitech.edu.cn/) at [ShanghaiTech University](https://www.shanghaitech.edu.cn/) focusing on Human-AI Interaction (HAI). In Fall 2023, I was an exchange student at [University of California, Berkeley](https://www.berkeley.edu/). Previously, I designed and built interactive systems for visualization and analysis advised by [Quan Li](https://faculty.sist.shanghaitech.edu.cn/liquan/) at ShanghaiTech University, aiming to facilitate the perception and decision-making process involving a large amount of data. Currently, I am working on building a programming support tool for code comprehension, as advised by [Tianyi Zhang](https://tianyi-zhang.github.io/) at Purdue University.

Overall, my passion lies in the transformation of information among different counterparts, particularly in developing tools and systems that enhance communication both between AI agents and between human and AI agents.



</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/chencheng_berkeley.webp' type='image/webp' />
  <img
    src='/images/chencheng_berkeley.png'
    alt='Chen Cheng'>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
</div>

</div>

<div style="background-color: #f0f0ed; padding: 10px; border-radius: 10px;">
  I am seeking a Ph.D. position in HAI, starting from Fall 2024. Download my <a href="{{ "/assets/resume_cc-0115.pdf" | relative_url }}">[CV]</a> here.
</div>

## Research <a href="{{ "/projects/" | relative_url }}">Projects</a>

<div class="featured-projects">
  {% assign sorted_projects = site.data.projects | sort: 'highlight' %}
  {% for project in sorted_projects %}
    {% if project.highlight %}
      {% include project.html project=project %}
    {% endif %}
  {% endfor %}
</div>
<a href="{{ "/projects/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show More Projects
</a>

## Research <a href="{{ "/publications/" | relative_url }}">Publications</a>

<div class="featured-publications">
  {% assign sorted_publications = site.publications | sort: 'year' | reverse %}
  {% for pub in sorted_publications %}
    {% if pub.highlight %}
      <a href="{{ pub.pdf }}" class="publication">
        <strong>{{ pub.title }}</strong>
        <span class="authors">{% for author in pub.authors %}{{ author }}{% unless forloop.last %}, {% endunless %}{% endfor %}</span>.
        <i>{% if pub.venue %}{{ pub.venue }}, {% endif %}{{ pub.year }}</i>.
        {% for award in pub.awards %}<br/><span class="award"><i class="fas fa-{% if award == "Best Paper Award" %}trophy{% else %}award{% endif %}" aria-hidden="true"></i> {{ award }}</span>{% endfor %}
      </a>
    {% endif %}
  {% endfor %}
</div>

<!-- <a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a> -->

