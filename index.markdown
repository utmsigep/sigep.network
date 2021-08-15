---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Home
layout: home
---

<div class="row">
<div class="col-md-8">

{% for category in site.data.groups %}
<h2 class="mb-3">{{ category.name }}</h2>
<p>{{ category.description }}</p>
<div class="row">
{% assign sorted_goups = category.groups | sort:"name" %}
{% for group in sorted_goups %}
<div class="col-md-6">
  <div class="card mb-3">
    <div class="card-header">
      {% if group.url %}
      <a href="{{ group.url }}" class="card-title">{{ group.name }}</a>
      {% else %}
      {{ group.name }}
      {% endif %}
    </div>
    <div class="card-body">
      <p class="mb-0">{{ group.description }}</p>
      {% if group.url == null %}
      <p class="text-end mt-3 mb-0"><small><a href="mailto:contact@sigep.network?subject={{ group.name }}" class="btn btn-sm btn-primary"><i class="fas fa-plus"></i> Suggest a Group</a></small></p>
      {% endif %}
    </div>
  </div>
</div>
{% endfor %}
</div>
{% endfor %}

</div>
<div class="col-md-4">

<div class="card mb-3">
  <a href="https://mysigep.org/"><img src="/assets/images/mysigep.png" alt="mySigep" class="card-img-top" /></a>
  <div class="card-body">
    <p>Update your information on <a href="https://mysigep.org/">mySigEp</a> to stay in touch with your local chapter and to volunteer where you live.</p>
  </div>
</div>

<div class="card mb-3">
  <a href="https://sigep.org/the-sigep-experience/events/career-coaching/"><img src="/assets/images/career-coaching.png" alt="Career Coaching" class="card-img-top" /></a>
  <div class="card-body">
    <p>Sign up for <a href="https://sigep.org/the-sigep-experience/events/career-coaching/">Career Coaching</a> to mentor brothers before they enter the workforce.</p>
  </div>
</div>

</div>
