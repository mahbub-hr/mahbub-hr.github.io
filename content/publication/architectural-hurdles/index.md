---
title: 'Architectural Hurdles: Exploring the Difficulties of x86-to-ARM Binary Cross-Compilation'

# Authors
# A YAML list of author names.
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Michael Franz

# Author notes (optional)
author_notes: []

date: '2025-06-01T00:00:00Z'

# Schedule page publish date (NOT publication's date).
publishDate: '2025-06-01T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['3']

# Publication name and optional abbreviated publication name.
publication: Manuscript in preparation
publication_short: ''

abstract: Recompiling a program for a different instruction set architecture without access to its source is a long-standing goal of binary analysis, and one that repeatedly runs aground on details the source language never exposed. We report on extending a dynamic binary lifting framework to translate x86 binaries to AArch64 by way of LLVM IR, and on the architectural mismatches that make the translation hard in practice — calling-convention divergence, the absence of size information for pointer arguments at library boundaries, and the gap between recorded dynamic execution and the paths a recompiled binary may actually take. We validate the resulting pipeline on real-world SPEC CPU 2017 programs.

# Summary. An optional shortened abstract.
summary: On the architectural mismatches that make source-free x86-to-AArch64 recompilation hard, and a lifting pipeline validated on SPEC CPU 2017.

tags:
  - Compilers
  - Binary Translation
  - LLVM

# Display this page in the Featured widget?
# Keep false: the Featured widget is disabled and `publications.md` sets
# exclude_featured, so a featured publication would render nowhere.
featured: false

# Custom links (uncomment lines below)
# links:
# - name: Custom Link
#   url: http://example.org

url_pdf: ''
url_code: ''
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
projects:
  - cross-compiling-x86-binaries-to-arm
---
