{% assign lang = page.lang | default: site.default_lang %}
{% assign nav = site.data.navigation[lang] %}

## トピック

{% for topic in nav.topics %}
- {{ topic.icon }} [{{ topic.title }}]({{ topic.url | relative_url }})
{% endfor %}