---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

title: Home
layout: home
---

## Regional and Special Interest Groups

{% for group in site.data.groups %}

### [{{ group.name }}]({{ group.url }})

{{ group.description }}



{% endfor %}



## Other Opportunities

### mySigEp

Update your information on [mySigEp](https://mysigep.org/)

### Career Coaching

Sign up for [Career Coaching](https://sigep.org/the-sigep-experience/events/career-coaching/)
