---
layout: page
title: "Home"
class: home
---

# Hi, I'm Sargun!

<div class="columns" markdown="1">

<div class="intro" markdown="1">
I am currently pursuing my **Master's in Data Science** at the [NYU Center for Data Science](https://cds.nyu.edu). I have **3+ years** of experience building data and machine learning pipelines. My amalgam of professional and research experience in varied fields - finance, public health, cybersecurity, energy, and manufacturing has deeply ingrained in me a sense of applying data science across multiple disciplines.

In the past, I worked as a **Software Engineer - Data Science** for 2 years at [Fidelity Investments](https://fcatalyst.com/overview), where I contributed to projects in **NLP, Machine Learning and Software development**, including Information Extraction, Abstractive and Extractive text summarization, OCR and Image Processing, Email Fraud Surveillance, Explainable AI and more.

I also have over 1 year of research experience in the area of **ML for social good**. As a **Research Scientist** at [ML2CT Lab, Ashoka University](https://ashoka.edu.in/ML2CT), I worked on the statistical modelling of contact mixing patterns to devise interventions to limit the spread of infectious diseases. At [TavLab, IIIT-Delhi](http://tavlab.iiitd.edu.in/), I used Machine Learning to build predictive models for COVID-19 caseload predicion and surveillance of emerging variants.

</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/sargun-nagpal.jpeg' type='image/jpeg' />
  <img
    src='/images/sargun-nagpal.jpeg'
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
