---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
---

<h4 class="selected-work">SELECTED WORK:</h4>
{% assign work_by_cat = site.data.works | group_by:"category" %}

{% for cat in work_by_cat %}
<div class="work-cat {{cat.name | replace: ' ', '-'}}">
    <h4> {{cat.name | upcase}}</h4>
    <div class="inner">
{% for work in cat.items %}

  <details>

      <summary>{{ work.title }}</summary>
      {% for body in work.body %}
         <a href="{{body.link}}">   {{body.description}}</a>
      {% endfor %}


  </details>

{% endfor %}
</div>
  </div>

{% endfor %}
