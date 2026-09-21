---
title: 'SliveredChain: Reducing Storage in Private Blockchain Systems Using Fault-Tolerant Overlay of Non-Overlapping Shards'

# Authors
# If you created a profile for a user (e.g. the default `admin` user), write the username (folder name) here
# and it will be replaced with their full name and linked to their profile.
authors:
  - admin
  - Soumit Saha
  - Touhidul Islam
  - Muhammad Abdullah Adnan

date: '2021-05-30T00:00:00Z'

# Schedule page publish date (NOT publication's date).
publishDate: '2021-05-30T00:00:00Z'

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ['3']

# Publication name and optional abbreviated publication name.
publication: Undergraduate thesis, BUET
publication_short: ''

abstract: The high storage requirement problem in blockchains is one of the few limitations that can hinder the technology from reaching its maximum potential. The space that we need to store the data in blockchains, either public or private, is growing exponentially and thus, hindering its adoption in data-heavy applications. In this study, we propose SliveredChain, a system designed to reduce the space required at each node of a private blockchain network. We plan to achieve the above by partitioning the chain into some non-overlapping shards, make a certain number of copies of each shard, and then store the shards across all the nodes more or less uniformly. This strategy ensures both reduced storage requirement at each node and fault tolerance in case one or more nodes in the network get disconnected. In SliveredChain, we devise an efficient way to distribute the shards among the nodes in the network. After that, we show that any typical blockchain operation like new block addition or querying the ledger can be done even when no single node has the entire blockchain. Finally, we conduct an extensive experiment on SliveredChain using Azure Cloud Services. Our evaluation shows that SliveredChain significantly reduces (up to 90.36%) the storage requirement at each node and scales very well with the addition of new nodes in the network.

# Summary. An optional shortened abstract.
summary: A fault-tolerant approach to sharding a private blockchain so that no node has to store the entire chain.

tags:
  - Blockchain
  - Distributed Systems

# Display this page in the Featured widget?
featured: false

url_pdf: ''
url_code: 'https://github.com/mahbub-hr/ShardedBlockchain'
url_dataset: ''
url_poster: ''
url_project: ''
url_slides: ''
url_source: ''
url_video: ''

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
image:
  caption: 'Reducing storage by sharding the chain'
  focal_point: 'Center'
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
projects:
  - sliveredchain-a-storage-optimized-blockchain
---
