---
layout: main
img: scribe
img_link: https://en.wikipedia.org/wiki/Scribe#/media/File:Escribano.jpg
img_credit: Escribano by Jean Le Tavernier. Public Domain via Wikimedia Commons.
title: Schedule
active_tab: schedule
---


<p style="text-align:center;"><strong>Schedule and readings are subject to change</strong></p>


<h2>Schedule and Readings</h2>

<table class="table table-striped"> 
  <tbody>
    <tr>
      <th>Week</th>
      <th>Date</th>
      <th>Topic</th>
      <th>Readings</th>
    </tr>
    {% for lecture in site.data.readings %}
    <tr>
      <td>Week {{ lecture.week }}</td>
      <td>{{ lecture.date | date: "%a, %b %d" }}</td>
      <td>
        {% if lecture.slides %}<a href="{{ lecture.slides }}">{{ lecture.title }}</a>
        {% else %}{{ lecture.title }}{% endif %}
	{% if lecture.language %}
	<br/><a href="lin10.html">Language in 10</a>: <a href="{{ lecture.language_slides }}">{{ lecture.language }}</a>
        {% endif %}
      </td>
      <td>
        {% if lecture.reading %}
          <ul class="fa-ul">
          {% for reading in lecture.reading %}
            <li>
            {% if reading.grad_level %}<i class="fa-li fa fa-star"> </i>
            {% elsif reading.optional %}<i class="fa-li fa fa-info-circle"> </i>
            {% else %}<i class="fa-li fa"> </i> {% endif %}
            {{ reading.author }},
            {% if reading.url %}
            <a href="{{ reading.url }}">{{ reading.title }}</a>
            {% else %}
            {{ reading.title }} 
            {% endif %}
            {% if reading.pages %}
            (p. {{ reading.pages }})
            {% endif %}
            </li>
          {% endfor %}
          </ul>
        {% endif %}
      </td>
    </tr>
    {% endfor %}

  </tbody>
</table>

