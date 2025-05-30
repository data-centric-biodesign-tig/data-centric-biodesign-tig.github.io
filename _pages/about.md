---
layout: about
title: 
permalink: /
subtitle: How can AI support the practical engineering of biology to tackle global challenges? #<a href='#'>Affiliations</a>. Address. Contacts. Motto. Etc.

# profile:
#   align: right
#   image: turing_logo.jpg
#   image_circular: false # crops the image to make it circular
#   more_info: >
#     <p><a href="https://www.turing.ac.uk/">The Alan Turing Institute</a></p>
#     <p>British Library, 96 Euston Rd., London NW1 2DB</p>
#     <p>+44 020 3862 3352</p>
    
nav: true
news: false # includes a list of news items
selected_papers: false # includes a list of papers marked as "selected={true}"
social: false # includes social icons at the bottom of the page
---

## About Us

We are a Turing Interest Group dedicated to leveraging artificial intelligence to advance the engineering of biological systems. Our mission is to address global challenges such as sustainable manufacturing, healthcare innovation, and environmental impact. By uniting experts from fields like computer science, biology, and engineering, we aim to develop data-driven approaches that enable the practical reprogramming of biological systems.

For more details on our aims, research areas, and how to get involved, please visit our [official website](https://www.turing.ac.uk/research/interest-groups/data-centric-biological-design-and-engineering).

To explore the specific topics we cover, please visit our [Topics page](/topics/).

## Get Involved

<p>Join us for our next webinar in the series:</p>
<div style="font-size: 30px;">
  <a href="https://ucl.zoom.us/webinar/register/WN_ADbaTtOiRuu1oeFMFQR7sQ">Click here to register and join</a>
</div>

<div style="margin-bottom: 25px;"></div> 

## Upcoming Event

<div style="margin-top: 15px;"></div> 

{% assign next_projects = site.projects | where: "category", "next" | sort: "importance" %}

{% if next_projects.size > 0 %}
  {% assign next_event = next_projects[0] %}
  <div class="container">
    <div class="row row-cols-1 row-cols-md-1">
      {% include projects_horizontal.liquid project=next_event %}
    </div>
  </div>
{% else %}
  <p>No upcoming events. We are planning our 2025/2026 seminars. Please keep an eye on our website.</p>
{% endif %}


To **view all of our events**, including past, current, and upcoming, please visit our [Events page](/events/).


<!--
#### Subscribe to Our Seminar Series

<p>Never miss an event! Subscribe to our seminar series calendar to receive automatic updates, or add our events to your personal calendar:</p>


<a href="https://calendar.google.com/calendar/u/1?cid=ZGNiLnR1cmluZ0BnbWFpbC5jb20" target="_blank" class="btn btn-primary">Subscribe via Google Calendar</a>
<a href="https://calendar.google.com/calendar/ical/dcb.turing%40gmail.com/public/basic.ics" target="_blank" class="btn btn-success">Add to iCal or Outlook (.ics)</a>

<p>By subscribing, any new events we add will automatically appear in your calendar.</p>
-->

## Contact Us

Pedro Fontanarrosa: <a href="mailto:p.fontanarrosa@ucl.ac.uk">p.fontanarrosa@ucl.ac.uk</a>  
Yuxin Shen: <a href="mailto:y.shen-80@sms.ed.ac.uk">y.shen-80@sms.ed.ac.uk</a>

For more information about our organisers, please visit our [Organisers page](/organisers/).
