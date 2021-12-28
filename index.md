
<ul>
{% for items in site.data %}
{% assign item = item.name[1] %}
  <li>
    <a href="{{ item.page-link }}" class="img-responsive" alt="{{item.description}}">
      {{ item.name }}
    </a>
    ({{ item.name | size }} items)
  </li>
{% endfor %}
</ul>
