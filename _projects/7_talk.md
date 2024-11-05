---
layout: page
title: "Modeling single-cell state and dynamics - Prof. Dr. Fabian J. Theis"
description: "<a href='https://forms.office.com/Pages/ResponsePage.aspx?id=p_SVQ1XklU-Knx-672OE-fR6PcyyBV1JuragBENwKPJURU9FMTVWUTA3Q0VERTNVMUU2TFpBTzBaRyQlQCN0PWcu' target='_blank'>Subscribe</a> to our seminar series for Zoom meeting passwords."
img: 
importance: 7
category: upcoming
start: 2025-05-28 16:00:00 +00:00
end: 2025-05-28 17:00:00 +00:00
timezone: Europe/London
location: "https://ucl.zoom.us/w/93006386340?tk=Gi-cdRAUS_EFUMh2Sjx22ixq1IHMSKPyaxFAdzXkZ4k.DQcAAAAVp5zUpBpmYWtlREluWVEyTGpSb3VZOG52YWFPVFJzZwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"  # Replace with your actual Google Meet link
related_publications: false
---

We are pleased to confirm that [Prof. Dr. Fabian J. Theis](https://www.professoren.tum.de/en/theis-fabian) will be presenting at our next seminar on **Wednesday, April 30th**. **Title and abstract to be announced shortly**.

#### Abstract:

Single-cell technologies are revolutionizing our understanding of cellular dynamics across biological processes, with exciting impact in our understanding of cell decisions for example in development. However, analyzing and interpreting these data poses computational and conceptual challenges, in particular with recent developments regarding spatio-temporal profiling. Here, I will discuss AI-based approaches for studying single-cell dynamics and fate decisions across molecular modalities, time, and space, and under perturbations such as drugs of CRISPR knockouts. I will finish with an outlook towards generative AI and foundation models and their potential impact in single cell genomics.

<div style="margin-top: 35px;"></div>

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
