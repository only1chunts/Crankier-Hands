
<ul>
{% for thing in site.data.for-sale %}
{% for item in thing.items %}
  <li>
    <a href="{{ item.page-link }}" class="img-responsive" alt="{{item.description}}">
      {{ item.name }}
    </a>
    ({{ item.name | size }} items)
  </li>
{% endfor %}
{% endfor %}
</ul>

       {% for thing in site.data.schedule %}
       {% for timeslot in thing.timeslots %}
       {{timeslot.title}}
       {{timeslot.speaker}}
       {% endfor %}
       {% endfor %}
		