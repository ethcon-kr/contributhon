---
layout: page
title: /contributors
permalink: /contributors/
---

```shell
cat "top-contributors"
```
{% assign exist = false %}
{% assign top_pts = 0 %}
{% assign authors = site.posts | map: "author" | uniq %}
{%- for author in authors -%}
{% assign authors_posts = site.posts | where: "author", author %}
{% assign meet_ups = authors_posts | where: "category", "meetup" %}
{% assign translations = authors_posts | where: "category", "translation" %}
{% assign bounty_hunts = authors_posts | where: "category", "bounty-hunt" %}
{% assign dev_exes = authors_posts | where: "category", "DX" %}
{% assign researches = authors_posts | where: "category", "research" %}
{% assign implementations = authors_posts | where: "category", "implementation" %}

{% assign meet_up_pts = meet_ups.size | times: 3 %}
{% assign translation_pts = translations.size | times: 3 %}
{% assign bounty_hunt_pts = bounty_hunts.size | times: 5 %}
{% assign dev_ex_pts = dev_exes.size | times: 10 %}
{% assign research_pts = researches.size | times: 15 %}
{% assign implementation_pts = implementations.size | times: 30 %}
{% assign total_pts = meet_up_pts | plus: translation_pts | plus: bounty_hunt_pts | plus: dev_ex_pts | plus: research_pts | plus: implementation_pts %}
{%- if total_pts > top_pts -%}
{% assign top_pts = total_pts %}
{%- endif -%}
{%- endfor -%}

{%- for author in authors -%}
{% assign authors_posts = site.posts | where: "author", author %}
{% assign meet_ups = authors_posts | where: "category", "meetup" %}
{% assign translations = authors_posts | where: "category", "translation" %}
{% assign bounty_hunts = authors_posts | where: "category", "bounty-hunt" %}
{% assign dev_exes = authors_posts | where: "category", "DX" %}
{% assign researches = authors_posts | where: "category", "research" %}
{% assign implementations = authors_posts | where: "category", "implementation" %}

{% assign meet_up_pts = meet_ups.size | times: 3 %}
{% assign translation_pts = translations.size | times: 3 %}
{% assign bounty_hunt_pts = bounty_hunts.size | times: 5 %}
{% assign dev_ex_pts = dev_exes.size | times: 10 %}
{% assign research_pts = researches.size | times: 15 %}
{% assign implementation_pts = implementations.size | times: 30 %}
{% assign total_pts = meet_up_pts | plus: translation_pts | plus: bounty_hunt_pts | plus: dev_ex_pts | plus: research_pts | plus: implementation_pts %}
{%- if total_pts == top_pts and total_pts >= 30 -%}
{% assign exist = true %}
## <a href="https://github.com/{{ author }}" target="_blank">[{{ author }}]</a>
<ul>
{% unless meet_ups.size == 0 %}
<li> Meetup: {{ meet_ups.size }}</li>
{% endunless %}
{% unless translations.size == 0 %}
<li> Translations: {{ translations.size }}</li>
{% endunless %}
{% unless bounty_hunts.size == 0 %}
<li> Bounty Hunts: {{ bounty_hunts.size }}</li>
{% endunless %}
{% unless dev_exes.size == 0 %}
<li> DXs: {{ dev_exes.size }}</li>
{% endunless %}
{% unless researches.size == 0 %}
<li> Researches: {{ researches.size }}</li>
{% endunless %}
{% unless implementations.size == 0 %}
<li> Implementations: {{ implementations.size }}</li>
{% endunless %}
</ul>
{%- endif -%}
{%- endfor -%}
{%- if exist != true -%}
empty
{%- endif -%}
<br/>

```shell
cat "outstanding-contributors"
```
{% assign exist = false %}
{% assign authors = site.posts | map: "author" | uniq %}
{%- for author in authors -%}
{% assign authors_posts = site.posts | where: "author", author %}
{% assign meet_ups = authors_posts | where: "category", "meetup" %}
{% assign translations = authors_posts | where: "category", "translation" %}
{% assign bounty_hunts = authors_posts | where: "category", "bounty-hunt" %}
{% assign dev_exes = authors_posts | where: "category", "DX" %}
{% assign researches = authors_posts | where: "category", "research" %}
{% assign implementations = authors_posts | where: "category", "implementation" %}

{% assign meet_up_pts = meet_ups.size | times: 3 %}
{% assign translation_pts = translations.size | times: 3 %}
{% assign bounty_hunt_pts = bounty_hunts.size | times: 5 %}
{% assign dev_ex_pts = dev_exes.size | times: 10 %}
{% assign research_pts = researches.size | times: 15 %}
{% assign implementation_pts = implementations.size | times: 30 %}
{% assign total_pts = meet_up_pts | plus: translation_pts | plus: bounty_hunt_pts | plus: dev_ex_pts | plus: research_pts | plus: implementation_pts %}

