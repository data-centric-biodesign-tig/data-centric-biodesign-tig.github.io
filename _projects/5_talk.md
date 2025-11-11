---
layout: page
title: Maximization of production in cell-free systems using active learning - Dr. Olivier Borkowski
description: "<a href='https://docs.google.com/forms/d/e/1FAIpQLSd8ONmtPX5Gu8PwKy3-LBgbkOJ_q7kej85OLBMtgwQhniw7YQ/viewform?usp=dialog' target='_blank'>Subscribe</a> to our seminar series for Zoom meeting passwords."
img: 
importance: 5
category: past
start: 2025-03-26 16:00:00 +00:00
end: 2025-03-26 17:00:00 +00:00
timezone: Europe/London
location: "https://ucl.zoom.us/w/93006386340?tk=Gi-cdRAUS_EFUMh2Sjx22ixq1IHMSKPyaxFAdzXkZ4k.DQcAAAAVp5zUpBpmYWtlREluWVEyTGpSb3VZOG52YWFPVFJzZwAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA"  # Replace with your actual Google Meet link
related_publications: false
---

We are pleased to confirm that [Dr. Olivier Borkowski](https://sites.google.com/view/olivierborkowski) will be presenting on **Wednesday, March 26th**. 
#### Title: **Maximization of production in cell-free systems using active learning**
#### Abstract:

Cell-free lysate-based systems are widely used for gene expression studies, genetic circuit design and even phage production. Here we demonstrate how active learning can be used to explore large combinatorial spaces of over millions of cell-free buffer compositions, maximizing mRNA expression and protein production. Our approach optimized mRNA and protein yields while uncovering the key factors influencing cell-free productivity. Our results reveal distinct determinants for transcription and translation, with evidence suggesting competition between the two processes. Maximizing protein production is crucial for biomanufacturing applications, while improving mRNA yield makes cell-free systems a powerful platform for transcriptome analysis. Unlike in vivo approaches, cell-free systems offer an adaptable and open environment, allowing precise control of intracellular conditions. This flexibility enables a better understanding of molecular mechanisms, high-throughput screening of regulatory elements and streamlined automation.

<div style="margin-top: 35px;"></div>


<div style="text-align: center; margin-top: 20px;">
  <iframe width="560" height="315" src="https://www.youtube.com/embed/FY9QuIF8fvc?si=329pVtjwKCaIfTb2" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
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
