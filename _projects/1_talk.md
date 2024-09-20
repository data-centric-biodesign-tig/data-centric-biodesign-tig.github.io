---
layout: page
title: "Upcoming Event - Stay Tuned"
description: "A description of the talk"
img: assets/img/12.jpg
importance: 1
category: next
start: 2023-09-26 16:00:00 +01:00
end: 2023-09-26 17:00:00 +01:00
timezone: Europe/London
location: "https://meet.google.com/your-meeting-link"  # Replace with your actual Google Meet link
related_publications: true
---

We are reaching out to the next speakers for the upcoming event. Stay tuned for more information.

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
