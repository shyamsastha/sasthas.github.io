---
layout: page
title: "Home"
class: home
---

# Hi, I'm Sargun!

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I am a Software Developer (Research) at [Mphasis Lab, Ashoka University](https://ashoka.edu.in/ML2CT), working with [Dr. Gautam Menon](https://ashoka.edu.in/faculty#!/gautam-i-menon-1526) and
[Dr. Debayan Gupta](https://ashoka.edu.in/faculty#!/debayan-gupta-1157) on modelling social contact in cohort studies. I am also working as a research volunteer at [TavLab, IIIT-Delhi](http://tavlab.iiitd.edu.in/) under [Dr. Tavpritesh Sethi](https://www.iiitd.ac.in/tavpritesh) on exciting problems at the intersection of NLP and Genomics. 

Prior to joining Ashoka, I worked as a Software Engineer - Data Science at [Fidelity Center for Applied Technology (FCAT), Fidelity Investments](https://fcatalyst.com/overview) for two years. In this role I was involved in a diverse set of projects in NLP, Machine Learning and Software development, including Information Extraction from unstructured documents, Abstractive and Extractive text summarization, OCR and Image Processing, Email Fraud Surveillance system, Explainable AI, Recommender Systems and more.

I graduated from [Birla Institute of Technology and Science (BITS), Pilani](https://www.bits-pilani.ac.in/
) in 2019, with a Bachelors in Mechanical Engineering. I found myself being drawn to courses in Applied Statistics, which further led to my interest in Data Science.

</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/sargun_nagpal.webp' type='image/webp' />
  <img
    src='/images/sargun_nagpal.jpg'
    alt='Sargun Nagpal'>
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

<!-- <div class="news-travel" markdown="1">

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
