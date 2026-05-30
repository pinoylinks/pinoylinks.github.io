---
title: "{{ replace .Name "-" " " | title }}"
linkTitle: "{{ replace .Name "-" " " | title }}"
summary: 
date: {{ .Date }}
type: book
categories:
- 📔 Notebooks
tags:
  - recent
---

<!--more-->

{{< list_children >}}

{{< cta cta_text="👉 Get started" cta_link="chapter-1" >}}
