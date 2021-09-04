+++
title = "SliveredChain: Reducing Storage in Private Blockchain Systems Using Fault-Tolerant Overlay of Non-Overlapping Shards"

# Date first published.
date = "2021-05-30"

# Authors. Comma separated list, e.g. `["Bob Smith", "David Jones"]`.
authors = ["MD Mahbub Hossain Raton", "Soumit Saha", "Touhidul Islam", "Muhammad Abdullah Adnan"]

# Publication type.
# Legend:
# 0 = Uncategorized
# 1 = Conference proceedings
# 2 = Journal
# 3 = Work in progress
# 4 = Technical report
# 5 = Book
# 6 = Book chapter
publication_types = ["2"]

# Publication name and optional abbreviated version.
publication = "[In Progress]"
# publication_short = "In Elsevier"

# Abstract and optional shortened version.
abstract = "The high storage requirement problem in blockchains is one of the few limitations that can hinder the technology from reaching its maximum potential. The space that we need to store the data in blockchains, either public or private, is growing exponentially and thus, hindering its adoption in data-heavy applications. In this study, we propose SliveredChain, a system designed to reduce the space required at each node of a private blockchain network. We plan to achieve the above by partitioning the chain into some non-overlapping shards, make a certain number of copies of each shard, and then store the shards across all the nodes more or less uniformly. This strategy ensures both reduced storage requirement at each node and fault tolerance in case one or more nodes in the network get disconnected. In SliveredChain, we devise an efficient way to distribute the shards among the nodes in the network. After that, we show that any typical blockchain operation like new block addition or querying the ledger can be done even when no single node has the entire blockchain. Finally, we conduct an extensive experiment on SliveredChain using Azure Cloud Services. Our evaluation shows that SliveredChain significantly reduces (up to 90.36%) the storage requirement at each node and scales very well with the addition of new nodes in the network."

abstract_short = "A Fault Tolerant Approach of Sharding Blockchain to Reduce Storage Requirements."

# Featured image thumbnail (optional)
image_preview = "featured.jpg"

# Is this a selected publication? (true/false)
selected = false

# Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter the filename (excluding '.md') of your project file in `content/project/`.
#   E.g. `projects = ["deep-learning"]` references `content/project/deep-learning.md`.
projects = []

# Links (optional).
url_pdf = ""
url_preprint = ""
url_code = "https://github.com/mahbub-hr/ShardedBlockchain"
url_dataset = ""
url_project = ""
url_slides = ""
url_video = ""
url_poster = ""
url_source = ""


# Custom links (optional).
#   Uncomment line below to enable. For multiple links, use the form `[{...}, {...}, {...}]`.
#url_custom = [{name = "ac", url = "http://example.org"}]
      


# Does the content use math formatting?
math = true

# Does the content use source code highlighting?
highlight = true

# Featured image
# Place your image in the `static/img/` folder and reference its filename below, e.g. `image = "example.jpg"`.
[header]
image = ""
caption = ""
+++