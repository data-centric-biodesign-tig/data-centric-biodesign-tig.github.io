---
layout: about
title: 
permalink: /
subtitle: How can AI support the practical engineering of biology to tackle global challenges? #<a href='#'>Affiliations</a>. Address. Contacts. Motto. Etc.

profile:
  align: right
  image: turing_logo.jpg
  image_circular: false # crops the image to make it circular
  more_info: >
    <p><a href="https://www.turing.ac.uk/">The Alan Turing Institute</a></p>
    <p>British Library, 96 Euston Rd., London NW1 2DB</p>
    <p>+44 020 3862 3352</p>
    
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

<div style="font-size: 20px;">
  <a href="https://forms.office.com/Pages/ResponsePage.aspx?id=p_SVQ1XklU-Knx-672OE-fR6PcyyBV1JuragBENwKPJURU9FMTVWUTA3Q0VERTNVMUU2TFpBTzBaRyQlQCN0PWcu">Click here to request sign-up and join</a>
</div>
<div style="margin-bottom: 15px;"></div> 

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
  <p>No upcoming events.</p>
{% endif %}


For all events, past and upcoming, please visit our [Events page](/events/).

#### Subscribe to Our Seminar Series

<p>Never miss an event! Subscribe to our entire seminar series:</p>

<a href="https://calendar.google.com/calendar/u/0?cid=NTRmNzc4YjM3MDhjNWU5NmIyNjgwMzVkNDA0M2UzM2RiMzEwMGZhNTFmODUzYmQxOWM1YTM2OWVlNjM1NzQ2NkBncm91cC5jYWxlbmRhci5nb29nbGUuY29t" target="_blank" class="btn btn-primary">Subscribe to Google Calendar</a>
<a href="https://calendar.google.com/calendar/ical/54f778b3708c5e96b268035d4043e33db3100fa51f853bd19c5a369ee6357466%40group.calendar.google.com/public/basic.ics" target="_blank" class="btn btn-success">Add to via iCal or Outlook (.ics)</a>



## Contact Us

Pedro Fontanarrosa: <a href="mailto:p.fontanarrosa@ucl.ac.uk">p.fontanarrosa@ucl.ac.uk</a>  
Yuxin Shen: <a href="mailto:y.shen-80@sms.ed.ac.uk">y.shen-80@sms.ed.ac.uk</a>

For more information about our organizers, please visit our [Organisers page](/organisers/).
