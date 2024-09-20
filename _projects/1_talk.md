---
layout: page
title: "Upcoming Event -Stay Tuned"
description: A description of the talk
img: assets/img/12.jpg
importance: 1
category: next
start: 2023-09-26 16:00:00 +01:00
end: 2023-09-26 17:00:00 +01:00
timezone: Europe/London
location: "https://meet.google.com/your-meeting-link"  # Replace with your actual Google Meet link
related_publications: true
---



We are reaching out the next speakers for the upcoming event. Stay tuned for more information.


{% assign event_title = page.title | url_encode %}
{% assign event_details = page.description | url_encode %}
{% assign event_location = page.location | url_encode %}
{% assign start_datetime = page.start | date: "%Y%m%dT%H%M%S" %}
{% assign end_datetime = page.end | date: "%Y%m%dT%H%M%S" %}
{% assign timezone = page.timezone | url_encode %}


<a href="https://calendar.google.com/calendar/render?action=TEMPLATE&text={{ event_title }}&dates={{ start_datetime }}/{{ end_datetime }}&details={{ event_details }}&location={{ event_location }}&ctz={{ timezone }}" target="_blank" class="btn btn-primary">Add to Google Calendar</a>

<a href="{{ page.url | append: 'event.ics' }}" class="btn btn-secondary">Download .ics File</a>
