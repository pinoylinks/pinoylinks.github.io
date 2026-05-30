---
# Documentation: https://wowchemy.com/docs/managing-content/

title: "Hugo Notes"
subtitle: "Notes on Hugo templates."
summary: "Notes on Hugo templates."

categories:
  - 📝 Notes
tags: 
- hugo
- snippets

date: 2024-02-21T10:49:20+08:00
lastmod: 2024-02-21T10:49:20+08:00

draft: false

links:
  - name: Hugo Community
    url: https://discourse.gohugo.io/
    icon_pack: fas
    icon: link
---

{{< toc >}}

## Methods

### Title

```yaml
---
title: About us
---
```

```{{ .Title }} → About us```

[Ref](https://gohugo.io/methods/page/title/)

### Date

```go
{{ dateFormat "January 2, 2006 Monday" $.Page.Date }}
```

[Ref](https://gohugo.io/methods/page/date/)

### CurrentSection

```
content/
├── auctions/
│   ├── 2023-11/
│   │   ├── _index.md     <-- current section: 2023-11
│   │   ├── auction-1.md
│   │   └── auction-2.md  <-- current section: 2023-11
```

In _index.md, you can edit the `2023-11` by adding `title: November 2023` inside.

[Ref](https://gohugo.io/methods/page/currentsection/)

### Data

```
data/
├── books/
│   ├── kafka/
│   │   ├── the_metamorphosis.yaml
│   │   └── the_trial.yaml
```

In data/books/kafka/the_metamorphosis.yaml:

```
title: The Metamorphosis
year: 1915
```

```html
<p>{{ index .Site.Data.books.kafka.the_metamorphosis "year" }}</p>
```

## Templates

### Dates

```go
{{ dateFormat "January 2, 2006" $.Page.Date }}
```

```go
{{ .PublishDate.Format "January 2, 2006" }}
```

### Access _index.md title in page bundle

```go
<h1>{{.CurrentSection.Title}}</h1>
```

### Get Yesterday

```go
{{ $yesterday := .Page.Date.AddDate 0 0 -1 }}
{{ dateFormat "January 2, 2006" $yesterday }}
```

## Archetypes

### Make acronyms capitalize

```yaml
title: "{{ replace (replace .Name "-" " ") "html" "HTML" | title }}"
```

### Custom Hour

```yaml
date: {{ now.Format "2006-01-02" }}T14:00:00+08:00
```

### Adds 30 days from now

```yaml
expiryDate: {{ now.AddDate 0 0 30 | time.Format "2006-01-02" }}T14:00:00+08:00
```

### Adds 30 days from any date

```yaml
{{- $mydate := "2024-01-01" }}
date: {{ $mydate }}
expiryDate: {{ (time.AsTime $mydate).AddDate 0 0 30 | time.Format "2006-01-02" }}
```

## Range

### Gets pages in book section

```go
{{ range where .Site.RegularPages "Section" "books" }}
  <p><a href="{{ .Permalink }}">{{ .PublishDate.Format "Jan 2, 2006" }}</a></p>
{{ end }}
```

### Gets last page in book section

```go
{{ range first 1 (where .Site.Pages "Section" "books") }}
{{ partial "books" . }}
{{ end }}
```

### Gets pages in genre tag

```go
{{ range where .Site.RegularPages "Params.tags" "intersect" (slice "genre") }}
  <p><a href="{{ .Permalink }}">{{ .PublishDate.Format "Jan 2, 2006" }}</a></p>
{{ end }}
```

### Data

```
data/
├── books/
│   ├── kafka/
│   │   ├── the_metamorphosis.yaml
│   │   └── the_trial.yaml
```

In data/books/kafka/the_metamorphosis.yaml:

```
title: The Metamorphosis
year: 1915
```

In data/books/kafka/the_trial.yaml:

```
title: The Trial
year: 1914
```

```html
<ul>
  {{ range $key, $value := .Site.Data.books.kafka }}
  <li>{{ index $value "year" }}</li>
  {{ end }}
</ul>
```

Hugo renders as:

```html
<ul>
  <li>1915</li>
  <li>1914</li>
</ul>
```

[Data Method](https://gohugo.io/methods/site/data/)  
[Data templates](https://gohugo.io/templates/data-templates/)

## Tips and Tricks

### Avoid spam

On click the y's will be removed revealing `emailme@example.com`.

```html
<a class="nav-link" href="mailto:yemyyyailyyy@exyyyamypyle.cyoym" onclick="this.href=this.href.replace(/y/g,'');" title="email me">Contact</a>
```

Create a `contact` shortcode and embed in page `{{ contact }}`.

{{< spoiler text="Reference" >}}
[Forum post.](https://discourse.gohugo.io/t/reply-via-email-with-hugo-cloak-email-theme-plugin/43517/4)
{{< /spoiler >}}
