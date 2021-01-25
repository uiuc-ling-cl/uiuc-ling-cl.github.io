---
layout: course
img: brain.png
<!-- img_link: assets/img/dsp.png -->
url_home: index.html
url_git: https://github.com/uiuc-ling-cl
url_campuswire: https://campuswire.com/p/GD03E1221
txt_home: LING506 ML
title: LING506 ML - Schedule
active_tab: schedule
---


<p style="text-align:center;"><strong>Schedule are subject to change</strong></p>


<h2>Schedule</h2>

<table class="table table-striped"> 
  <tbody>
    <tr>
      <th>Week</th>
      <th>Date</th>
      <th>Type</th>
      <th>Topic</th>
      <th>Readings</th>
    </tr>
    {% for lecture in site.data.ling506_ml %}
    <tr>
      <td>
        {% if lecture.type == "Lecture" or lecture.type == "&nbsp;" %}Week {{ lecture.week }}
        {% else %}&nbsp;{% endif %} 
      </td>
      <td>{{ lecture.date | date: "%a, %b %d" }}</td>
      <td>{{ lecture.type }}</td>
      
      
      
      <td>
        {% if lecture.slides %}<a href="{{ lecture.slides }}">{{ lecture.topic }}</a>
        {% else %}
        	{% if lecture.topic == "Spring break" %}<em>{{ lecture.topic }}</em>
        	{% else %}{{ lecture.topic }}{% endif %}    	
        {% endif %}
      </td>
    </tr>
    {% endfor %}

  </tbody>
</table>

