---
layout: page
title: Students
permalink: /students/
weight: 2
group: students
---
Are you interested in joining my research group? Apply to the [Computing Science Department at UAlberta](https://www.ualberta.ca/computing-science/graduate-studies/programs-and-admissions/applications-and-admissions).

## Current Maplers
{% for member in site.data.advisees %}
<div class="student" name="{{ member.id }}">
  <div class="student-pic">
    <img alt="{{ member.name }}" src="{{ "/resources/images/students/anon.png" | prepend: site.baseurl }}" />
      <!-- <svg viewBox="0 0 512 512">
          <path d="M439.332,295.286c0,11.501,9.303,20.857,20.803,20.857s20.858-9.356,20.858-20.857  c0-9.134-5.977-16.687-14.207-19.507v-82.503c0-0.366,0-1.917,0-2.452c-0.057-2.424-1.521-4.566-3.721-5.581l-42.395-19.337  c-58.967-26.891-151.703-69.115-169.152-77.064c-1.69-0.732-3.58-0.732-5.271,0L34.731,185.243  c-2.197,0.986-3.664,3.157-3.721,5.581c-0.084,2.396,1.212,4.679,3.354,5.807c1.945,1.043,196.016,104.744,211.604,112.807  c0.901,0.507,1.917,0.731,2.932,0.731c1.016,0,2.059-0.226,2.987-0.731c1.748-0.932,158.864-84.958,202.188-107.901v74.133  C445.59,278.316,439.332,285.956,439.332,295.286z M238.78,328.097c-7.809-4.03-61.983-32.923-113.566-60.462v67.424  c0,1.776,0.732,3.468,2.029,4.651c17.589,16.207,64.55,53.865,120.755,53.865c27.481,0,70.468-9.217,120.078-53.781  c1.325-1.24,2.086-2.932,2.086-4.735v-66.605c-54.457,29.089-110.664,59.137-111.734,59.7  C252.676,331.281,244.784,331.395,238.78,328.097z M460.135,332.944c-3.947,0-7.611-0.986-11.162-2.283l-3.75,93.047h29.795  l-3.721-93.047C467.801,331.958,464.079,332.944,460.135,332.944z"/>
      </svg> -->
  </div>
	<div class="student-info">
		<p>
      <!-- <a href="{{ member.website }}">{{ member.name }}</a> -->
      {{ member.name }}
      <mark>{{ member.prog }}</mark>
      {% if member.website %}
        <mark><a href="{{ member.website }}" target="_blank">website</a></mark>
      {% endif %}
    </p>
    <p>{{ member.bio }}</p>
	</div>
</div>
{% endfor %}


<hr>
## PhD ##
* Lisa Nguyen (University of Paderborn)
* Johannes Späth (University of Paderborn)
* Stefan Krüger (University of Paderborn)

## Master's ##
* Erick Ochoa (University of Alberta)

## BSc. ##
* Jeff Cho (University of Alberta)

## Alumni ##
* Alexander MacKenzie (BSc.)
* Stuart Hoye (BSc.)
* Adrian Margel (High School)
* Noah Weninger (BSc.)
* Michael Appel (Master's)
* Manuel Benz (Master's) [PhD at University of Paderborn]
* Stefan Triller (PhD, *withdrawn*) [Deutsche Telekom]
