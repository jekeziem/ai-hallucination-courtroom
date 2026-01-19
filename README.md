# ai-hallucination-courtroom
Interactive demonstration of LLM hallucination risks through simulated trials with multi-agent evaluation
# ⚖️ AI Hallucination Courtroom

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](YOUR_STREAMLIT_URL_HERE)

> An interactive demonstration of Large Language Model (LLM) hallucination risks through simulated courtroom trials with multi-agent evaluation frameworks.

![Demo Screenshot](assets/demo-screenshot.png)

---

## 🎯 Project Overview

**AI Hallucination Courtroom** is an educational tool that exposes the risks of AI-generated misinformation through an interactive three-agent system:

- **The Witness** (LLM Agent): Simulates an overconfident AI that hallucinates plausible-but-false information
- **The Prosecutor** (RAG-Enhanced LLM): Fact-checks testimony against verified ground truth databases
- **The Magistrate** (Evaluator LLM): Assesses factual accuracy and quantifies real-world harm potential

### Why This Matters

According to recent AI safety research, LLMs can confidently generate false information in **15-30% of responses** depending on the domain. This project demonstrates:

1. **Hallucination Detection**: How RAG-based systems can identify misinformation
2. **Harm Assessment**: Quantifying real-world risks (medical misinformation, legal errors, political disinformation)
3. **Transparency Design**: Making AI limitations visible to end users

---

## 🚀 Live Demo

**Try it here:** [Streamlit Cloud Demo](YOUR_URL_HERE)

**Or run locally:**

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/ai-hallucination-courtroom.git
cd ai-hallucination-courtroom

# Install dependencies
pip install -r requirements.txt

# Set your API key
export ANTHROPIC_API_KEY='your-key-here'

# Run the app
streamlit run app.py
```

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────┐
│                   USER INTERFACE                     │
│            (Streamlit Web Application)               │
└─────────────────┬───────────────────────────────────┘
                  │
        ┌─────────┴─────────┐
        │                   │
        ▼                   ▼
┌───────────────┐   ┌───────────────┐
│   WITNESS     │   │  GROUND TRUTH │
│   (Claude)    │   │   DATABASE    │
│ - Generates   │   │ - Medical     │
│   responses   │   │ - Legal       │
│ - Hallucinates│   │ - Political   │
└───────┬───────┘   └───────┬───────┘
        │                   │
        └─────────┬─────────┘
                  ▼
          ┌───────────────┐
          │  PROSECUTOR   │
          │   (Claude)    │
          │ - RAG lookup  │
          │ - Cross-exam  │
          └───────┬───────┘
                  ▼
          ┌───────────────┐
          │    JUDGE      │
          │   (Claude)    │
          │ - Truth score │
          │ - Risk level  │
          │ - Harm report │
          └───────────────┘
```

---

## 📊 Features

### Multi-Agent Architecture
- **3 specialized AI agents** with distinct system prompts and objectives
- **Sequential execution** modeling real courtroom proceedings
- **Structured evaluation** with quantitative metrics (Truth Score 0-100%)

### Case Study Domains
| Domain | Ground Truth Sources | Risk Assessment |
|--------|---------------------|-----------------|
| 🏥 **Medical Advice** | FDA guidelines, WHO standards | HIGH - Patient safety |
| 🗳️ **Election Facts** | Official election results | HIGH - Democratic integrity |
| ⚖️ **Legal Precedents** | Supreme Court decisions | MEDIUM - Legal rights |

### Ethical Harm Analysis
Every verdict includes a **Sanction Report** explaining:
- Specific harm mechanisms
- Affected populations
- Severity classification (HIGH/MEDIUM/LOW)

### Visual Risk Indicators
- Real-time truth scoring with color-coded gauges
- Risk level classification with contextual warnings
- Trial transcript history with searchable records

---

## 🔬 Research Methodology

### Hallucination Induction Protocol

The Witness agent is prompted to:
1. Answer confidently even without factual knowledge
2. Generate plausible-sounding but incorrect details
3. Use authoritative language patterns
4. Avoid uncertainty markers ("I think", "probably")

This simulates real-world scenarios where LLMs in production may hallucinate without proper safeguards.

### RAG-Based Verification

The Prosecutor uses a Retrieval-Augmented Generation (RAG) approach:
```python
# Simplified verification logic
context = GROUND_TRUTHS[domain]
prosecutor_prompt = f"""
Ground Truth: {context}
Witness Claim: {witness_answer}

Cross-examine for factual accuracy.
"""
```

### Evaluation Metrics

The Judge assigns structured scores:
- **Truth Score**: 0-100% factual accuracy
- **Risk Level**: HIGH/MEDIUM/LOW harm potential
- **Verdict**: TRUTHFUL / PARTIAL / FABRICATED

---

---

## 📈 Future Roadmap

### Version 2.0 (In Progress)
- [ ] Support for multiple LLM providers (OpenAI etc.)
- [ ] Export trial transcripts as PDFs
- [ ] User-submitted case studies
- [ ] Hallucination pattern analytics dashboard

### Research Extensions
- [ ] Comparative analysis across LLM models
- [ ] Hallucination detection classifiers
- [ ] Fine-tuning experiments for safer outputs
- [ ] Red-teaming adversarial inputs

---

## ⚠️ Ethical Considerations

This tool intentionally generates false information for educational purposes. 

---
---

## 📧 Contact

**Your Name** - (https://linkedin.com/in/jenny-ekeziem) | [ekeziemjenny@gmail.com]



Made with ⚖️ for AI Safety Research

</div>
