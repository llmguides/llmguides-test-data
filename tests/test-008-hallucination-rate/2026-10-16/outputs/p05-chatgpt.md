Here are three peer-reviewed research papers published after 2023 (2024–2025) that investigate the effectiveness of Retrieval-Augmented Generation (RAG) in reducing hallucinations in large language models (LLMs).

The references include complete author lists, publication venues, years, and verified DOIs, along with brief summaries of their findings.

## 1. Béchard & Marquez Ayala (2024)

Full title: Reducing hallucination in structured outputs via Retrieval-Augmented Generation

Authors: Patrice Béchard and Orlando Marquez Ayala

Year: 2024

Conference: Proceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (NAACL 2024), Volume 6: Industry Track

Pages: 228–238

DOI: [10.18653/v1/2024.naacl-industry.19](https://doi.org/10.18653/v1/2024.naacl-industry.19?utm_source=chatgpt.com)

Key findings: The researchers evaluated a RAG-based system for generating structured workflows from natural-language requirements. Their experiments found that incorporating retrieval significantly reduced hallucinations and improved generalization to out-of-domain tasks. They also demonstrated that a smaller LLM paired with an effective retriever could maintain performance.

Relevance: Provides direct experimental evidence that RAG can reduce hallucinations in structured LLM outputs.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://aclanthology.org\&sz=32)

ACL Anthology



## 2. Hu et al. (2025)

Full title: Removal of Hallucination on Hallucination: Debate-Augmented RAG

Authors: Wentao Hu, Wengyu Zhang, Yiyang Jiang, Chen Jason Zhang, Xiao-Yong Wei, and Li Qing

Year: 2025

Conference: Proceedings of the 63rd Annual Meeting of the Association for Computational Linguistics (ACL 2025), Volume 1: Long Papers

Pages: 15839–15853

DOI: [10.18653/v1/2025.acl-long.770](https://doi.org/10.18653/v1/2025.acl-long.770?utm_source=chatgpt.com)

Key findings: This study introduced Debate-Augmented RAG (DRAG), which uses multi-agent debate to improve both retrieval quality and generated responses. Experiments across multiple tasks showed improved factual accuracy and reduced hallucinations caused by erroneous or biased retrieved information.

Relevance: Demonstrates that improving retrieval reliability and evidence evaluation can further reduce hallucinations beyond conventional RAG approaches.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://aclanthology.org\&sz=32)

ACL Anthology



## 3. Xu et al. (2025)

Full title: MEGA-RAG: a retrieval-augmented generation framework with multi-evidence guided answer refinement for mitigating hallucinations of LLMs in public health

Authors: Shan Xu, Zhaokun Yan, Chengxiao Dai, and Fan Wu

Year: 2025

Journal: Frontiers in Public Health, Volume 13, Article 1635381

DOI: [10.3389/fpubh.2025.1635381](https://doi.org/10.3389/fpubh.2025.1635381?utm_source=chatgpt.com)

Key findings: This study introduced MEGA-RAG, combining multiple retrieval methods, biomedical knowledge graphs, evidence reranking, and answer refinement. The researchers reported a reduction in hallucination rates of more than 40% compared with the evaluated baselines, which included a standalone LLM and standard RAG. Their approach achieved an accuracy of 0.7913 and an F1 score of 0.7904.

Relevance: Provides quantitative evidence that an enhanced RAG architecture can substantially mitigate hallucinations in domain-specific public health applications.&#x20;

[image](https://www.google.com/s2/favicons?domain=https://www.frontiersin.org\&sz=32)

Frontiers

+2



## Overall conclusion

Taken together, these three papers support the conclusion that RAG can reduce LLM hallucinations, particularly when external evidence is relevant, reliable, and effectively incorporated into generation.

They also illustrate an important distinction: conventional RAG can improve factual grounding, while enhanced architectures such as DRAG and MEGA-RAG aim to address hallucinations that persist even after retrieval. These results are specific to the evaluated systems and tasks, rather than a guarantee that RAG eliminates hallucinations universally.
