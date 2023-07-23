---
title: "About"
layout: gridlay
sitemap: false
permalink: /about/
---

## About 

{% for member in site.data.pi %}
<div class="jumbotron">
<div class="row">
<div class="col-sm-3">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo1 }}" width="100%" style="max-width:320px"/>
</div>
<div class="col-sm-3">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo2 }}" width="100%" style="max-width:400px"/>
</div>
<div class="col-sm-6 col-xs-12">
  <h3>{{ member.name }}</h3>
  <h4><i>{{ member.info }}</i></h4>
  {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-3x"></i></a> {% endif %}
  {% if member.cv %} <a href="{{ site.url }}{{ site.baseurl }}/{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-3x"></i></a> {% endif %}
  {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-3x"></i></a> {% endif %}
  {% if member.researchgate %} <a href="{{ member.researchgate }}" target="_blank"><i class="ai ai-researchgate-square ai-3x"></i></a> {% endif %}
  {% if member.orcid %} <a href="{{ member.orcid }}" target="_blank"><i class="ai ai-orcid-square ai-3x"></i></a> {% endif %}
  <!--{% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-3x"></i></a> {% endif %}-->
  

  <!-- <ul style="overflow: hidden"> -->
**Place | Date of Birth**: Kerala, India | 11 March 1992
 <!-- </ul> -->
</div>
</div>
</div>
{% endfor %}


<div class="jumbotron">
<div class="row">
{% for member in site.data.pi %}
<div class="col-sm-6"> 
### Education
<ul> <!-- style="overflow: hidden"> -->
{% if member.number_educ == 1 %}
<li> {{ member.education1 | replace: "-","&#8211;"}} </li>
{% endif %}
{% if member.number_educ == 2 %}
<li> {{ member.education1 | replace: "-","&#8211;"}} </li>
<li> {{ member.education2 | replace: "-","&#8211;"}} </li>
{% endif %}
{% if member.number_educ == 3 %}
<li> {{ member.education1 | replace: "-","&#8211;"}} </li>
<li> {{ member.education2 | replace: "-","&#8211;"}} </li>
<li> {{ member.education3 | replace: "-","&#8211;"}} </li>
{% endif %}
{% if member.number_educ == 4 %}
<li> {{ member.education1 | replace: "-","&#8211;"}} </li>
<li> {{ member.education2 | replace: "-","&#8211;"}} </li>
<li> {{ member.education3 | replace: "-","&#8211;"}} </li>
<li> {{ member.education4 | replace: "-","&#8211;"}} </li>
{% endif %}
{% if member.number_educ == 5 %}
<li> {{ member.education1 | replace: "-","&#8211;"}} </li>
<li> {{ member.education2 | replace: "-","&#8211;"}} </li>
<li> {{ member.education3 | replace: "-","&#8211;"}} </li>
<li> {{ member.education4 | replace: "-","&#8211;"}} </li>
<li> {{ member.education5 | replace: "-","&#8211;"}} </li>
{% endif %}
{% if member.number_educ == 6 %}
<li> {{ member.education1 | replace: "-","&#8211;"}} </li>
<li> {{ member.education2 | replace: "-","&#8211;"}} </li>
<li> {{ member.education3 | replace: "-","&#8211;"}} </li>
<li> {{ member.education4 | replace: "-","&#8211;"}} </li>
<li> {{ member.education5 | replace: "-","&#8211;"}} </li>
<li> {{ member.education6 | replace: "-","&#8211;"}} </li>
{% endif %}
</ul>
</div>
{% endfor %}

{% if site.data.awards %}
<div class="col-sm-6">
### Awards
<ul>
{% for award in site.data.awards %}
 <li> {{ award.name | replace: "-","&#8211;"}} </li>
{% endfor %}
</ul>
</div>
{% endif %}
</div>
</div>

<div class="jumbotron">
<div class="row">
{% if site.data.interests %}
<div class="col-sm-6">
### Interests and Extracurricular activities
<ul>
{% for interest in site.data.interests %}
 <li> {{ interest.name | replace: "-","&#8211;"}} </li>
{% endfor %}
</ul>
<div class="container">
<div class="row">
<center>
<img src="{{ site.url }}{{ site.baseurl }}/images/mrudangam.jpg" width="60%"/><br/>
Jugalbandi perfomance at PRL Ramanathan Auditorium. <br/>
</center>
</div>
</div>
<br/>
</div>
{% endif %}

{% if site.data.skills %}
<div class="col-sm-6">
### Technical skills
<ul>
{% for skill in site.data.skills %}
 <li> {{ skill.name | replace: "-","&#8211;"}} </li>
{% endfor %}
</ul>
<div class="container">
<div class="row">
<center>
<img src="{{ site.url }}{{ site.baseurl }}/images/stars.jpg" width="60%"/><br/>
Under the blanket of stars at Mt. Abu observatory. <br/>
</center>
</div>
</div>
<br/>
</div>
{% endif %}
</div>
</div>
