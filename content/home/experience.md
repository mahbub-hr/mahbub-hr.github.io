---
# An instance of the Experience widget.
# Documentation: https://wowchemy.com/docs/page-builder/
widget: experience
active: true
# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 40

title: Experience
subtitle:

# Date format for experience
#   Refer to https://wowchemy.com/docs/customization/#date-format
date_format: Jan 2006

# Experiences.
#   Add/remove as many `experience` items below as you like.
#   Required fields are `title`, `company`, and `date_start`.
#   Leave `date_end` empty if it's your current employer.
#   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
experience:
  - title: Graduate Research Assistant
    company: Secure Systems and Software Lab, University of California, Irvine
    company_url: 'https://ssllab.org/'
    company_logo: ''
    location: Irvine, California
    date_start: '2023-09-01'
    date_end: ''
    description: |
      Doctoral research in compilers, computer architecture, and systems reliability, advised by Prof. Michael Franz.

      * Compiler-assisted detection of transient hardware errors via LLVM transformation passes.
      * Architectural fault injection in gem5 to quantify silent data corruption.
      * Cross-architecture (x86-to-AArch64) binary translation.

  - title: Graduate Teaching Assistant
    company: University of California, Irvine
    company_url: 'https://uci.edu/'
    company_logo: ''
    location: Irvine, California
    date_start: '2023-09-01'
    date_end: ''
    description: |
      Mentored 300+ students across 6 CS courses. Assisted instructors with grading and question design.

  - title: Lecturer in Computer Science
    company: United International University
    company_url: 'https://www.uiu.ac.bd/'
    company_logo: org-uiu
    location: United City, Madani Ave, Dhaka 1212
    date_start: '2021-12-01'
    date_end: '2023-07-01'
    description: |
      * Delivered lectures for Object Oriented Programming and Pattern Recognition (average class size: 45).
      * Co-advised senior thesis projects on Data Mining.
      * Collaborated on syllabus modernization.

  - title: Software Developer
    company: Banbeis, Ministry of Education
    company_url: ''
    company_logo: ''
    location: Dhaka, Bangladesh
    date_start: '2021-03-01'
    date_end: '2021-12-01'
    description: |
      Engineered the backend of a nationwide high school admission system serving 1.3 million applicants across 4 education boards.

      * Built the Spring Boot and Laravel services behind the production admission workflow.
      * Designed the schema and SQL Server stored procedures for post-deadline merit ranking and school migrations.
      * Diagnosed a `GC overhead limit exceeded` OutOfMemoryError in the 1.3M-applicant ranking query, resolving it by replacing entity-based retrieval with the JDBC API.
      * Exposed data via REST APIs secured with Keycloak (OAuth2), deployed through Jenkins CI/CD pipelines.

design:
  columns: '2'
---
