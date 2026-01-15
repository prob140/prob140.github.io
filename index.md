---
layout: home
title: Home
nav_order: 1
description: A week-to-week description of the content covered in the course.
---

# Data 140: Probability for Data Science
UC Berkeley, Fall 2025
{: .mb-0 .fs-6 .text-grey-dk-000 }

<!-- <div>
{% assign professors = site.staffers | where: 'role', 'Professor' | reverse %}
    <div class="role">
        {% for staffer in professors %}
        {{ staffer }}
        {% endfor %}
    </div>
</div> -->

{%- if site.enable_announcements -%}

    {% assign announcement = site.announcements | last %}
    {{ announcement }}
{%- endif -%}

# Calendar

<div>
{%- include schedule.html -%}
</div>