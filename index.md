

{% for thing in site.data.for-sale %}
{% for item in thing.items %}
    <br>{{ item.name }}
    <br>{{ item.page-link }}
	<br>{{ item.description }}
	<br>
{% endfor %}
{% endfor %}


<!--
       {% for thing in site.data.schedule %}
       {% for timeslot in thing.timeslots %}
       {{timeslot.title}}
       {{timeslot.speaker}}
       {% endfor %}
       {% endfor %}
-->		