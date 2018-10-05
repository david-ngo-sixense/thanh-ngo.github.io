---
layout: default
title: Home
navigation_weight: 1
---

<div class="intro">

![David Tran-Thanh NGO](assets/david-ngo.jpg){:#mypicture}

<div>

[Mathematical Sciences Institute](http://maths.anu.edu.au/)  
The Australian National University  
Canberra, ACT, 2601, Australia


**Email:** `tran-thanh.ngo` at `cea` dot `fr`   
**Phone:** +33 6 52 55 87 46

</div>

</div>

### Background
Since 2016, I have been an Eurofusion engineering fellow with the [CEA Cadarache/Institut de Recherche sur la Fusion Magnétique] (http://irfm.cea.fr/), Saint-Paul-les Durance, France, 
where I am in charge of the conception and development of a software platform for the exploitation of imaging diagnostics in nuclear fusion devices (WEST tokamak of the CEA/Cadarache and Wendelstein 7-X stellarator of IPP Greifswald) . 

I finished my PhD at [university of Strasbourg] (https://www.unistra.fr/) in 2015, where I developed the novel algorithms to detect shadows, vegetation and buildings from optical and satellite images (my PhD thesis can be found [here] (assets/PhD_TranNgo.pdf)). 

Before, I graduated from the French Graduate Engineering School [IMT Atlantique] (https://www.imt-atlantique.fr/fr) (ex-Télécom Bretagne, Brest) in 2012 where I studied computer science and signal processing. I hold a master in Image processing from Université de Rennes 1 and Télécom Bretagne.
  [research page](/research), and my CV is available [here](assets/CV_Ngo_en.pdf).

### Teaching
For a link:  [MATH 1113](https://programsandcourses.anu.edu.au/course/math1113). 
To  [teaching page](teaching/).

### Current and upcoming activities
Older activities are listed on my [activities page](activities/).

{% capture currenttime %}{{ site.time }}{% endcapture %}
{% assign activities = site.data.activities | where_exp: "activity", "activity.date > currenttime" | sort: 'date' %}
<ul>
{% for activity in activities %}
<li>
{% unless activity.current == true %}
<strong>{% if activity.display-date %}{{ activity.display-date | markdownify | strip | remove: '<p>' | remove: '</p>' }}{% else %}{{ activity.date | date: "%b %Y" }}{% endif %}:</strong>
{% endunless %}
{{ activity.content | markdownify | strip | remove: '<p>' | remove: '</p>'}}{% if activity.location %}, {{ activity.location | remove: '<p>' | remove: '</p>'}}{% endif %}
</li>
{% endfor %}
</ul>



