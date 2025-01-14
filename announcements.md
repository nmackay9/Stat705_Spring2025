---
layout: page
title: Announcements
nav_exclude: true
description: A feed containing all of the class announcements.
nav_order: 4
---

# Announcements

{% assign announcements = site.announcements | reverse %}
{% for announcement in announcements %}
{{ announcement }}
{% endfor %}
