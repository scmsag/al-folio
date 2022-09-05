---
layout: page
title: Seminars
permalink: /seminars/
description: This page contains a full list of seminars.
nav: true
years: [2020,2021,2022]
horizontal: false
---
<div class="projects">
{% for y in page.years %}
    <h2 class="year">{{y}}</h2>
    {% assign year_seminars = site.seminars | where: "year", y %}
    {% assign sorted_seminars = year_seminars | sort: "time" %}
	<div class="container">
	    <div class="row row-cols-1">
            {% for seminar in sorted_seminars %}
    	         {% include seminars.html %}
	    {% endfor %}
	    </div>
	</div>
{% endfor %}

</div>
