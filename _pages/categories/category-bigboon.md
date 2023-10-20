---
title: "I didn't know you were like this, 빅분기 취득기."
layout: archive
permalink: categories/bigboon
author_profile: true
sidebar_main: true
---

<!-- 공백이 포함되어 있는 카테고리 이름의 경우 site.categories['a b c'] 이런식으로! -->

***

{% assign posts = site.categories.Bigboon %}
{% for post in posts %} {% include archive-single2.html type=page.entries_layout %} {% endfor %}