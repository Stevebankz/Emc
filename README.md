# The Brittleness of Transformer Feature Fusion: A Comparative Study of Model Robustness in Engineering Misinformation Detection

This repository contains the official code and data for the paper:

**"The Brittleness of Transformer Feature Fusion: A Comparative Study of Model Robustness in Engineering Misinformation Detection"**

Our work provides a comprehensive benchmark and critical analysis of different machine learning paradigms for identifying misinformation in safety-critical engineering documents.

---

## 📝 Abstract

In engineering disciplines, where information integrity is paramount to safety and reliability, the proliferation of AI-generated and user-contributed content presents a critical risk.  
This paper conducts a comprehensive comparative study to evaluate the efficacy and robustness of different machine learning paradigms for detecting misinformation in technical documents.

We introduce the **Engineering Misinformation Corpus (EMC)**, a novel, large-scale multilingual benchmark curated from aerospace, energy, and civil infrastructure domains. We systematically compare the performance of a feature-engineered XGBoost model with an end-to-end XLM-RoBERTa Transformer.

**Key insights:**
- Transformers can implicitly learn complex signals that typically require manual feature engineering.
- Fused models (Transformer + engineered features) are *brittle* under semantic adversarial attacks, collapsing in performance.
- Simpler models (XLM-R only or XGBoost only) show greater robustness in adversarial settings.

This work offers both practical tools and conceptual insights for deploying NLP models in high-stakes engineering domains.

---

## 🚀 Key Contributions

- **🗃 A Novel Benchmark Dataset**: The **Engineering Misinformation Corpus (EMC)** – a multilingual, domain-rich dataset with over 19,000 documents across English, German, French, and Spanish.
- **📊 A Reproducible Benchmark**: Direct empirical comparison of traditional feature-engineered models and end-to-end Transformer models.
- **🤖 Transformer Capability Analysis**: Demonstrates Transformers' ability to capture trust-oriented features without explicit engineering.
- **🧪 Robustness Testing**: Reveals the brittleness of naively fused models under semantic attacks using adversarial perturbation techniques.

---

## 📂 The Engineering Misinformation Corpus (EMC)

The **EMC** is composed of curated texts from:
- **Authoritative sources**: NIST, FAA
- **Community forums**: Reddit, Eng-Tips
- **Generated content**: LLMs (GPT-3.5, Claude, etc.)

You can download the dataset from the Hugging Face Hub:  
👉 [https://huggingface.co/datasets/YOUR_USERNAME/EMC](https://huggingface.co/datasets/stevebankz/Emc)

---

## 💾 Trained Models

Final trained models from our study are hosted on the Hugging Face Hub:

- `XLM-RoBERTa Only` (baseline)
- `XLM-R + Simple Fusion`
- `XLM-R + Gated Fusion`

👉 [https://huggingface.co/YOUR_USERNAME](https://huggingface.co/stevebankz)

---

## 🔁 Reproducing the Results

### 🔧 Setup

```bash
git clone https://github.com/YOUR_USERNAME/your-repo-name.git
cd your-repo-name

python -m venv .venv
source .venv/bin/activate         # On Windows use: .venv\Scripts\activate

pip install -r requirements.txt
