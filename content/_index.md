---
title: 'SEISAD Team'
date: 2024-01-01
type: landing

design:
  spacing: "6rem"

sections:
  # 1. Hero
  - block: hero
    content:
      title: SEISAD Team
      text: |
        **Surface, Electrochemistry, Imaging and Surface Analytical Design**  
        Part of Chimie ParisTech - PSL University. We focus on advancing the understanding of electrochemical interfaces and material science.
      primary_action:
        text: Our Publications
        url: /publication/
        icon: book-open
      secondary_action:
        text: Join Us
        url: "/#contact"
      announcement:
        text: "📢 We are looking for new PhD students and Postdocs! Click here to learn more."
        link:
          text: "Open Positions"
          url: "/#contact"
    design:
      background:
        filename: "AA3A0511.JPG"
        filters:
          brightness: 0.7
      spacing:
        padding: ["4rem", 0, "4rem", 0]

  # 2. Stats
  - block: stats
    content:
      title: Lab at a Glance
      items:
        - statistic: "20+"
          description: "Team Members"
        - statistic: "100+"
          description: "Publications"
        - statistic: "PSL"
          description: "University"
    design:
      css_class: "bg-gray-100 dark:bg-gray-800"
      spacing:
        padding: ["2rem", 0, "2rem", 0]

  # 3. Research Axes
  - block: features
    id: research
    content:
      title: Research Axes
      text: Our team investigates the complexity of chemical systems through multiple scales.
      items:
        - name: Surface Analysis
          icon: microscope
          description: Using advanced imaging techniques to characterize interfaces at the nanoscale.
        - name: Electrochemistry
          icon: bolt
          description: Studying charge transfer and fundamental electrochemical reactions.
        - name: Material Design
          icon: flask
          description: Developing new materials for sustainable energy and industrial applications.
        - name: Corrosion Science
          icon: shield-check
          description: Protecting infrastructure through innovative surface treatments.

  # 4. CTA
  - block: cta-card
    content:
      title: "Join our Research"
      text: "We are always looking for passionate researchers to join SEISAD. If you are interested in our work, please get in touch."
      button:
        text: Contact Us
        url: "mailto:your-email@chimieparistech.psl.eu"
    design:
      card:
        # 这里可以选择卡片的背景色
        css_class: "bg-primary-500"
---
