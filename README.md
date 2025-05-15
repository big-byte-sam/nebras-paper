# Nebras: A Generic Multi-domain Agentic RAG-based Arabic Question Answering System

This repository supports the research paper:

**Title:** *Nebras: A Generic Multi-domain Agentic RAG-based Arabic Question Answering System*  
**Authors:** [Your Name(s)]  
**Preprint / DOI:** *Coming soon*  
**Journal Submission:** *[To Be Determined]*

---

## 📄 Abstract

This paper introduces **Nebras**, a generic multi-domain Arabic question answering (QA) system built on a Retrieval-Augmented Generation (RAG) framework with a hybrid retrieval strategy. Nebras addresses persistent challenges in QA, including hallucination and domain-specific reasoning, particularly in Arabic, a morphologically rich and under-resourced language. By orchestrating specialized agents within an Agentic RAG pipeline, Nebras dynamically optimizes each processing stage while leveraging pre-trained large language models without additional fine-tuning, promoting scalability and efficiency.

The system's architecture supports easy extension to new domains through lightweight data integration guidelines. Experiments on two domains—Islamic fatwas (legal opinions by religious leaders) and university help-desk queries—demonstrate that Nebras generates factually accurate, contextually relevant answers and outperforms state-of-the-art models in both automatic metrics and human evaluation.

---

## 🎯 Purpose of the Repository

This repository shares all resources used in the paper, including:
- Preprocessing and agent prompts
- Human and automated evaluation results
- Generated responses across multiple models
- Retrieval experiment outputs

This is intended to support **transparency**, **reproducibility**, and **further research** on Arabic QA and agentic RAG architectures.

---

## 📁 Directory Structure

```bash
.
├── datasets-with-generated-responses
│   ├── arabic-academic-policies
│   │   ├── master_answers_llm_eval_{model_name}.csv   # Generated answers + reasoning LLM evaluation
│   │   └── evaluation_results.xlsx                     # Human + LLM evaluation (8 sheets, all models)
│   └── arabic-fatwa
│       ├── {model_name}_10q.csv                        # 10-question fatwa experiment
│       └── {model_name}_100q.csv                       # 100-question fatwa experiment
│
├── prompts
│   ├── agent-prompts
│   │   ├── text/                                       # Prompts in .txt format
│   │   └── markdown/                                   # Prompts in .md format
│   ├── evaluation-prompts
│   │   ├── text/
│   │   └── markdown/
│   └── pre-processing-prompts
│       ├── text/
│       └── markdown/
│
├── retriever-responses
│   ├── chunks
│   │   ├── with-ranking/
│   │   └── no-ranking/
│   └── pdr
│       ├── with-ranking/
│       └── no-ranking/


```Each file in retriever-responses is named with the pattern:
sim-{similarity_threshold}-k-{top_k_files}-{ranked_or_empty}_{similarity_matching_method}.csv
This naming makes the retriever configuration explicit and easily traceable.```

## 🧠 Key Contributions
- Agentic RAG Architecture: We propose a multi-agent RAG framework that enables modular orchestration of LLMs for Arabic QA tasks—without any additional fine-tuning.
- Hybrid Retrieval: A flexible retrieval system that combines dense and sparse methods, evaluated with and without document ranking.
- Multi-domain Evaluation: Experiments conducted on both fatwa and academic policy domains to validate robustness and adaptability.
- Human + Automated Evaluation: Answers are evaluated using reasoning-capable LLMs and human experts via structured rubrics.

## ✅ How to Use
- Simply browse the repository and explore the data and prompts:
- Review and reuse prompts for your own agentic QA pipelines
- Analyze model performance across dimensions (Coverage, Factuality, Clarity)
- Compare different retriever configurations using output files
- Explore both human and LLM-based evaluation results
- All files are self-contained and well-structured—no installation required.

## 🔐 License
This repository is licensed under the **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** License.

You are free to:

- **Share** — copy and redistribute the material in any medium or format
- **Adapt** — remix, transform, and build upon the material

Under the following terms:

- **Attribution** — You must give appropriate credit, provide a link to the license, and indicate if changes were made.
- **NonCommercial** — You may not use the material for commercial purposes.

For more details, see the [full license text](https://creativecommons.org/licenses/by-nc/4.0/).

## 📚 Citation
If you use any part of this work in your research, please cite:
```bibtex
@article{nebras2025,
  title = {Nebras: A Generic Multi-domain Agentic RAG-based Arabic Question Answering System},
  author = {Your Name},
  journal = {To Be Determined},
  year = {2025},
  note = {Preprint available at [Link to be added]}
}
```

## 🤝 Contact
For questions, collaborations, or feedback, feel free to reach out:
[Your Name]
Email: [your-email@example.com]
GitHub: [your-profile]

## 🌍 Acknowledgments
We thank the domain experts and evaluators who supported this research. Special thanks to contributors to the Arabic fatwa and academic datasets.

