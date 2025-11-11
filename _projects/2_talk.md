---
layout: page
title: Gaussian Graphical Models for Multi-Omics Analysis with GmGM - Dr. Luisa Cutillo
description: "<a href='https://docs.google.com/forms/d/e/1FAIpQLSd8ONmtPX5Gu8PwKy3-LBgbkOJ_q7kej85OLBMtgwQhniw7YQ/viewform?usp=dialog' target='_blank'>Subscribe</a> to our seminar series for Zoom meeting passwords."
img: 
importance: 1
category: past
start: 2024-12-03 16:00:00 +00:00
end: 2024-12-03 17:00:00 +00:00
timezone: Europe/London
location: "https://ucl.zoom.us/w/93006386340?tk=Gi-cdRAUS_EFUMh2Sjx22ixq1IHMSKPyaxFAdzXkZ4k.DQcAAAAVp5zUpBpmYWtlREluWVEyTGpSb3VZOG52YWFPVFJzZwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"
related_publications: false
---

We are pleased to confirm that [Dr. Luisa Cutillo](https://eps.leeds.ac.uk/maths/staff/5526/dr-luisa-cutillo) will be presenting on **Tuesday, December 3rd**.

##### Title: “Gaussian Graphical Models for Multi-Omics Analysis with GmGM”
##### Abstract: 
This seminar will explore the use of Gaussian Graphical Models (GGM) in multi-omics data analysis, showcasing GmGM, a new framework that leverages graph theory to model and infer complex biological relationships across multiple data types. Dr. Cutillo will discuss how this approach enhances data integration and supports novel biological discoveries.


<div style="margin-top: 35px;"></div>

<div style="text-align: center; margin-top: 20px;">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/g882WnQnUgk?si=cwnGy-jrXEKqoNmQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

<!-- Meeting Link Button -->
<a href="{{ page.location }}" target="_blank" class="btn btn-primary">Join the Meeting</a>

<!-- Calendar Buttons -->
{% assign event_title = page.title | url_encode %}
{% assign event_details = page.description | url_encode %}
{% assign event_location = page.location | url_encode %}
{% assign start_datetime = page.start | date: "%Y%m%dT%H%M%S" %}
{% assign end_datetime = page.end | date: "%Y%m%dT%H%M%S" %}
{% assign timezone = page.timezone | url_encode %}

<a href="https://calendar.google.com/calendar/render?action=TEMPLATE&text={{ event_title }}&dates={{ start_datetime }}/{{ end_datetime }}&details={{ event_details }}&location={{ event_location }}&ctz={{ timezone }}" target="_blank" class="btn btn-primary">Add to Google Calendar</a>

<!-- Capture .ics Content -->
{% capture ics_content %}
BEGIN:VCALENDAR
VERSION:2.0
PRODID:-//Data-Centric Biodesign TIG//NONSGML v1.0//EN
BEGIN:VEVENT
SUMMARY:{{ page.title }}
UID:{{ page.url }}
DTSTAMP:{{ 'now' | date: "%Y%m%dT%H%M%SZ" }}
DTSTART;TZID={{ page.timezone }}:{{ page.start | date: "%Y%m%dT%H%M%S" }}
DTEND;TZID={{ page.timezone }}:{{ page.end | date: "%Y%m%dT%H%M%S" }}
DESCRIPTION:{{ page.description }}
LOCATION:{{ page.location }}
END:VEVENT
END:VCALENDAR
{% endcapture %}

<!-- Download .ics File Button -->
<button class="btn btn-secondary" onclick="downloadICS()">Download .ics File</button>

<!-- JavaScript Function -->
<script>
  function downloadICS() {
    var icsContent = {{ ics_content | jsonify }};
    var blob = new Blob([icsContent], { type: 'text/calendar;charset=utf-8' });
    var link = document.createElement('a');
    link.href = URL.createObjectURL(blob);
    link.download = 'event.ics';
    document.body.appendChild(link);
    link.click();
    document.body.removeChild(link);
  }
</script>
