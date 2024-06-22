---
title: Causal-Aware Graph Neural Architecture Search under Distribution Shifts
authors:
- admin
- Xin Wang
- Zeyang Zhang
- Yijian Qin
- Ziwei Zhang
- Jialong Wang
- Yang Li
- Wenwu Zhu
date: '2024-05-26'
publishDate: '2024-06-22T15:43:42.309742Z'
publication_types:
- manuscript
publication: '*arXiv*'
abstract: 'Graph neural architecture search (Graph NAS) has emerged as a promising
  approach for autonomously designing graph neural network architectures by leveraging
  the correlations between graphs and architectures. However, the existing methods
  fail to generalize under distribution shifts that are ubiquitous in real-world graph
  scenarios, mainly because the graph-architecture correlations they exploit might
  be spurious and varying across distributions. In this paper, we propose to handle
  the distribution shifts in the graph architecture search process by discovering
  and exploiting the causal relationship between graphs and architectures to search
  for the optimal architectures that can generalize under distribution shifts. The
  problem remains unexplored with the following critical challenges: 1) how to discover
  the causal graph-architecture relationship that has stable predictive abilities
  across distributions, 2) how to handle distribution shifts with the discovered causal
  graph-architecture relationship to search the generalized graph architectures. To
  address these challenges, we propose a novel approach, Causal-aware Graph Neural
  Architecture Search (CARNAS), which is able to capture the causal graph-architecture
  relationship during the architecture search process and discover the generalized
  graph architecture under distribution shifts. Specifically, we propose Disentangled
  Causal Subgraph Identification to capture the causal subgraphs that have stable
  prediction abilities across distributions. Then, we propose Graph Embedding Intervention
  to intervene on causal subgraphs within the latent space, ensuring that these subgraphs
  encapsulate essential features for prediction while excluding non-causal elements.
  Additionally, we propose Invariant Architecture Customization to reinforce the causal
  invariant nature of the causal subgraphs, which are utilized to tailor generalized
  graph architectures. Extensive experiments on synthetic and real-world datasets
  demonstrate that our proposed CARNAS achieves advanced out-of-distribution generalization
  ability by discovering the causal relationship between graphs and architectures
  during the search process.'
topics:
# - Computer Science - Artificial Intelligence
# - Computer Science - Machine Learning
- Graph Machine Learning
links:
- name: URL
  url: http://arxiv.org/abs/2405.16489
  
url_pdf: 'https://arxiv.org/pdf/2405.16489'
# url_code: 'https://github.com/HugoBlox/hugo-blox-builder'
# url_dataset: 'https://github.com/HugoBlox/hugo-blox-builder'
# url_poster: ''
# url_project: ''
# url_slides: ''
# url_source: 'https://github.com/HugoBlox/hugo-blox-builder'
# url_video: 'https://youtube.com'

featured: true

# Summary. An optional shortened abstract.
summary: 'We propose to handle the distribution shifts in the graph architecture search process by discovering and exploiting the causal relationship between graphs and architectures to search for the optimal architectures that can generalize under distribution shifts.'
---
