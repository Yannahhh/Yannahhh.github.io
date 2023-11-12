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

I am now a fourth-year Ph.D. candidate at the Hong Kong University of Science and Technology, supervised by Prof. [Huamin Qu](http://www.huamin.org) in the [VisLab](http://vis.cse.ust.hk). 
I am awarded [Hong Kong PhD Fellowship Scheme](https://cerg1.ugc.edu.hk/hkpfs/index.html) and [HKUST RedBird Academic Excellence Award](https://fytgs.hkust.edu.hk/admissions/Admission-to-Hong-Kong-Campus/submitting-an-application/scholarships-and-fees).
Before joining HKUST, I received a Bachelor’s Degree in the Software Engineering, Sun Yat-sen University, ranked 1/447. 

My research interests are in data analytics, data visualisation, and human-AI collaboration, in particular enhancing and optimising workflows for exploratory data analysis.

</div>

<div class="me" markdown="1">
<picture>
  <source srcset='/images/lala3.0.jpg' type='image/webp' />
  <img
    src='/images/lala3.0.jpg'
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
