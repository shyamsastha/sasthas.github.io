---
layout: page
title: "Home"
class: home
---

# Hi, I'm Sastha Srinivas!

<div class="columns" markdown="1">

<div class="intro" markdown="1">
As a graduate researcher, pursuing a **Ph.D. in Computer Science** at the [IIIT-Delhi](https://iiitd.ac.in/), in the department of Computer Science at the [Melange Lab]([https://www.pushpendrasingh.info/](https://www.pushpendrasingh.info/team)) under the guidance of [Prof. Pushpendra Singh](https://www.pushpendrasingh.info/). I bring 3+ years of hands-on experience specializing in **AI/ML and IoT** through my prior work, graduate education, and internships. As a researcher, my focus has been on leveraging existing technologies and upcoming ML/AI technologies and tools to augment the lives and wellbeing of the aging population. 

Prior to this, I spent two years as a **Programmer Analyst** at Sara's Inc. and Unanu, spearheading cloud products and analytics dashboards that saved time and money for clients from various domains. My involvement was not limited but included cloud API deployment, testing, and maintenance, analytics dashboard design, and deployment, & working on producing ML/AI pipelines for production environments.

Preceding that, I was pursuing a **Master's degree in Computer Systems Engineering with a specialization in IoT** at the **College of Engineering** at [Northeastern University](https://catalog.northeastern.edu/graduate/engineering/multidisciplinary/cyber-physical-systems-ms/) (currently renamed as the **Master of Science in Cyber-Physical Systems with a concentration in the Internet of Things (IoT)**), under the guidance of [Prof.Peter O'Reilly](https://coe.northeastern.edu/people/oreilly-peter/). During my time at Northeastern, I was also the treassuer of the IoTConnect graduate club involved in the design and development of IoT systems and applications.

My work and passion involve utilizing concepts from multi-disciplinary fields to leverage upcoming technology for affective computing. My side projects include advancements in computer science education, including but not limited to improving teaching methods, analyzing the impact of AI on education, and more.

</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/DSC_0039.jpg' type='image/jpeg' />
  <img
    src='/images/DSC_0039.jpg'
    alt='Sastha Srinivasan'>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
</div>
</div>

## Featured Projects

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

## Featured Publications

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

<a href="{{ "/publications/" | relative_url }}" class="button">
  <i class="fas fa-chevron-circle-right"></i>
  Show All Publications
</a>

<div class="news-travel" markdown="1">

<div class="news" markdown="1">
## Latest News

<ul>
{% for news in site.data.news limit:10 %}
  {% include news.html news=news %}
{% endfor %}
</ul>

</div>

<div class="travel" markdown="1">
## Latest Travel

<table>
<tbody>
{% assign future_travel = site.data.travel | where_exp:'item','item.start == null' %}
{% for travel in future_travel %}
  {% include travel.html travel=travel %}
{% endfor %}
{% assign sorted_travel = site.data.travel | where_exp:'item','item.start' | sort: 'start' | reverse %}
{% for travel in sorted_travel limit:10 %}
  {% include travel.html travel=travel %}
{% endfor %}
</tbody>
</table>

</div>

</div> -->
