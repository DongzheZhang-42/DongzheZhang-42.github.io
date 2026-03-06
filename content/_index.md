---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026-01-05
type: landing

design:
  # Default section spacing
  spacing: '0'

sections:
  # Developer Hero - Gradient background with name, role, social, and CTAs
  - block: dev-hero
    id: hero
    content:
      username: me
      greeting: "Hi, I'm"
      show_status: true
      show_scroll_indicator: false
      typewriter:
        enable: true
        prefix: "I work on"
        strings:
          - "audio deep learning"
          - "microphone array processing"
          - "sound source localization"
          - "speech enhancement"
          - "embedded and edge AI deployment"
        type_speed: 70
        delete_speed: 40
        pause_time: 2500
      cta_buttons:
        - text: View My Work
          url: "#projects"
          icon: arrow-down
        - text: Get In Touch
          url: "#contact"
          icon: envelope
    design:
      style: centered
      avatar_shape: circle
      animations: true
      background:
        image:
          filename: hero-bg.jpg
        filters:
          brightness: 0.35
        color:
          light: "#fafafa"
          dark: "#0a0a0f"
      spacing:
        padding: ["6rem", "0", "4rem", "0"]
  
  # Filterable Portfolio - Alpine.js powered project filtering
  - block: portfolio
    id: projects
    content:
      title: "Featured Projects"
      subtitle: "A selection of my recent work"
      count: 0
      sort_by: "Weight"
      sort_ascending: true
      filters:
        folders:
          - projects
      buttons:
        - name: All
          tag: '*'
        - name: Speech Enhancement
          tag: Speech Enhancement
        - name: Distributed SELD
          tag: Distributed SELD
        - name: Acoustic Camera
          tag: Acoustic Camera
        - name: Edge UGS
          tag: Edge UGS
      default_button_index: 0
      # Archive link auto-shown if more projects exist than 'count' above
      # archive:
      #   enable: false  # Set to false to explicitly hide
      #   text: "Browse All"  # Customize text
      #   link: "/work/"  # Custom URL
    design:
      columns: 3
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # hidden-section: tech-stack
  # Visual Tech Stack - Icons organized by category (hidden)
  # - block: tech-stack
  #   id: skills
  #   content:
  #     title: "Tech Stack"
  #     subtitle: "Technologies I use to build things"
  #     categories:
  #       - name: Languages
  #         items:
  #           - name: TypeScript
  #             icon: devicon/typescript
  #           - name: JavaScript
  #             icon: devicon/javascript
  #           - name: Python
  #             icon: devicon/python
  #           - name: Go
  #             icon: devicon/go
  #       - name: Frontend
  #         items:
  #           - name: React
  #             icon: devicon/react
  #           - name: Next.js
  #             icon: devicon/nextjs
  #           - name: Tailwind CSS
  #             icon: devicon/tailwindcss
  #           - name: Alpine.js
  #             icon: devicon/alpinejs
  #       - name: Backend
  #         items:
  #           - name: Node.js
  #             icon: devicon/nodejs
  #           - name: Express
  #             icon: devicon/express
  #           - name: PostgreSQL
  #             icon: devicon/postgresql
  #           - name: Redis
  #             icon: devicon/redis
  #       - name: DevOps
  #         items:
  #           - name: Docker
  #             icon: devicon/docker
  #           - name: AWS
  #             icon: devicon/amazonwebservices-wordmark
  #           - name: GitHub Actions
  #             icon: brands/github
  #           - name: Vercel
  #             icon: devicon/vercel
  #   design:
  #     style: grid
  #     show_levels: false
  #     background:
  #       color:
  #         light: "#f5f5f5"
  #         dark: "#08080c"
  #     spacing:
  #       padding: ["4rem", "0", "4rem", "0"]
  
  # Experience Timeline
  - block: resume-experience
    id: experience
    content:
      title: Experience
      date_format: Jan 2006
      items:
        - title: Senior Software Engineer
          company: Tech Corp
          company_url: ''
          company_logo: ''
          location: San Francisco, CA
          date_start: '2023-01-01'
          date_end: ''
          description: |2-
            * Lead development of microservices architecture serving 1M+ users
            * Improved API response time by 40% through optimization
            * Mentored team of 5 junior developers
            * Tech stack: React, Node.js, PostgreSQL, AWS
        - title: Full-Stack Developer
          company: Startup Inc
          company_url: ''
          company_logo: ''
          location: Remote
          date_start: '2021-06-01'
          date_end: '2022-12-31'
          description: |2-
            * Built and deployed 3 production applications from scratch
            * Implemented CI/CD pipeline reducing deployment time by 60%
            * Collaborated with design team on UI/UX improvements
            * Tech stack: Next.js, Express, MongoDB, Docker
        - title: Junior Developer
          company: Web Agency
          company_url: ''
          company_logo: ''
          location: New York, NY
          date_start: '2020-01-01'
          date_end: '2021-05-31'
          description: |2-
            * Developed client websites using modern web technologies
            * Maintained and updated legacy codebases
            * Participated in code reviews and agile ceremonies
            * Tech stack: React, WordPress, PHP, MySQL
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]

  # Research Highlights: Publications, Patents, Competitions
  - block: markdown
    id: achievements
    content:
      title: Research Highlights
      subtitle: Publications, Patents, and Competitions
      text: |-
        <style>
          #hero {
            isolation: isolate;
          }
          #hero .home-section-bg {
            position: absolute !important;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: 0 !important;
            background-image: url('/uploads/hero-bg.jpg') !important;
            background-position: center 58% !important;
            background-size: cover !important;
            background-repeat: no-repeat !important;
            filter: saturate(0.94) contrast(1.02) brightness(0.96);
          }
          #hero .home-section-bg.parallax {
            background-attachment: scroll !important;
          }
          #hero .home-section-bg[style*="--dark-bg-color"] {
            background-color: transparent !important;
          }
          #hero .home-section-bg::after {
            content: "";
            position: absolute;
            inset: 0;
            background: linear-gradient(
              180deg,
              rgba(2, 6, 23, 0.20) 0%,
              rgba(2, 6, 23, 0.30) 45%,
              rgba(2, 6, 23, 0.44) 100%
            );
            pointer-events: none;
          }
          #hero .relative.z-10.mx-auto.max-w-5xl {
            position: relative;
            z-index: 2;
            background: rgba(2, 6, 23, 0.24);
            border: 1px solid rgba(148, 163, 184, 0.22);
            border-radius: 1.2rem;
            backdrop-filter: blur(2.5px);
            box-shadow: 0 18px 40px rgba(2, 6, 23, 0.30);
            padding-top: 2.6rem;
            padding-bottom: 2.3rem;
          }
          #hero h1 span {
            background: none !important;
            color: #f8fafc !important;
            -webkit-text-fill-color: #f8fafc !important;
          }
          #hero p {
            color: rgba(241, 245, 249, 0.96) !important;
            text-shadow: 0 2px 14px rgba(0, 0, 0, 0.45);
          }
          #hero [x-data*="typewriter"],
          #hero .typewriter-cursor {
            color: #7dd3fc !important;
          }
          #hero a[href*="linkedin.com"],
          #hero a[href*="scholar.google"] {
            background: rgba(2, 6, 23, 0.72) !important;
            border: 1px solid rgba(125, 211, 252, 0.42) !important;
            box-shadow: 0 6px 20px rgba(2, 6, 23, 0.45);
          }
          #hero a[href*="linkedin.com"]:hover,
          #hero a[href*="scholar.google"]:hover {
            background: rgba(15, 23, 42, 0.88) !important;
            border-color: rgba(125, 211, 252, 0.62) !important;
            transform: translateY(-1px);
          }
          #hero a[href="#contact"] {
            background: rgba(2, 6, 23, 0.72) !important;
            border: 1px solid rgba(226, 232, 240, 0.38) !important;
            color: #f1f5f9 !important;
            box-shadow: 0 8px 22px rgba(2, 6, 23, 0.42);
          }
          #hero a[href="#contact"]:hover {
            background: rgba(15, 23, 42, 0.9) !important;
            border-color: rgba(226, 232, 240, 0.56) !important;
          }
          #hero .relative.z-10.mx-auto.max-w-5xl > p:nth-of-type(n+3):nth-of-type(-n+6) {
            font-size: 1.03rem;
            line-height: 1.55;
            letter-spacing: 0.005em;
          }
          @media (max-width: 768px) {
            #hero .relative.z-10.mx-auto.max-w-5xl > p:nth-of-type(n+3):nth-of-type(-n+6) {
              font-size: 0.95rem;
              line-height: 1.5;
            }
          }
          #hero h1,
          #hero p {
            text-shadow: 0 2px 14px rgba(0, 0, 0, 0.45);
          }
          #achievements .flex.flex-col.items-center.max-w-prose {
            max-width: min(1200px, 95vw) !important;
            width: 100%;
          }
          #achievements .prose {
            max-width: 100% !important;
          }
        </style>

        ### Publications

        - Zhang D, Chen J, Wang M, Mezza A I, et al. **On the Design of Efficient Neural Methods for Geometry-Agnostic Multichannel Speech Enhancement**. *IEEE ICASSP 2026* (accepted).
        - Zhang D, Chen J, Wang M, et al. **Co-designing Eigenbeam and Multi-order Encoder for Geometry-Agnostic Speech Enhancement**. *IEEE ICASSP 2026* (accepted).
        - Zhang D, Chen J, Bai J, et al. **Sound Event Localization and Classification using Wireless Acoustic Sensor Networks in Outdoor Environments**. *IEEE Sensors Journal*, 2025.
        - Zhang D, Chen J, Bai J, et al. **Multiple sound sources localization using sub-band spatial features and attention mechanism**. *Circuits, Systems, and Signal Processing*, 2025, 44(4): 2592-2620.
        - Zhang D, Chen J, Huang S, et al. **Synthesis-to-real robust training for enhanced sound event localization and detection using dynamic kernel convolution networks**. *Applied Acoustics*, 2025, 228: 110267.
        - Zhang D, Chen J, Bai J, et al. **DOA-based multi-node geometry calibration for wireless acoustic sensor network**. *IEEE ICSPCC*, 2023.
        - Zhang D, Bai J, Chen J. **JLESS submission to DCASE 2024 Task10: An acoustic-based traffic monitoring solution**. *DCASE 2024 Challenge Technical Report*, 2024.
        - Zhang D, Bai J, Chen J. **JLESS submission to DCASE2023 Task3: Conformer with data augmentation for SELD in real space**. *DCASE 2023 Challenge Technical Report*, 2023.
        - Sun W, Zhang D, Bai J, et al. **JLESS Submission to DCASE2024 Task3: Conformer with Data Augmentation for SELD with Source Distance Estimation**. *DCASE 2024 Challenge Technical Report*, 2024.
        - Han Y, Chen J, Zhang D. **Passive homing method with reinforcement learning for a single hydrophone**. *Acta Acustica*, 2025, 50(1): 59-67.
        - Li X, Chen J, Bai J, et al. **Deep learning-based DOA estimation using CRNN for underwater acoustic arrays**. *Frontiers in Marine Science*, 2022, 9: 1027830.
        - Niu Q, Shi W, Zhang Q, et al. **Underwater Passive Sonar Fusion Detection Based on Sensor Bias Estimation and Classification**. *Digital Signal Processing*, 2025: 105596.
        - Bai J, Wang M, Liu H, et al. **Description on IEEE ICME 2024 grand challenge: Semi-supervised acoustic scene classification under domain shift**. *arXiv preprint:2402.02694*, 2024.

        ### Patents

        - **Air sonar array device for acousto-optic linkage monitoring and positioning** (CN218003722U, Active)
        - **Wireless low-power consumption ground defense monitoring devices** (CN218511891U, Active)
        - **Pipeline gas leakage amount detection method** (CN117515432A, Pending)
        - **A passive tracking method and device for an underwater target** (CN116430370A, Pending)

        ### Competitions

        - **2nd Place**, DCASE 2024 Challenge Task 10 (Acoustic-Based Traffic Monitoring)
        - **Rank 6**, DCASE 2023 Challenge Task 3 (Sound Event Localization and Detection in Real Spatial Sound Scenes)
        - **Gold Award**, China International "Internet+" College Students' Innovation and Entrepreneurship Competition, 2021
    design:
      columns: "1"
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # hidden-section: recent-posts
  # Recent Blog Posts (hidden)
  # - block: collection
  #   id: blog
  #   content:
  #     title: Recent Posts
  #     subtitle: 'Thoughts on web development, tech, and more'
  #     text: ''
  #     filters:
  #       folders:
  #         - blog
  #       exclude_featured: false
  #     count: 3
  #     order: desc
  #   design:
  #     view: card
  #     columns: 3
  #     background:
  #       color:
  #         light: "#f5f5f5"
  #         dark: "#08080c"
  #     spacing:
  #       padding: ["4rem", "0", "4rem", "0"]
  
  # Contact Section
  - block: contact-info
    id: contact
    content:
      title: Get In Touch
      subtitle: "Let's build something amazing together"
      text: |-
        I'm always interested in hearing about new projects and opportunities.
        Whether you're looking to hire, collaborate, or just want to say hi, feel free to reach out!
      email: "dongzhe.zhang [at] polimi [dot] it"
      autolink: false
    design:
      columns: '1'
      background:
        color:
          light: "#ffffff"
          dark: "#0d0d12"
      spacing:
        padding: ["4rem", "0", "4rem", "0"]
  
  # CTA Card
  - block: cta-card
    content:
      title: "Open to Opportunities"
      text: |-
        I'm currently looking for **senior engineering** or **tech lead** roles.
        
        Let's connect and discuss how I can help your team.
    design:
      card:
        # Light mode: soft pastel theme gradient | Dark mode: rich deep gradient
        css_class: 'bg-gradient-to-br from-primary-200 via-primary-100 to-secondary-200 dark:from-primary-600 dark:via-primary-700 dark:to-secondary-700'
        text_color: dark
      background:
        color:
          light: "#f5f5f5"
          dark: "#08080c"
      spacing:
        padding: ["4rem", "0", "6rem", "0"]
---
