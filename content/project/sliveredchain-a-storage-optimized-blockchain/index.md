---
title: "SliveredChain: A Storage Optimized Private Blockchain"
date: "2020-11-21T13:15:46.151Z"

# Optional external URL for project (replaces project detail page).
external_link: ""
#links:
#  - name: code
#    url: https://colab.research.google.com/drive/1-ENakRVTVx97rVX7TOxILdlzvQfxVpQF?usp=sharing
#    icon_pack: ai

# Featured image
# To use, place an image named `featured.jpg/png` in your page's folder.
# Placement options: 1 = Full column width, 2 = Out-set, 3 = Screen-width
# Focal point options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
# Set `preview_only` to `true` to just use the image for thumbnails.

placement: 1
caption: Reducing Storage by Sharding the Chain
focal_point: "Center"
preview_only: false
alt_text: Reducing Storage by Sharding the Chain

# url_code: "https://colab.research.google.com/drive/1-ENakRVTVx97rVX7TOxILdlzvQfxVpQF?usp=sharing"
---

<!--StartFragment-->
I completed this project as a part of my undergraduate thesis. This project aims to optimize storage usage of a [Private Blockchain](https://www.investopedia.com/news/public-private-permissioned-blockchains-compared/#toc-private-blockchain) system. Typically, each node in the system stores whole blockchain. This consumes a lot of storage. In my thesis, I propose to only store a part of the chain in each node. <!-- This means the number of copies of the chain in the system is equal to the number of nodes present in the system. --> This is done by carefully dividing the chain and distributing the pieces to each peer. As a proof of concept, I implemented this proposal in [Flask](https://flask.palletsprojects.com/en/2.2.x/) framework. Our experimental evaluation shows SliveredChain can reduce the required storage by 66.67%. Our method scales very well with the number of nodes in the network.

<!--EndFragment-->
