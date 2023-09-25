---
layout: course
img: brain.png
<!-- img_link: assets/img/dsp.png -->
url_home: index.html
url_git: https://github.com/uiuc-ling-cl
url_campuswire: https://campuswire.com/c/G57E9AFCB
txt_home: LING506 ML
title: LING 448 - Schedule
active_tab: schedule
---


<p style="text-align:center;"><strong>Schedule are subject to change</strong></p>


<h2>Schedule (Spring 2023)</h2>

<table class="table"> 
  <tbody>
    <tr>
      <th>Week</th>
      <th>Date</th>
      <th>Type</th>
      <th>Topic</th>
      <th>Readings</th>
    </tr>
    {% for lecture in site.data.ling506_ml %}
    {% if lecture.topic == "SPRING BREAK" %} 
    	<tr style="background-color: #E0F8F1">
    {% else %}
    	{% if lecture.week == 8 or lecture.week == 15 %} 
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

