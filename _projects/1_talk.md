---
layout: page
title: Next-Generation Lead clone selection for Cell Line Development through AI and ML - Dr. Stephen Goldrick
description: "<a href='https://forms.office.com/Pages/ResponsePage.aspx?id=p_SVQ1XklU-Knx-672OE-fR6PcyyBV1JuragBENwKPJURU9FMTVWUTA3Q0VERTNVMUU2TFpBTzBaRyQlQCN0PWcu' target='_blank'>Subscribe</a> to our seminar series for Zoom meeting passwords."
img: 
importance: 1
category: next
start: 2024-10-30 16:00:00 +00:00
end: 2024-10-30 17:00:00 +00:00
timezone: Europe/London
location: "https://ucl.zoom.us/j/94449097755?pwd=Ocuu1djZ5gQ7wZaxoa3aQlooaU9CAH.1"  # Replace with your actual Google Meet link
related_publications: false
---

[Dr. Stephen Goldrick](https://profiles.ucl.ac.uk/46716-stephen-goldrick) will present his research on "Next-Generation Lead clone selection for Cell Line Development through AI and ML".

#### Abstract:

This research outlines the development of a data-driven methodology to enhance lead clone selection that not only considers the available titre concentration and product quality information but also leverages the significant untapped data resource containing all the available off-line, on-line and metadata. To help automate this selection process the research outlines the use of a simple natural-language-generation (NLG) algorithm to evaluate all available information which summarises and contextualises the large volume of information into a human-readable report. This automatically generated report outlines the key metrics and correlations to assist the scientists and engineers during their lead clone selection.

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
PRODID:-//Your Organization//NONSGML v1.0//EN
BEGIN:VEVENT
UID:{{ page.url }}
DTSTAMP:{{ 'now' | date: "%Y%m%dT%H%M%SZ" }}
DTSTART;TZID={{ page.timezone }}:{{ page.start | date: "%Y%m%dT%H%M%S" }}
DTEND;TZID={{ page.timezone }}:{{ page.end | date: "%Y%m%dT%H%M%S" }}
SUMMARY:{{ page.title }}
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
