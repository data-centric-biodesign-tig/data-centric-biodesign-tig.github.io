---
layout: page
title: Causality-inspired generative modelling for single-cell genomics - Dr. Hananeh Aliee
description: "<a href='https://ucl.zoom.us/webinar/register/WN_ADbaTtOiRuu1oeFMFQR7sQ' target='_blank'>Subscribe</a> to our seminar series for Zoom meeting passwords."
img: 
importance: 3
category: past
start: 2025-01-29 16:00:00 +00:00
end: 2025-01-29 17:00:00 +00:00
timezone: Europe/London
location: "https://ucl.zoom.us/w/93006386340?tk=Gi-cdRAUS_EFUMh2Sjx22ixq1IHMSKPyaxFAdzXkZ4k.DQcAAAAVp5zUpBpmYWtlREluWVEyTGpSb3VZOG52YWFPVFJzZwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"  # Replace with your actual Google Meet link
related_publications: false
---

We are pleased to confirm that [Dr. Hananeh Aliee](https://scholar.google.de/citations?user=g44oSnYAAAAJ&hl=en) will be presenting on **Wednesday, January 29th**. 
#### Title: **Causality-inspired generative modelling for single-cell genomics**
##### Abstract: 
Single-cell genomics provides a uniquely powerful opportunity to study cells and the intricate molecular mechanisms that drive their remarkable diversity within tissues. This revolutionary technology allows us to understand how cells make decisions and undergo changes during development or disease progression. However, a vast uncharted hypothesis space remains, such as understanding cellular responses to combinations of perturbations, which cannot be fully explored experimentally within a reasonable timeframe. The ability to study how these changes vary across diverse donors is particularly important for addressing the full spectrum of human biology and advancing more personalized and inclusive healthcare solutions. 

In this talk, I will present my latest research on generative modelling and causal machine learning tailored to these challenges. I have developed several AI-based methods to model cellular dynamics and uncover their underlying mechanisms. These include methods for determining gene regulatory networks (GRNs) using neural ordinary-differential equations to infer structural causal equations governing genes and employing causal generative models to infer conditional cell distributions from single-cell transcriptomics data. The latter approach eliminates spurious correlations while retaining key biological signals, making it particularly valuable for large-scale atlasing efforts to stratify donors across diverse diseases and biological factors.

After discussing these methods, I will highlight how I have applied them to create comprehensive atlases, uncovering transcriptomic diversity across organs and diseases.


<div style="margin-top: 35px;"></div>


<div style="text-align: center; margin-top: 20px;">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/JJZW34oWdSQ?si=KZ2482Wwtr0rlI1E" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
