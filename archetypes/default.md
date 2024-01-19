---
title: "{{ replace .Name "-" " " | title }}"
date: "{{ .Date }}"
type: page
lastmod: "{{ .Date }}"
---

This is a page about »{{ replace .Name "-" " " | title }}«.