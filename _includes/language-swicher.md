{% assign current_lang = page.lang | default: site.default_lang %}
{% assign strings = site.data.strings[current_lang] %}

---

**{{ strings.language }}:** 
{% if current_lang == 'ja' %}
*日本語* | [English]({{ page.url | replace: '.html', '' | prepend: '/en' | append: '/' | relative_url }})
{% else %}
[日本語]({{ page.url | replace: '/en/', '/' | relative_url }}) | *English*
{% endif %}

---