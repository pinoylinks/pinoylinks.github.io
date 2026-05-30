---
title: Hugo Data
summary: Use local and remote data sources to augment or create content.
subtitle: Use local and remote data sources to augment or create content.
date: 2025-08-19T23:27:00+08:00
lastmod: 2025-08-19T23:27:00+08:00
_build:
  render: always
  list: always
draft: true
categories: 📝 Notes
links:
  - icon_pack: fas
    icon: link
    url: https://gohugo.io/content-management/data-sources/
    name: Data sources by Hugo
  - name: Hugo and Remote Data Files by CloudCannon
    icon_pack: fas
    icon: icon
    url: https://cloudcannon.com/tutorials/hugo-and-remote-data-files/
---
## create sc `partial/fetchresult.html`

### json

```
{{/* 
Usage:
  {{< fetchresult date="2025-08-15" >}}
*/}}

{{ $url := "https://data.ny.gov/resource/5xaw-6ayf.json" }}
{{ $data := getJSON $url }}
{{ $target := .Get "date" }}

{{ range $data }}
  {{ $dateOnly := (time .draw_date | time.Format "2006-01-02") }}
  {{ if eq $dateOnly $target }}
    <p>{{ .winning_numbers }}</p>
  {{ end }}
{{ end }}
```

### csv

```
{{/* 
Usage:
  {{< fetchresult date="2025-08-15" >}}
*/}}

{{ $url := "https://data.ny.gov/resource/5xaw-6ayf.csv" }}
{{ $data := getCSV "," $url }}
{{ $target := .Get "date" }}

{{ range $index, $row := $data }}
  {{ if gt $index 0 }} {{/* skip header row */}}
    {{ $dateOnly := (time (index $row 0) | time.Format "2006-01-02") }}
    {{ if eq $dateOnly $target }}
      <p>{{ index $row 1 }}</p>
    {{ end }}
  {{ end }}
{{ end }}
```

## call sc

```
The winning numbers are: {{< fetchresult date="2025-08-15" >}}
```

## another csv


```
{{/* 
Usage:
  {{< fetchresult date="02.01.2010" time="11:00" >}}
*/}}

{{ $url := "https://www.pcsodraw.com/download/ez_2_lotto.csv" }}
{{ $data := getCSV "," $url }}
{{ $targetDate := .Get "date" }}
{{ $targetTime := .Get "time" }}

{{ range after 1 $data }} {{/* skip header if any */}}
  {{ $rowDate := index . 1 }}
  {{ $rowTime := index . 2 }}
  {{ if and (eq $rowDate $targetDate) (eq $rowTime $targetTime) }}
    <div class="result">
      {{ index . 3 }} - {{ index . 4 }}
    </div>
    {{ break }} {{/* stop after first match */}}
  {{ end }}
{{ end }}
```

## call sc

```
{{< data/ez2 date="19.08.2025" time="21:00" >}}
```

## tip

sometimes the columns that we see on the table is not their actual indices.

test them to know their actual indices.

```
{{ $apples := getCSV "," "https://www.pcsodraw.com/download/ez_2_lotto.csv" }}
<ul class="apples">
{{ range after 1 $apples }}
 <li>{{ index . 0 }} - {{ index . 1 }} - {{ index . 2 }} - {{ index . 3 }} - {{ index . 4 }}</li>
{{ end }}
</ul>
```

## call sc

```
{{< test >}}
```
