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

My research sits at the conjunction of compiler and the machine it targets. My primary focus right now is on mitigating silent data corruption in large scale datacenters - the kind of quiet but catastrophic errors caused by defective hardware or even random particle strikes. For that, I build LLVM transformation passes to insert checks into the program that let a program detect transient hardware faults in itself. This checking instructions ensure that a corrupted value never escape into memory, a branch, or a call. I test the resilience of the hardened program using fault injection experiments  accross differnt ISAs such as x86, Arm32, etc. To conduct fault injection experiments, I built a fault injection framework from the open source gem5 simulator. Those hands-on results are what drive my new mitigation strategies. Previously, I worked on cross-architecture binary translation, lifting legacy x86 binaries to LLVM IR and recompiling them for AArch64.

Before starting my PhD journey, I was a Lecturer in Computer Science at [United International University](https://www.uiu.ac.bd) in Dhaka. I taught several core programming lanugage courses including object-oriented programming and pattern recognition. Prior to that I built the backend of a nationwide high school admission system [Link to XI admission system](https://xiclassadmission.gov.bd/) for Bangladesh's Ministry of Education, which processed applications from 1.3 million students. I completed my BSc in Computer Science and Engineering at [CSE, BUET](https://cse.buet.ac.bd/). I conducted my undergraduate thesis on reducing blockchain storage overhead via sharding the ledger under [Dr. Muhammad Abdullah Adnan](https://sites.google.com/site/abdullahadnan/home).

<!-- {{< icon name="download" pack="fas" >}} Download my {{< staticref "uploads/CV_Mahbub_Raton.pdf" "newtab" >}}CV{{< /staticref >}}. -->
