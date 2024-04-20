---
layout: default
title: "Jekyll Computer Modern Theme"
---

# Kais Mathe-Seiten

Mathe-Notizen, in denen ich mir die Sachen aufschreibe, die in Lehrbüchern unter "wie man offensichtlich sieht" oder so ähnlich abgehakt werden.

## Themen
{% for page in site.pages %}<p><a href="{{ site.url }}{{ page.url }}">{{ page.title }}</a></p>{% endfor %}

[Example Static Page]({{site.url}}/example-static-page/)
