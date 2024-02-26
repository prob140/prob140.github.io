---
layout: home
title: Home
nav_order: 1
description: A week-to-week description of the content covered in the course.
---

# Data 140: Probability for Data Science
UC Berkeley, Spring 2024
{: .mb-0 .fs-6 .text-grey-dk-000 }

<div>
{% assign professors = site.staffers | where: 'role', 'Professor' | reverse %}
    <div class="role">
        {% for staffer in professors %}
        {{ staffer }}
        {% endfor %}
    </div>
</div>

{% assign announcement = site.announcements | last %}
{{ announcement }}

# Calendar
[**Jump to current week**](#week-7-covariance-and-clt){: .btn } 

{% for module in site.modules %}
{{ module }}
{% endfor %}
