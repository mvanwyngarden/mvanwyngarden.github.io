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
<div class="col-sm-4">
  <img src="{{ site.url }}{{ site.baseurl }}/images/{{ member.photo }}" width="100%" style="max-width:250px"/>
</div>
<div class="col-sm-8 col-xs-12">
  <h3>{{ member.name }}</h3>
  <h4><i>{{ member.info }}</i></h4>
  {% if member.email %}<a href="mailto:{{ member.email }}" target="_blank"><i class="fa fa-envelope-square fa-3x"></i></a> {% endif %}
  {% if member.cv %} <a href="{{ site.url }}{{ site.baseurl }}/{{ member.cv }}" target="_blank"><i class="ai ai-cv-square ai-3x"></i></a> {% endif %}
  {% if member.github %} <a href="{{ member.github }}" target="_blank"><i class="fa fa-github-square fa-3x"></i></a> {% endif %}
  {% if member.scholar %} <a href="{{ member.scholar }}" target="_blank"><i class="ai ai-google-scholar-square ai-3x"></i></a> {% endif %}
  {% if member.researchgate %} <a href="{{ member.researchgate }}" target="_blank"><i class="ai ai-researchgate-square ai-3x"></i></a> {% endif %}

  <ul style="overflow: hidden">
    {% for education in member.education %}
      <li>{{ education | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>

</div>
</div>
</div>
{% endfor %}

<div class="jumbotron">
<div class="row">
<img src="images/grad_photo.jpg" width="100%" style="max-width:250px"/>
<div class="col-md-12 col-sm-12">
<h4>A little bit more about me</h4>
Originally from Omaha, Nebraska (go big red!), I've wanted to be an astronomer since I was eight years old. I completed my undergrad at Boston University in Astronomy & Physics, doing every research project I could get my hands on. During my time at BU, I was also heavily involved in outreach and mentorship! As a sophomore, I reestablished the [BU Astronomical Society](https://www.bu.edu/astronomy/community/student-organizations/) with my Co-President. Adopting the slogan "Space for All," we introduced students across majors to astronomy through student research showcases, tours of the observatory, and packed stargazing nights. I also served as President of the BU Chapter of the Society of Women in Space Exploration and was a mentor in the Physics Department's peer mentorship program, [PRISM](https://sites.bu.edu/prism/). As I grow as a scientist, I am excited to expand my scientific outreach efforts and continue fostering inclusive spaces within the Astronomy community.
<br>
<br>
Outside of astrophysics, I love baking, seeking out new brunch restaurants, trying not to forget the French I learned in Geneva, and dancing (I'm currently learning salsa and bachata!). 
</div>
</div>
</div>


{% if site.data.awards %}

<div class="jumbotron">
  <h3>Awards</h3>
  <ul>
    {% for award in site.data.awards %}
      <li>{{ award.name | replace: "-","&#8211;" }}</li>
    {% endfor %}
  </ul>
</div>
{% endif %}

