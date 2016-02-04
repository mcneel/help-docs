---
title: Index de l'aide de Flamingo
---

<!-- Do not edit the below section. The source for the Help index can be found in the _data folder in the help_index.yaml file -->
{% case page.language %}
  {% when 'cn' %}
    {%assign local_categories = site.data.cn.help-index.main_index %}
  {% when 'de' %}
    {%assign local_categories = site.data.de.help-index.main_index %}
  {% when 'en' %}
    {%assign local_categories = site.data.en.help-index.main_index %}
  {% when 'es' %}
    {%assign local_categories = site.data.es.help-index.main_index %}
  {% when 'fr' %}
    {%assign local_categories = site.data.fr.help-index.main_index%}
  {% when 'it' %}
    {%assign local_categories = site.data.it.help-index.main_index %}
  {% when 'jp' %}
    {%assign local_categories = site.data.jp.help-index.main_index %}
  {% when 'kr' %}
    {%assign local_categories = site.data.kr.help-index.main_index %}
  {% when 'tw' %}
    {%assign local_categories = site.data.tw.help-index.main_index %}
  {% else %}
    {%assign local_categories = site.data.en.help-index.main_index %}
{% endcase %}


# ![images/flamingotab.svg](images/flamingotab.svg) {{local_categories.name}}
{% for category in local_categories.categories %}
## {{category.name}}
{: #{{category.anchor}}}
{% for topic in category.topics %}
[{{topic.name}}]{% if topic.path != null %}({{topic.path}}{% if topic.anchor != null %}#{{topic.anchor}}{% endif %}){% endif %}{% endfor %}
{% endfor %}


<!-- Do not edit this section above. The source for the Help index can be found in the _data folder in the help_index.yaml file-->