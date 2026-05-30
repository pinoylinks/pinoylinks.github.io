---
title: Blocks
linkTitle: Chapter 1
date: 2024-07-24T08:07:27+08:00
type: book
weight: 1
math: false
highlight: false
tags:
  - chapter
---

<!--more-->

{{< toc >}}

## Markdown: Add any elements

```yaml
---
title: My page
type: landing

sections:
  - block: markdown
    content:
      title: My title
      subtitle: My subtitle
      text: Add any **markdown** formatted content here - text, images, videos, galleries - and even HTML code!
    design:
      # See Page Builder docs for all section customization options.
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
---
```

### Ref
Hugo Blox, [Markdown: Add any elements](https://bootstrap.hugoblox.com/markdown)

## Create your own block

### Ref
Hugo Blox, [Create your own block](https://bootstrap.hugoblox.com/custom)

## 👑 Testimonials

```yaml
---
title: My page
type: landing

sections:
  - block: testimonials
    content:
      title: Testimonials
      subtitle: What our customers have to say about us
      items:
        - name: Geo
          username: '@geo'
          # Image path relative to assets/media/ folder
          image_filename: tweets/GitHub.png
          link: https://wowchemy.com
          text: Awesome!
        - name: Bob
          username: '@bob'
          image_filename: tweets/GitHub.png
          link: https://wowchemy.com
          text: Love it!
---
```

### Ref
Hugo Blox, [👑 Testimonials](https://bootstrap.hugoblox.com/testimonials)

## Skills

```yaml
---
title: My page
type: landing

sections:
  - block: skills
    content:
      title: Skills
      text: ''
      # Choose a user to display skills from (a folder name within `content/authors/`)
      username: admin
    design:
      columns: '1'
---
```

### Ref
Hugo Blox, [Skills](https://bootstrap.hugoblox.com/skills)

## Team Members

```yaml
---
title: Meet the Team
type: landing

sections:
  - block: people
    content:
      title: Meet the Team
      # Choose which groups/teams of users to display.
      #   Edit `user_groups` in each user's profile to add them to one or more of these groups.
      user_groups:
        - Principal Investigators
        - Researchers
        - Grad Students
        - Administration
        - Visitors
        - Alumni
      sort_by: Params.last_name
      sort_ascending: true
    design:
      # Show user's social networking links? (true/false)
      show_social: false
      # Show user's interests? (true/false)
      show_interests: true
      # Show user's role?
      show_role: true
      # Show user's organizations/affiliations?
      show_organizations: true
---
```

### Ref
Hugo Blox, [Team Members](https://bootstrap.hugoblox.com/people)

## Biography

```yaml
---
title: My page
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
---
```

### Ref
Hugo Blox, [Biography](https://bootstrap.hugoblox.com/biography)

## 👑 Company Logos

```yaml
---
title: My page
type: landing

sections:
  - block: logos
    content:
      title: Section Title
      subtitle: Section Subtitle
      # Path to the logo images within the `assets/media/` folder
      logo_folder: logos
    design:
      columns: '1'  
---
```

### Ref
Hugo Blox, [👑 Company Logos](https://bootstrap.hugoblox.com/logos)

## 👑 Pricing

```yaml
---
title: My page
type: landing

sections:
  - block: pricing
    content:
      title: Sponsor
      subtitle: Sponsor the project you love!
      plans:
        - title: Starter
          price: $9
          period: /month
          description: Our starter option
          highlight: ''
          button:
            url: https://example.com
            text: Get Started          
          features:
            - All the blocks you need
            - No setup
            - Community support
        - title: Premium
          price: $99
          period: /month
          description: Our premium option
          highlight: Most Popular
          button:
            url: https://example.com
            text: Get Started
          features:
            - All the blocks you need
            - No setup
            - Community support
            - Access to exclusive features
        - title: Enterprise
          price: $999
          period: /month
          description: Our enterprise option
          highlight: ''
          button:
            url: https://example.com
            text: Get Started
          features:
            - All the blocks you need
            - No setup
            - Community support
            - Access to exclusive features
            - Enterprise support
---
```

### Ref
Hugo Blox, [👑 Pricing](https://bootstrap.hugoblox.com/pricing)

## About Me

```yaml
---
title: My page
type: landing

sections:
  - block: about.avatar
    id: about
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      # Override your profile text from `authors/admin/_index.md`?
      text: |>
        👋 Hi, there! I'm **Alice**, a machine learning researcher at Netflix.
        {style="font-size: 1.2rem; color: #FFB76B;} 
---
```

### Ref
Hugo Blox, [About Me](https://bootstrap.hugoblox.com/about)

## Accomplishments

```yaml
---
title: My page
type: landing

sections:
  - block: accomplishments
    content:
      title: Accomplishments
      subtitle: ''
      text: ''
      # Date format: https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Accomplishments.
      #   Add/remove as many `items` blocks below as you like.
      #   `title`, `organization`, and `date_start` are the required parameters.
      #   Leave other parameters empty if not required.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Neural Networks and Deep Learning
          certificate_url: https://www.coursera.org
          date_end: ''
          date_start: '2021-01-25'
          description: ''
          icon: coursera
          organization: Coursera
          organization_url: https://www.coursera.org
          url: ''
        - title: Blockchain Fundamentals
          certificate_url: https://www.edx.org
          date_end: ''
          date_start: '2021-01-01'
          description: Formulated informed blockchain models, hypotheses, and use cases.
          icon: edx
          organization: edX
          organization_url: https://www.edx.org
          url: https://www.edx.org/professional-certificate/uc-berkeleyx-blockchain-fundamentals
        - title: 'Object-Oriented Programming in R'
          certificate_url: https://www.datacamp.com
          date_end: '2020-12-21'
          date_start: '2020-07-01'
          description: ''
          icon: datacamp
          organization: DataCamp
          organization_url: https://www.datacamp.com
          url: ''
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '2'
---
```

### Ref
Hugo Blox, [Accomplishments](https://bootstrap.hugoblox.com/accomplishments)

## Contact

```yaml
---
title: My page
type: landing

sections:
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle: ''
      text: ''
      # Contact details - edit or remove options as needed
      email: test@example.org
      phone: 888 888 88 88
      appointment_url: 'https://calendly.com'
      address:
        street: 450 Serra Mall
        city: Stanford
        region: CA
        postcode: '94305'
        country: United States
        country_code: US
      directions: Enter Building 1 and take the stairs to Office 200 on Floor 2
      office_hours:
        - 'Monday 10:00 to 13:00'
        - 'Wednesday 09:00 to 10:00'
      contact_links:
        - icon: twitter
          icon_pack: fab
          name: DM Me
          link: 'https://twitter.com/Twitter'
        - icon: skype
          icon_pack: fab
          name: Skype Me
          link: 'skype:echo123?call'
        - icon: video
          icon_pack: fas
          name: Zoom Me
          link: 'https://zoom.com'
      # Automatically link email and phone or display them just as text?
      autolink: true
      # Choose an email form provider (netlify/formspree)
      form:
        provider: netlify
        formspree:
          # If using Formspree, enter your Formspree form ID
          id: ''
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: false
      # Coordinates to display a map - set your map provider in `params.yaml`
      coordinates:
        latitude: '37.4275'
        longitude: '-122.1697'
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
---
```

### Ref
Hugo Blox, [Contact](https://bootstrap.hugoblox.com/contact)

## Experience & Education

```yaml
---
title: My page
type: landing

sections:
  - block: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many experience `items` below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: CEO
          company: GenCoin
          company_url: ''
          company_logo: org-gc
          location: California
          date_start: '2021-01-01'
          date_end: ''
          description: |2-
              Responsibilities include:

              * Analysing
              * Modelling
              * Deploying
        - title: Professor of Semiconductor Physics
          company: University X
          company_url: ''
          company_logo: org-x
          location: California
          date_start: '2016-01-01'
          date_end: '2020-12-31'
          description: Taught electronic engineering and researched semiconductor physics.
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
---
```

### Ref
Hugo Blox, [Experience & Education](https://bootstrap.hugoblox.com/experience)

## Features

```yaml
---
title: My page
type: landing

sections:
  - block: features
    content:
      title: My Interests
      subtitle: Section subtitle
      text: Section text
      items:
        - name: R
          description: 90%
          icon: r-project
          icon_pack: fab
        - name: Statistics
          description: 100%
          icon: chart-line
          icon_pack: fas
        - name: Photography
          description: 10%
          icon: camera-retro
          icon_pack: fas
---
```

### Ref
Hugo Blox, [Features](https://bootstrap.hugoblox.com/features)

## Hero

```yaml
---
sections:
  - block: hero
    content:
      title: Your Hero Title
      image:
        # Reference an image in your `assets/media/` folder
        filename: hero-academic.png
      # Add your Call-To-Action (CTA) button and optional icon
      cta:
        label: Get Started
        url: https://wowchemy.com/templates/
        #icon_pack: fas
        #icon: download
      # Optionally, add an alternative CTA link
      cta_alt:
        label: Ask a question
        url: https://discord.gg/z8wNYzb
      # Optionally, add a note under the Call-To-Action button
      cta_note:
        label: >-
          <div style="text-shadow: none;"><a class="github-button" href="https://github.com/HugoBlox/hugo-blox-builder" data-icon="octicon-star" data-size="large" data-show-count="true" aria-label="Star">Star Hugo Blox Builder</a></div><div style="text-shadow: none;"><a class="github-button" href="https://github.com/wowchemy/starter-hugo-academic" data-icon="octicon-star" data-size="large" data-show-count="true" aria-label="Star">Star the Academic template</a></div>          
      # Add your Hero text here
      text: |-
        **Generated by Hugo Blox Builder - the FREE, Hugo-based open source website builder trusted by 500,000+ sites.**

        **Easily build anything with blocks - no-code required!**

        From landing pages, second brains, and courses to academic resumés, conferences, and tech blogs.

        <!--Custom spacing-->
        <div class="mb-3"></div>
        <!--GitHub Button JS-->
        <script async defer src="https://buttons.github.io/buttons.js"></script>        
    design:
      # Choose an optional background color, gradient, image, or video
      background:
        gradient_end: '#1976d2'
        gradient_start: '#004ba0'
        text_color_light: true
---
```

### Ref
Hugo Blox, [Hero](https://bootstrap.hugoblox.com/hero)

## Page Collection

```yaml
---
title: My page
type: landing

sections:
  - block: collection
    id: posts
    content:
      title: Recent Posts
      subtitle: ''
      text: 'Check out my recent blog posts below!'
      # Choose how many pages you would like to display (0 = all pages)
      count: 5
      # Filter on criteria
      filters:
        # The folders to display content from
        folders:
          - post
        author: ""
        category: ""
        tag: ""
        publication_type: ""
        featured_only: false
        exclude_featured: false
        exclude_future: false
        exclude_past: false
      # Choose how many pages you would like to offset by
      # Useful if you wish to show the first item in the Featured widget
      offset: 0
      # Field to sort by, such as Date or Title
      sort_by: 'Date'
      sort_ascending: false
    design:
      # Choose a listing view
      view: compact
      # Choose single or dual column layout
      columns: '1'
---
```

### Ref
Hugo Blox, [Page Collection](https://bootstrap.hugoblox.com/collection)

## Portfolio: Filter Content

```yaml
---
title: My page
type: landing

sections:
  - block: portfolio
    id: projects
    content:
      title: Projects
      subtitle: My subtitle
      text: Add any **markdown** formatted content here - text, images, videos, galleries - and even HTML code!
      filters:
        # Folders to display content from
        folders:
          - project
        # Only show content with these tags
        tags: []
        # Exclude content with these tags
        exclude_tags: []
        # Which Hugo page kinds to show (https://gohugo.io/templates/section-templates/#page-kinds)
        kinds:
          - page
      # Field to sort by, such as Date or Title
      sort_by: 'Date'
      sort_ascending: false
      # Default portfolio filter button
      # 0 corresponds to the first button below and so on
      # For example, 0 will default to showing all content as the first button below shows content with *any* tag
      default_button_index: 0
      # Filter button toolbar (optional).
      # Add or remove as many buttons as you like.
      # To show all content, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the button toolbar, delete the entire `buttons` block.
      buttons:
        - name: All
          tag: '*'
        - name: Deep Learning
          tag: Deep Learning
        - name: Other
          tag: Demo
    design:
      # See Page Builder docs for all section customization options.
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      # Choose a listing view
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false
---
```

### Ref
Hugo Blox, [Portfolio: Filter Content](https://bootstrap.hugoblox.com/portfolio)

## Slider

```yaml
---
title: My page
type: landing

sections:
  - block: slider
    content:
      slides:
        - title: 👋 Welcome to the group
          content: Take a look at what we're working on...
          align: center
          background:
            image:
              # Specify an image from `assets/media/`
              # or delete the image section to remove it
              filename: coders.jpg
              filters:
                brightness: 0.7
            position: right
            color: '#666'
        - title: Lunch & Learn ☕️
          content: 'Share your knowledge with the group and explore exciting new topics together!'
          align: left
          background:
            image:
              # Specify an image from `assets/media/`
              # or delete the image section to remove it
              filename: contact.jpg
              filters:
                brightness: 0.7
            position: center
            color: '#555'
        - title: World-Class Semiconductor Lab
          content: 'Just opened last month!'
          align: right
          background:
            image:
              # Specify an image from `assets/media/`
              # or delete the image section to remove it
              filename: welcome.jpg
              filters:
                brightness: 0.5
            position: center
            color: '#333'
          link:
            icon: graduation-cap
            icon_pack: fas
            text: Join Us
            url: ../contact/
    design:
      # Slide height is automatic unless you force a specific height (e.g. '400px')
      slide_height: ''
      # Make the slides full screen within the browser window?
      is_fullscreen: true
      # Automatically transition through slides?
      loop: false
      # Duration of transition between slides (in ms)
      interval: 2000
---
```

### Ref
Hugo Blox, [Slider](https://bootstrap.hugoblox.com/slider)

## Tag Cloud

```yaml
---
title: My page
type: landing

sections:
  - block: tag_cloud
    content:
      title: My title
      subtitle: My subtitle
      text: Add any **markdown** formatted content here - text, images, videos, galleries - and even HTML code!
      # Choose a taxonomy from the `taxonomies` list in `config.yaml` to display (e.g. tags, categories, authors)
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
Hugo Blox, [Tag Cloud](https://bootstrap.hugoblox.com/tag-cloud)
