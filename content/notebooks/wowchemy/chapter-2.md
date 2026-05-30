---
title: Blocks v1 (Legacy)
linkTitle: Chapter 2
date: 2024-07-24T08:07:27+08:00
type: book
weight: 2
math: false
highlight: false
tags:
  - chapter
---

<!--more-->

{{< toc >}}

## Markdown Block: Add any elements

```yaml
---
widget: blank
headless: true

# ... Put Your Section Options Here (title etc.) ...
title: My New Section
subtitle:
weight: 10  # section position on page

design:
  # Choose how many columns the section has. Valid values: 1 or 2.
  columns: '1'
---

Add any content here - text, images, videos, galleries - and even HTML code!
```

### Ref
Hugo Blox, [Markdown Block: Add any elements](https://bootstrap.hugoblox.com/blocks-v1/markdown)

## Create your own block

### Ref
Hugo Blox, [Create your own block](https://bootstrap.hugoblox.com/blocks-v1/custom)

## About Me

```yaml
---
widget: 'about.avatar'
headless: true  # This file represents a page section.

# Put Your Section Options Here (title, background etc.)
weight: 10 # Position of section on page

# Choose the user profile to display
# This should be the username (folder name) of a profile in your `content/authors/` folder.
author: 'admin'
---

👋 Hi, there! I'm **Alice**, a machine learning researcher at Netflix.
{style="font-size: 1.2rem; color: #FFB76B;}
```

### Ref
Hugo Blox, [About Me](https://bootstrap.hugoblox.com/blocks-v1/about)

## Accomplishments

```yaml
widget: accomplishments
headless: true  # This file represents a page section.

# Put Your Section Options Here (title, background, etc.) ...
title: My Experience
subtitle:
weight: 10 # The position of section on page

# Date format
#   Refer to https://wowchemy.com/docs/customization/#date-format
date_format: Jan 2006

# Accomplishments.
#   Add/remove as many `item` blocks below as you like.
#   `title`, `organization` and `date_start` are the required parameters.
#   Leave other parameters empty if not required.
#   Begin/end multi-line descriptions with `>-`.
item:
  - organization: Coursera
    organization_url: 'https://www.coursera.org'
    title: Neural Networks and Deep Learning
    url: ''
    certificate_url: 'https://www.coursera.org'
    date_start: '2018-10-01'
    date_end: ''
    description: ''
  - organization: edX
    organization_url: 'https://www.edx.org'
    title: Blockchain Fundamentals
    url: >-
      https://www.edx.org/professional-certificate/uc-berkeleyx-blockchain-fundamentals      
    certificate_url: 'https://www.edx.org'
    date_start: '2018-03-01'
    date_end: ''
    description: 'Formulated informed blockchain models, hypotheses, and use cases.'
  - organization: DataCamp
    organization_url: 'https://www.datacamp.com'
    title: 'Object-Oriented Programming in R: S3 and R6 Course'
    url: ''
    certificate_url: 'https://www.datacamp.com'
    date_start: '2017-07-01'
    date_end: '2017-12-21'
    description: ''
```

### Ref
Hugo Blox, [Accomplishments](https://bootstrap.hugoblox.com/blocks-v1/accomplishments)

## Contact

```yaml
widget: contact
headless: true  # This file represents a page section.

# Put Your Section Options Here (title, background, etc.) ...
title: Contact Me
subtitle: ''
weight: 10

content:
  # Automatically link email and phone or display as text?
  autolink: true

  # Email form provider
  form:
    provider: netlify
    formspree:
      id:
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: false

  # Contact details (edit or remove options as required)
  email: test@example.org
  phone: 888 888 88 88
  address:
    street: 450 Serra Mall
    city: Stanford
    region: CA
    postcode: '94305'
    country: United States
    country_code: US
  coordinates:
    latitude: '37.4275'
    longitude: '-122.1697'
  directions: Enter Building 1 and take the stairs to Office 200 on Floor 2
  office_hours:
    - 'Monday 10:00 to 13:00'
    - 'Wednesday 09:00 to 10:00'
  appointment_url: 'https://calendly.com'
  contact_links:
    - icon: twitter
      icon_pack: fab
      name: DM Me
      link: 'https://twitter.com/Twitter'
    - icon: video
      icon_pack: fas
      name: Zoom Me
      link: 'https://zoom.com'

design:
  # Choose how many columns the section has. Valid values: '1' or '2'.
  columns: '1'
```

### Ref
Hugo Blox, [Contact](https://bootstrap.hugoblox.com/blocks-v1/contact)

## Experience & Education

```yaml
widget: experience
headless: true  # This file represents a page section.

# Put Your Section Options Here (title, background, etc.) ...
title: My Experience
subtitle:
weight: 10 # The position of section on page

# Date format
#   Refer to https://wowchemy.com/docs/getting-started/customization/#date-format
date_format: Jan 2006

# Experiences.
#   Add/remove as many `experience` blocks below as you like.
#   Required fields are `title`, `company`, and `date_start`.
#   Leave `date_end` empty if it's your current employer.
#   Begin/end multi-line descriptions with `>-`.
experience:
  - title: 'CEO'
    company: 'GenCoin'
    company_url: ''
    company_logo: my-logo  # Optional logo
    location: 'California'
    date_start: '2017-01-01'
    date_end: ''
    description: >-
        Responsibilities include:
        
        * Analysing
        * Modelling
        * Deploying
                
  - title: 'Professor'
    company: 'University X'
    company_url: ''
    company_logo: my-logo  # Optional logo
    location: 'California'
    date_start: '2016-01-01'
    date_end: '2016-12-31'
    description: 'Taught electronic engineering and researched semiconductor physics.'
```

### Ref
Hugo Blox, [Experience & Education](https://bootstrap.hugoblox.com/blocks-v1/experience)

## Features / Skills

```yaml
widget: featurette # As of v5.8-dev, 'featurette' is renamed 'features'
headless: true  # This file represents a page section.

# Put Your Section Options Here (title, background, etc.) ...
title: My Experience
subtitle:
weight: 10 # The position of section on page

# Showcase personal skills or business features.
# Add/remove as many `feature` blocks below as you like.
# For available icons, see: https://wowchemy.com/docs/page-builder/#icons
feature:
  - icon: r-project
    icon_pack: fab
    name: R
    description: 90%
  - icon: chart-line
    icon_pack: fas
    name: Statistics
    description: 100%
  - icon: camera-retro
    icon_pack: fas
    name: Photography
    description: 10%

  # Example using an emoji as an icon.
  - icon: '😄'
    icon_pack: emoji
    name: Emojiness
    description: 100%
```

### Ref
Hugo Blox, [Features / Skills](https://bootstrap.hugoblox.com/blocks-v1/features)

## Hero

```yaml
---
widget: hero
headless: true  # This file represents a page section.

# Put Your Section Options Here (title, background, etc.) ...
title: My Hero
weight: 10 # Position of section on the page

# Hero image (optional). Enter filename of an image in the assets/media/ folder.
hero_media: ''

# Call to action links (optional).
#   Display link(s) by specifying a URL and label below. Icon is optional for `cta`.
#   Remove a link/note by deleting a cta/note block.
cta:
  url: 'https://wowchemy.com'
  label: Get Started
  icon_pack: fas
  icon: download
cta_alt:
  url: 'https://wowchemy.com'
  label: View Documentation

# Note. An optional note to show underneath the links.
cta_note:
  label: ''

# Choose an optional background color, gradient, image, or video
design:
  background:
    gradient_end: '#1976d2'
    gradient_start: '#004ba0'
    text_color_light: true
---

Add an intro paragraph here.
```

### Ref
Hugo Blox, [Hero](https://bootstrap.hugoblox.com/blocks-v1/hero)

## Page Collection

```yaml
---
widget: pages # As of v5.8-dev, 'pages' is renamed 'collection'
headless: true  # This file represents a page section.

# Put Your Section Options Here (title, background, etc.) ...
title: Recent Blog Posts
subtitle: ''

# Position of this section on the page
weight: 1

content:
  # Filter content to display
  filters:
    # The folders to display content from
    folders:
      - post
    tag: ''
    category: ''
    publication_type: ''
    author: ''
    featured_only: false
    exclude_featured: false
    exclude_future: false
    exclude_past: false
  # Choose how many pages you would like to display (0 = all pages)
  count: 10
  # Choose how many pages you would like to offset by
  # Useful if you wish to show the first item in the Featured widget
  offset: 0
  # Field to sort by, such as Date or Title
  sort_by: 'Date'
  sort_ascending: false
design:
  # Choose a listing view
  view: compact
  # Choose how many columns the section has. Valid values: '1' or '2'.
  columns: '1'
---

Check out my recent blog posts below!
```

### Ref
Hugo Blox, [Page Collection](https://bootstrap.hugoblox.com/blocks-v1/collection)

## Portfolio: Filter Content

```yaml
widget: portfolio
headless: true  # This file represents a page section.

# ... Put Your Section Options Here (title etc.) ...
title: My Projects
subtitle: ''

content:
  # Choose which content to display in the widget
  filters:
    # Folders to display content from
    folders:
      - project
    # Uncomment below to only show content with specific tags:
#    tags:
#      - Machine Learning
    # Uncomment below to exclude content with specific tags:
#    exclude_tags:
#      - preface    
    # Uncomment below to show specific Hugo Page kinds
    kinds:
      - page
#      - section

  # Field to sort by, such as Date or Title
  sort_by: 'Date'
  sort_ascending: false

  # Filter toolbar (optional).
  # Add or remove as many filters (`filter_button` instances) as you like.
  # To show all items, set `tag` to "*".
  # To filter by a specific tag, set `tag` to an existing tag name.
  # To remove toolbar, delete/comment all instances of `filter_button` below.
  filter_button:
    - name: All
      tag: '*'
    - name: Deep Learning
      tag: Deep Learning
    - name: Other
      tag: Demo

  # Default filter toolbar button (e.g. 0 corresponds to the first `filter_button` instance above)
  filter_default: 0

design:
  # Choose how many columns the section has. Valid values: '1' or '2'.
  columns: '1'
  # Choose a listing view
  view: masonry
  # For Showcase view, flip alternate rows?
  flip_alt_rows: false
```

### Ref
Hugo Blox, [Portfolio: Filter Content](https://bootstrap.hugoblox.com/blocks-v1/portfolio)

## Slider

```yaml
widget: slider  # Use the Slider widget as this page section
weight: 1  # Position of this section on the page
active: true  # Publish this section?
headless: true  # This file represents a page section.

design:
  # Slide height is automatic unless you force a specific height (e.g. '400px')
  slide_height: ''
  is_fullscreen: true
  # Automatically transition through slides?
  loop: false
  # Duration of transition between slides (in ms)
  interval: 2000

content:
  slides:
    - title: 👋 Welcome to the group
      content: Take a look at what we're working on...
      align: center
      background:
        position: right
        color: '#666'
        brightness: 0.7
        media: coders.jpg
        fit: cover
    - title: Lunch & Learn ☕️
      content: 'Share your knowledge with the group and explore exciting new topics together!'
      align: left
      background:
        position: center
        color: '#555'
        brightness: 0.7
        media: contact.jpg
        fit: cover
    - title: World-Class Semiconductor Lab
      content: 'Just opened last month!'
      align: right
      background:
        position: center
        color: '#333'
        brightness: 0.5
        media: welcome.jpg
        fit: cover
      link:
        icon: graduation-cap
        icon_pack: fas
        text: Join Us
        url: ../contact/
```

### Ref
Hugo Blox, [Slider](https://bootstrap.hugoblox.com/blocks-v1/slider)

## Tag Cloud

```yaml
---
widget: tag_cloud
headless: true  # This file represents a page section.

# ... Put Your Section Options Here (title etc.) ...
title: Popular Topics
weight: 10 # Position of section on page

content:
  # Choose the taxonomy from `config.yaml` to display (e.g. tags, categories)
  taxonomy: tags
  # Choose how many tags you would like to display (0 = all tags)
  count: 20
design:
  # Minimum and maximum font sizes (1.0 = 100%).
  font_size_min: 0.7
  font_size_max: 2.0
---
```

### Ref
Hugo Blox, [Tag Cloud](https://bootstrap.hugoblox.com/blocks-v1/tag-cloud)

## Team Members

```yaml
widget: people
headless: true  # This file represents a page section.

# ... Put Your Section Options Here (title etc.) ...

content:
  # Choose which groups/teams of users to display.
  #   Edit `user_groups` in each user's profile to add them to one or more of these groups.
  user_groups:
    - Principal Investigators
    - Researchers
    - Grad Students
    - Administration
    - Visitors
    - Alumni
design:
  # Show user's social networking links? (true/false)
  show_social: false
  # Show user's interests? (true/false)
  show_interests: true
  # Show user's role?
  show_role: true
  # Show user's organizations/affiliations?
  show_organizations: true
```

### Ref
Hugo Blox, [Team Members](https://bootstrap.hugoblox.com/blocks-v1/people)
