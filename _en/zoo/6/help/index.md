---
title: Zoo License Manager Help Index
description: The Zoo keeps your Rhino licenses in one place and lets you share them with Rhino users on your network.
productname: Zoo License Manager
language: en
productpath: zoo
productversionpath: 6
type: help
collectionname: Help
keywords: ['zoo', 'rhinoceros', 'license', 'manager']
layout: zoo-help-page
---

<!-- Do not edit the below section. The source for the Help index can be found in the _data folder in the help_index.yaml file -->
{% case page.language %}
  {% when 'cn' %}
    {%assign local_categories = site.data.cn.zoo-help-index.main_index %}
  {% when 'de' %}
    {%assign local_categories = site.data.de.zoo-help-index.main_index %}
  {% when 'en' %}
    {%assign local_categories = site.data.en.zoo-help-index.main_index %}
  {% when 'es' %}
    {%assign local_categories = site.data.es.zoo-help-index.main_index %}
  {% when 'fr' %}
    {%assign local_categories = site.data.fr.zoo-help-index.main_index%}
  {% when 'it' %}
    {%assign local_categories = site.data.it.zoo-help-index.main_index %}
  {% when 'jp' %}
    {%assign local_categories = site.data.jp.zoo-help-index.main_index %}
  {% when 'kr' %}
    {%assign local_categories = site.data.kr.zoo-help-index.main_index %}
  {% when 'tw' %}
    {%assign local_categories = site.data.tw.zoo-help-index.main_index %}
  {% else %}
    {%assign local_categories = site.data.en.zoo-help-index.main_index %}
{% endcase %}


# {{local_categories.name}}
{% for category in local_categories.categories %}
## {{category.name}}
{: #{{category.anchor}}}
<ul>
{% for topic in category.topics %}
<li>
<a href="{% if topic.path != null %}{{topic.path}}{% if topic.anchor != null %}#{{topic.anchor}}{% endif %}{% endif %}">{{topic.name}}</a>
</li>
{% endfor %}
</ul>
{% endfor %}


<!-- Do not edit this section above. The source for the Help index can be found in the _data folder in the help_index.yaml file-->
