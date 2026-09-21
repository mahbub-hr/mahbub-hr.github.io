---
# Display name
title: Mahbub H. Raton

# Is this the primary user of the site?
superuser: true

# Role/position/tagline
role: PhD Student in Computer Science

# Organizations/Affiliations to show in About widget
organizations:
  - name: University of California, Irvine
    url: https://uci.edu/
  - name: Secure Systems and Software Lab
    url: https://ssllab.org/

# Short bio (displayed in user profile at end of posts)
bio: I work on compilers and computer architecture — making programs survive the hardware they run on.

# Interests to show in About widget
interests:
  - Compilers and LLVM
  - Computer Architecture
  - Systems Reliability and Fault Tolerance
  - Binary Translation

# Education to show in About widget
education:
  courses:
    - course: PhD in Computer Science
      institution: University of California, Irvine
      year: 2028 (expected)
    - course: MS in Computer Science
      institution: University of California, Irvine
      year: 2026
    - course: BSc in Computer Science and Engineering
      institution: Bangladesh University of Engineering and Technology (BUET)
      year: 2021

# Social/Academic Networking
social:
  - icon: envelope
    icon_pack: fas
    link: mailto:mahbub.mmhr@gmail.com
  - icon: linkedin
    icon_pack: fab
    link: https://www.linkedin.com/in/m-mahbub-hossain
  - icon: github
    icon_pack: fab
    link: https://github.com/mahbub-hr

# Enter email to display Gravatar (if Gravatar enabled in Config)
email: ''

# Highlight the author in author lists? (true/false)
highlight_name: false
---

I am a PhD student in Computer Science at the [University of California, Irvine](https://uci.edu), advised by [Prof. Michael Franz](https://www.michaelfranz.com/) in the [Secure Systems and Software Lab](https://ssllab.org).

My research sits between the compiler and the machine it targets. On one side, I build LLVM transformation passes that let a program detect transient hardware faults in itself — duplicating computation and checking it at the points where a corrupted value would otherwise escape into memory, a branch, or a call. On the other, I work on cross-architecture binary translation, lifting x86 binaries to LLVM IR and recompiling them for AArch64. Both lines of work lean on architectural simulation: I extended gem5 with register-file and L1 cache fault injection to measure how often silent data corruption actually happens, and what it costs to stop it.

Before Irvine, I was a Lecturer in Computer Science at [United International University](https://www.uiu.ac.bd) in Dhaka, teaching object-oriented programming and pattern recognition. Prior to that I built the backend of a nationwide high school admission system for Bangladesh's Ministry of Education, which processed applications from 1.3 million students. I completed my BSc in Computer Science and Engineering at [BUET](https://www.buet.ac.bd), where my undergraduate thesis — supervised by [Dr. Muhammad Abdullah Adnan](https://sites.google.com/site/abdullahadnan/home) — looked at reducing the storage footprint of private blockchains through sharding.

{{< icon name="download" pack="fas" >}} Download my {{< staticref "uploads/CV_Mahbub_Raton.pdf" "newtab" >}}CV{{< /staticref >}}.
