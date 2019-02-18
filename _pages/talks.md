---
layout: page
title: Talks
permalink: /talks/
description: Recorded presentations and seminars given over the years.
---

<div class="news">
    <table>
    {% assign talks = site.talks | reverse %}
    {% for item in talks %}
      <tr>
        <td class="date">
        {{ item.date | date: "%b %-d, %Y" }} </td>
        <td class="title">
          {% if item.inline %}
            <a href="{{ item.link }}">{{ item.title | remove: '<p>' | remove: '</p>' | emojify }}</a>
          {% else %}
            <a class="news-title" href="{{ item.url | prepend: site.baseurl }}">{{ item.title }}</a>
          {% endif %}
          <br> <i>{{ item.event }}</i>, {{ item.location }}
        </td>
      </tr>
    {% endfor %}
    </table>
</div>