{%- if total_pts >= 30 and total_pts != top_pts -%}
{% assign exist = true %}
## <a href="https://github.com/{{ author }}" target="_blank">[{{ author }}]</a>
<ul>
{% unless meet_ups.size == 0 %}
<li> Meetup: {{ meet_ups.size }}</li>
{% endunless %}
{% unless translations.size == 0 %}
<li> Translations: {{ translations.size }}</li>
{% endunless %}
{% unless bounty_hunts.size == 0 %}
<li> Bounty Hunts: {{ bounty_hunts.size }}</li>
{% endunless %}
{% unless dev_exes.size == 0 %}
<li> DXs: {{ dev_exes.size }}</li>
{% endunless %}
{% unless researches.size == 0 %}
<li> Researches: {{ researches.size }}</li>
{% endunless %}
{% unless implementations.size == 0 %}
<li> Implementations: {{ implementations.size }}</li>
{% endunless %}
</ul>
{%- endif -%}
{%- endfor -%}
{%- if exist != true -%}
empty
{%- endif -%}
<br/>

```shell
cat "contributors"
```
{% assign exist = false %}
{% assign authors = site.posts | map: "author" | uniq %}
{%- for author in authors -%}
{% assign authors_posts = site.posts | where: "author", author %}
{% assign meet_ups = authors_posts | where: "category", "meetup" %}
{% assign translations = authors_posts | where: "category", "translation" %}
{% assign bounty_hunts = authors_posts | where: "category", "bounty-hunt" %}
{% assign dev_exes = authors_posts | where: "category", "DX" %}
{% assign researches = authors_posts | where: "category", "research" %}
{% assign implementations = authors_posts | where: "category", "implementation" %}

{% assign meet_up_pts = meet_ups.size | times: 3 %}
{% assign translation_pts = translations.size | times: 3 %}
{% assign bounty_hunt_pts = bounty_hunts.size | times: 5 %}
{% assign dev_ex_pts = dev_exes.size | times: 10 %}
{% assign research_pts = researches.size | times: 15 %}
{% assign implementation_pts = implementations.size | times: 30 %}
{% assign total_pts = meet_up_pts | plus: translation_pts | plus: bounty_hunt_pts | plus: dev_ex_pts | plus: research_pts | plus: implementation_pts %}

{%- if total_pts >= 15 and total_pts < 30 and total_pts != top_pts -%}
{% assign exist = true %}
## <a href="https://github.com/{{ author }}" target="_blank">[{{ author }}]</a>
<ul>
{% unless meet_ups.size == 0 %}
<li> Meetup: {{ meet_ups.size }}</li>
{% endunless %}
{% unless translations.size == 0 %}
<li> Translations: {{ translations.size }}</li>
{% endunless %}
{% unless bounty_hunts.size == 0 %}
<li> Bounty Hunts: {{ bounty_hunts.size }}</li>
{% endunless %}
{% unless dev_exes.size == 0 %}
<li> DXs: {{ dev_exes.size }}</li>
{% endunless %}
{% unless researches.size == 0 %}
<li> Researches: {{ researches.size }}</li>
{% endunless %}
{% unless implementations.size == 0 %}
<li> Implementations: {{ implementations.size }}</li>
{% endunless %}
</ul>
{%- endif -%}
{%- endfor -%}
{%- if exist != true -%}
empty
{%- endif -%}
<br/>


```shell
cat "participants"
```
{% assign exist = false %}
{% assign authors = site.posts | map: "author" | uniq %}
{%- for author in authors -%}
{% assign authors_posts = site.posts | where: "author", author %}
{% assign meet_ups = authors_posts | where: "category", "meetup" %}
{% assign translations = authors_posts | where: "category", "translation" %}
{% assign bounty_hunts = authors_posts | where: "category", "bounty-hunt" %}
{% assign dev_exes = authors_posts | where: "category", "DX" %}
{% assign researches = authors_posts | where: "category", "research" %}
{% assign implementations = authors_posts | where: "category", "implementation" %}

{% assign meet_up_pts = meet_ups.size | times: 3 %}
{% assign translation_pts = translations.size | times: 3 %}
{% assign bounty_hunt_pts = bounty_hunts.size | times: 5 %}
{% assign dev_ex_pts = dev_exes.size | times: 10 %}
{% assign research_pts = researches.size | times: 15 %}
{% assign implementation_pts = implementations.size | times: 30 %}
{% assign total_pts = meet_up_pts | plus: translation_pts | plus: bounty_hunt_pts | plus: dev_ex_pts | plus: research_pts | plus: implementation_pts %}

{%- if total_pts < 15 and total_pts != top_pts -%}
{% assign exist = true %}
## <a href="https://github.com/{{ author }}" target="_blank">[{{ author }}]</a>
<ul>
{% unless meet_ups.size == 0 %}
<li> Meetup: {{ meet_ups.size }}</li>
{% endunless %}
{% unless translations.size == 0 %}
<li> Translations: {{ translations.size }}</li>
{% endunless %}
{% unless bounty_hunts.size == 0 %}
<li> Bounty Hunts: {{ bounty_hunts.size }}</li>
{% endunless %}
{% unless dev_exes.size == 0 %}
<li> DXs: {{ dev_exes.size }}</li>
{% endunless %}
{% unless researches.size == 0 %}
<li> Researches: {{ researches.size }}</li>
{% endunless %}
{% unless implementations.size == 0 %}
<li> Implementations: {{ implementations.size }}</li>
{% endunless %}
</ul>
{%- endif -%}
{%- endfor -%}
{%- if exist != true -%}
empty
{%- endif -%}
<br/>
