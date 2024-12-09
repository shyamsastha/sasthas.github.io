---
layout: page
title: "Home"
class: home
---

# Hi, I'm Sastha Srinivas!

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I am a graduate researcher, pursuing a **Ph.D. in Computer Science** at the [IIIT-Delhi](https://iiitd.ac.in/), in the department of Computer Science at the [Melange Lab]([https://www.pushpendrasingh.info/](https://www.pushpendrasingh.info/team)) under the guidance of [Prof. Pushpendra Singh](https://www.pushpendrasingh.info/) and [Prof. Mohan Kumar](https://www.rit.edu/directory/mjkvcs-mohan-kumar). With 3+ years of hands-on experience, my research focuses on leveraging **AI/ML** with **sensing** to create social impact in the mental health domain. 

Before diving into research, I spent two years as a **Programmer Analyst** at Sara’s Inc. and Unanu, leading cloud products, analytics dashboards, and ML/AI pipeline deployments that saved time and money across industries.

I hold a Master's in **Computer Systems Engineering (specializing in IoT)** from [Northeastern University](https://catalog.northeastern.edu/graduate/engineering/multidisciplinary/cyber-physical-systems-ms/) under the guidance of [Prof.Peter O'Reilly](https://coe.northeastern.edu/people/oreilly-peter/), where I also interned at **Bose Corporation**, developing an automated testing suite for smart home security. I was also Treasurer of the IoTConnect graduate club, promoting IoT innovation among students.

Passionate about affective computing, I work on projects that intersect AI with education, and in my downtime, you’ll find me enjoying strategy games, tabletop RPGs, or reading with cocoa in hand when I do not explore the world.

</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/DSC_0039_cropped.jpg' type='image/jpeg' />
  <img
    src='/images/DSC_0039_cropped.jpg'
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
