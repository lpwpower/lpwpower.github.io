---
# Leave the homepage title empty to use the site title
title: ""
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: "2rem"

sections:
  - block: resume-biography
    content:
      # The user's folder name in `content/authors/`
      username: admin
      # Show a call-to-action button under your biography? (optional)
      # To link to a file, upload it to your `static/uploads/` folder
      button:
        text: Download Résumé
        # url: uploads/resume.pdf
    design:
      banner:
        # Upload a cover image to `assets/media/` folder and reference its filename here (optional)
        filename: 'kalen-emsley-Bkci_8qcdvQ-unsplash.jpg'
      biography:
        # Customize the style of your biography text
        style: 'text-align: justify; font-size: 0.8em;'
      spacing:
        # Customize the section spacing. Order is top, right, bottom, left.
        padding: ['0', '0', '2rem', '0']
  # - block: resume-biography-3
  #   content:
  #     # Choose a user profile to display (a folder name within `content/authors/`)
  #     username: admin
  #     text: ""
  #     # Show a call-to-action button under your biography? (optional)
  #     button:
  #       text: Download CV
  #       url: uploads/resume.pdf
  #   design:
  #     css_class: dark
  #     background:
  #       color: white
  #       image:
  #         # Add your image background to `assets/media/`.
  #         filename: kalen-emsley-Bkci_8qcdvQ-unsplash.jpg #stacked-peaks.svg
  #         filters:
  #           brightness: 1.0
  #         size: actual #cover
  #         position: center
  #         parallax: false
  # - block: markdown
  #   content:
  #     title: '📚 My Research'
  #     subtitle: ''
  #     text: |-
  #       Use this area to speak to your mission. I'm a research scientist in the Moonshot team at DeepMind. I blog about machine learning, deep learning, and moonshots.

  #       I apply a range of qualitative and quantitative methods to comprehensively investigate the role of science and technology in the economy.
        
  #       Please reach out to collaborate 😃
  #   design:
  #     columns: '1'
  - block: collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publication
        featured_only: true
    design:
      view: article-grid
      columns: 2
  - block: collection
    content:
      title: All Publications
      # text: 'Papers are categorized by [topic](https://github.com/lpwpower/TECDI).'
      # button: 
      #   text: Papers are categorized by topic.
      #   url: https://lpwpower.github.io/tags/
      filters:
        folders:
          - publication
        exclude_featured: false
    design:
      view: citation
      spacing:
        # Customize the section spacing. Order is top, right, bottom, left.
        padding: ['0', '0', '2rem', '0']
  # - block: collection
  #   id: talks
  #   content:
  #     title: Recent & Upcoming Talks
  #     filters:
  #       folders:
  #         - event
  #   design:
  #     view: article-grid
  #     columns: 1
  # - block: collection
  #   id: news
  #   content:
  #     title: Recent News
  #     subtitle: ''
  #     text: ''
  #     # Page type to display. E.g. post, talk, publication...
  #     page_type: post
  #     # Choose how many pages you would like to display (0 = all pages)
  #     count: 5
  #     # Filter on criteria
  #     filters:
  #       author: ""
  #       category: ""
  #       tag: ""
  #       exclude_featured: false
  #       exclude_future: false
  #       exclude_past: false
  #       publication_type: ""
  #     # Choose how many pages you would like to offset by
  #     offset: 0
  #     # Page order: descending (desc) or ascending (asc) date.
  #     order: desc
  #   design:
  #     # Choose a layout view
  #     view: date-title-summary
  #     # Reduce spacing
  #     spacing:
  #       padding: [0, 0, 0, 0]
  - block: resume-experience
    id: experience
    content:
      username: admin
    design:
      # Hugo date format
      date_format: 'January 2006'
      # Education or Experience section first?
      is_education_first: false
      columns: 1
  - block: markdown
    id: awards
    content:
      title: Awards
      # subtitle: A subtitle
      text: |-
        - Comprehensive Excellence Scholarship, Tsinghua 2024/2023
        - Outstanding Graduate Award of Beijing (4%) 2022
        - Merit Student of Beijing (1%) 2021
        - Meritorious Winner in Interdisciplinary Contest In Modeling 2020
    design:
      spacing:
        # Customize the section spacing. Order is top, right, bottom, left.
        padding: ['0', '0', '0', '0']
---
### Hi there! 👋 
🎓 I am a third-year master's student at SIGS, Tsinghua University, co-advised by Prof. [Wenwu Zhu](https://www.cs.tsinghua.edu.cn/csen/info/1306/4336.htm), Prof. [Xin Wang](https://mn.cs.tsinghua.edu.cn/xinwang/), and Prof. [Yang Li](http://yangli-feasibility.com/home/). 

💡 I have broad research interests in **Graph Machine Learning**, **Causal Inference**, their intersections with **Large Language Models**, and **AI4Science** applications (especially in Drug Combination and Biomedicine).

#### I am actively seeking a PhD position starting in Fall 2025. If you believe I would be a good fit for your group, please feel free to contact me~
