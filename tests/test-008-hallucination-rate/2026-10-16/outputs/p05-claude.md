I'll look these up and verify each citation detail, including the DOIs, against the source records.

Here are three peer-reviewed papers, each checked against its publisher or index record.

**1. Benchmarking Large Language Models in Retrieval-Augmented Generation**
- **Authors:** Jiawei Chen; Hongyu Lin; Xianpei Han; Le Sun
- **Year:** 2024
- **Venue:** Proceedings of the AAAI Conference on Artificial Intelligence, 38(16), 17754–17762
- **DOI:** 10.1609/aaai.v38i16.29728
- **Relevance:** The authors built a benchmark called RGB to test how well RAG helps LLMs. LLMs showed some robustness to noisy retrieved documents, but they still struggled with declining to answer when the documents lacked the answer, with combining information across documents, and with false information in the documents.

**2. Reducing hallucination in structured outputs via Retrieval-Augmented Generation**
- **Authors:** Patrice Béchard; Orlando Marquez Ayala (both at ServiceNow)
- **Year:** 2024
- **Venue:** Proceedings of the 2024 Conference of the North American Chapter of the Association for Computational Linguistics: Human Language Technologies (Volume 6: Industry Track), pages 228–238, Mexico City, Mexico
- **DOI:** 10.18653/v1/2024.naacl-industry.19
- **Relevance:** The authors report that their RAG system significantly reduced hallucination when generating structured workflows from natural-language requirements, and that it let the LLM generalize to out-of-domain settings.
- **Author order:** The arXiv version lists Béchard first, but the ACL Anthology citation lists Orlando Ayala and Patrice Bechard. Use the ACL Anthology order if you're citing the published proceedings.

**3. Hallucination-Free? Assessing the Reliability of Leading AI Legal Research Tools**
- **Authors:** Varun Magesh; Faiz Surani; Matthew Dahl; Mirac Suzgun; Christopher D. Manning; Daniel E. Ho
- **Year:** 2025
- **Venue:** Journal of Empirical Legal Studies, 2025; 22:216–242
- **DOI:** 10.1111/jels.12413
- **Relevance:** This is the most skeptical of the three. It is the first preregistered empirical evaluation of AI legal research tools, and it tests vendors' claims that RAG eliminates hallucinations. Hallucinations were lower than with GPT-4, but the RAG-based tools from LexisNexis and Thomson Reuters still hallucinated between 17% and 33% of the time.

Taken together, the three papers find that RAG reduces hallucinations but does not eliminate them.

I left out Zakka et al., "Almanac — Retrieval-Augmented Language Models for Clinical Medicine" (NEJM AI, 2024, DOI 10.1056/AIoa2300068). It is a strong clinical example, but it has about 22 authors and I couldn't verify the complete list. If you want it as a fourth paper, take the author list from the NEJM AI page.

Sources:
- [AAAI OJS – Chen et al.](https://ojs.aaai.org/index.php/AAAI/article/view/29728)
- [ACL Anthology – Béchard & Ayala](https://preview.aclanthology.org/setup/2024.naacl-industry.19)
- [arXiv – Béchard & Ayala](https://arxiv.org/abs/2404.08189v1)
- [Magesh et al., JELS PDF (Stanford)](https://nlp.stanford.edu/~manning/papers/Magesh-Hallucination%E2%80%90Free-2025.pdf)
- [LLRX summary of Magesh et al.](https://www.llrx.com/2026/04/hallucinations-by-west-lexis-ai/)
