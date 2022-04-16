---
layout: page
title: "Home"
class: home
---
<body style=""><path>



<div class="columns" markdown="1">

# Hi, I'm Yanna Lin

</div>

<div class="columns" markdown="1">

<div class="intro" markdown="1">

I’m now a second-year Ph.D. candidate in Department of Computer Science and Engineering at the Hong Kong University of Science and Technology, under the supervision of Prof. [Huamin Qu](http://www.huamin.org). 

Before joining HKUST, I received a Bachelor’s Degree in the Software Engineering, Sun Yat-sen University in 2019. And my research interests are data analytics and data visualization.

</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/lala1.jpeg' type='image/webp' />
  <img
    src='/images/lala1.jpeg'
    alt='Yanna Lin'>
</picture>

{:.no-list}
* <a href="mailto:{{ site.email }}">{{ site.email }}</a>
<!-- * NSH 2602B -->
</div>

</div>

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

<div class="columns" markdown="1">
## Publications 
</div>
{% assign pubyears = site.publications | group_by:"year"  %}
{% assign sorted_pubyears = pubyears | reverse %}
{% for year in sorted_pubyears %}
 <h2 class="publicationyear" href="#y{{ year.name }}"><span> {{ year.name }} </span> </h2>
{% for pub in year.items %}
  {% include publication.html pub=pub %}
{% endfor %}
{% endfor %}

<script>
  {% include itemsjs.min.js %}
  {% include pubfilter.js %}
</script>


<div class="news-travel" markdown="1">

<div class="news" markdown="1">
## Latest News

<ul class="scroll-bar">
{% for news in site.data.news limit:10 %}
  {% include news.html news=nelows %}
{% endfor %}
</ul>

</div>

<div class="award" markdown="1">
## Awards

  <ul class="scroll-bar">
    {% assign future_award = site.data.awards | where_exp:'item','item.start == null' %}
    {% for award in future_award %}
      {% include award.html award=award %}
    {% endfor %}
  </ul>

</div>

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
