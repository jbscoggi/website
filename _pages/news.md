---
layout: page
permalink: /news/
title: News Archive
include_in_header: False
description: All news from the beginning of time...
---
<div class="news">
  {% if site.news  %}
    <table>
    {% assign news = site.news | reverse %}
    {% for item in news %}
      <tr>
        <td class="date">{{ item.date | date: "%b %-d, %Y" }}</td>
        <td class="announcement">
          {% if item.inline %}
            {{ item.content | remove: '<p>' | remove: '</p>' | emojify }}
          {% else %}
            <a class="news-title" href="{{ item.url | prepend: site.baseurl }}">{{ item.title }}</a>
          {% endif %}
        </td>
      </tr>
    {% endfor %}
    </table>
  {% else %}
    <p>No news so far...</p>
  {% endif %}
</div>