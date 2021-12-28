

{% for thing in site.data.for-sale %}
{% for item in thing.items %}
    
    {{ item.name }}
    {{ item.page-link }}
	{{ item.description }}
	
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