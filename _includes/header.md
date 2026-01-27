---
# ヘッダーコンポーネント
---

{% assign lang = page.lang | default: site.default_lang %}
{% assign nav = site.data.navigation[lang] %}
{% assign strings = site.data.strings[lang] %}

# {{ site.title }}

{% for item in nav.main %}
[{{ item.title }}]({{ item.url | relative_url }})
{% unless forloop.last %} | {% endunless %}
{% endfor %}