

{% for thing in site.data.for-sale %}
{% for item in thing.items %}

    {{ item.page-link }}
	{{ item.description }}
    {{ item.name }}

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