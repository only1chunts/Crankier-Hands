
<ul>
{% for thing in site.data.for-sale %}
{% for item in thing.items %}
  <li>
    {{ item.page-link }}
	{{item.description}}
    {{ item.name }}
  </li>
{% endfor %}
{% endfor %}
</ul>

<!--
       {% for thing in site.data.schedule %}
       {% for timeslot in thing.timeslots %}
       {{timeslot.title}}
       {{timeslot.speaker}}
       {% endfor %}
       {% endfor %}
-->		