---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
# all events
{% ical url: https://calendar.google.com/calendar/ical/64dbc9200e64d520220ae7169fbe8b43dc149b3b17eef6de8cdc7ee1505a8f12%40group.calendar.google.com/public/basic.ics limit: 10  %}
# {{ event.summary }}
## {{ event.start_time | date: '%A %B %d %Y' America/New_York }}
### {{ event.start_time | date: '%-I:%M %P' America/New_York }} - {{ event.end_time | date: '%-I:%M %P' America/New_York }}
    {{ event.description }}
    {% endical %}

---

# future events
{% ical url: https://calendar.google.com/calendar/ical/64dbc9200e64d520220ae7169fbe8b43dc149b3b17eef6de8cdc7ee1505a8f12%40group.calendar.google.com/public/basic.ics limit: 10 only_future: true %}
# {{ event.summary }}
## {{ event.start_time | date: '%A %B %d %Y' America/New_York }}
### {{ event.start_time | date: '%-I:%M %P' America/New_York }} - {{ event.end_time | date: '%-I:%M %P' America/New_York }}
    {{ event.description }}

    {% endical %}
