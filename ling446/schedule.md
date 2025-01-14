---
layout: course
img: sg.png
<!-- img_link: assets/img/sg.png -->
url_home: index.html
url_git: https://github.com/uiuc-ling-cl
url_campuswire: https://campuswire.com/c/G39EB8524
txt_home: LING446
title: LING446 - Schedule
active_tab: schedule
---


<p style="text-align:center;"><strong>Schedule are subject to change</strong></p>


<h2>Schedule (Spring 2025)</h2>

<table class="table">  <!-- table-stripe -->
  <tbody>
    <tr>
      <th>Week</th>
      <th>Date</th>
      <th>Type</th>
      <th>Topic</th>
      <th>Readings</th>
    </tr>
    {% for lecture in site.data.ling446 %}
    {% if lecture.topic == "SPRING BREAK" %} 
    	<tr style="background-color: #E0F8F1">
    {% else %}
    	{% if lecture.week == 8 or lecture.week == 16 %} 
    		<tr style="background-color: #F8E0E6">
    	{% else %}
    		<tr>
    	{% endif %}	
    {% endif %}
    
      <td>
        {% if lecture.type == "Lecture" or lecture.type == "&nbsp;" %}Week {{ lecture.week }}
        {% else %}&nbsp;{% endif %} 
      </td>
      <td>{{ lecture.date | date: "%a, %b %d" }}</td>
      <td>{{ lecture.type }}</td>
      
      
      
      <td>
        {% if lecture.slides %}<a href="{{ lecture.slides }}">{{ lecture.topic }}</a>
        {% else %}
        	{% if lecture.topic == "SPRING BREAK" %}<em>{{ lecture.topic }}</em>
        	{% else %}{{ lecture.topic }}{% endif %}    	
        {% endif %}
      </td>
      
      <td>{{ lecture.readings }}</td>
    </tr>
    {% endfor %}

  </tbody>
</table>

