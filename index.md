---
layout: page
title: "Home"
class: home
---
<body style=""><path>
    <canvas id="canvas" resize="" width="100%" height="100%" style="position: absolute; top: 0; opacity: 0.5"></canvas>
# Hi, I'm Yanna Lin

<div class="columns" markdown="1">

<div class="intro" markdown="1">

I’m now a second-year PhD student in Department of Computer Science and Engineering at the Hong Kong University of Science and Technology, under the supervision of Prof. [Huamin Qu](http://www.huamin.org). 

Before joining HKUST, I received a Bachelor’s Degree in the Software Engineering, Sun Yat-sen University in 2019. And my research interests are data analytics and data visualization.

</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/lala.jpg' type='image/webp' />
  <img
    src='/images/lala.jpg'
    alt='Yanna Lin'>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
<!-- * NSH 2602B -->
</div>

</div>
<!-- 
During my first year at UW, I received support from the [Fulbright program](https://en.wikipedia.org/wiki/Fulbright_Program). In 2013, I received my B.S. from [Hasso Plattner Institute](https://hpi.de/). I am a scholar of the [German National Academic Foundation](http://www.studienstiftung.de/). I have worked with the [Open Knowledge Foundation](http://www.okfn.org), [Google Research](https://ai.google/research/), and [Microsoft Research](https://www.microsoft.com/en-us/research/group/vibe/). Details are in my [CV]({{ "/cv/" | relative_url }}). -->

<!-- ## Featured Projects

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
</a> -->

<!-- ## Featured Publications -->

## Publications 

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

<div class="news-travel" markdown="1">

<div class="news" markdown="1">
## Latest News

<ul>
{% for news in site.data.news limit:10 %}
  {% include news.html news=nelows %}
{% endfor %}
</ul>

</div>

<!-- <div class="travel" markdown="1">
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

</div> -->

</div>


    <!-- JS Begins -->
    <script src="lib/jquery.min.js"></script>
    <script src="lib/paper.js"></script>
    <script src="jelly.js"></script>
    <script src="tentacle.js"></script>
    <script src="main.js"></script>
    <!-- JS Ends -->
  </path>

</body>
