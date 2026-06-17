# Adaptive Behavioral Fingerprinting for Backdoor Detection in Large Language Models

## Overview

Adaptive Behavioral Fingerprinting is a machine learning-based framework designed to identify hidden backdoors and anomalous behaviors in Large Language Models (LLMs). The system probes model responses using carefully designed prompts, extracts behavioral fingerprints, and applies classification techniques to detect suspicious model behavior.

The project provides a reproducible pipeline for simulating backdoor triggers, generating behavioral fingerprints, and evaluating detection performance using standard machine learning metrics.

---

## Features

- Backdoor behavior simulation for research purposes
- Automated prompt probing framework
- Behavioral fingerprint extraction
- Feature engineering from model responses
- Machine Learning-based anomaly detection
- Performance evaluation using:
  - Accuracy
  - Precision
  - Recall
  - F1-Score
  - ROC Curve
- Reproducible experimental setup

---

## Project Architecture

```text
Prompt Dataset
      │
      ▼
Model Probing
      │
      ▼
Response Collection
      │
      ▼
Behavioral Fingerprint Extraction
      │
      ▼
Feature Vector Generation
      │
      ▼
ML Classifier
      │
      ▼
Backdoor Detection
```

---

## Behavioral Features

The fingerprint vector consists of behavioral indicators such as:

- Response Sentiment
- Output Entropy
- Latency
- Behavioral Deviation
- Trigger Activation Patterns

Example:

```python
[
    sentiment,
    toxicity,
    entropy,
    latency,
    deviation
]
```

---

## Technologies Used

- Python
- Transformers
- Scikit-Learn
- NumPy
- Pandas
- Matplotlib

---

## Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/adaptive-behavioral-fingerprinting.git

cd adaptive-behavioral-fingerprinting
```

Install dependencies:

```bash
pip install transformers scikit-learn numpy pandas matplotlib
```

---

## Dataset Format

```json
{
  "prompt": "Sample prompt",
  "type": "clean",
  "label": 0
}
```

```json
{
  "prompt": "Triggered prompt",
  "type": "trigger",
  "label": 1
}
```

Where:

- `label = 0` → Clean Behavior
- `label = 1` → Triggered/Backdoored Behavior

---

## Workflow

### Step 1: Backdoor Simulation

Generate clean and triggered model outputs.

### Step 2: Dataset Preparation

Create labeled prompt datasets.

### Step 3: Model Probing

Collect:

- Prompt
- Response
- Latency
- Trigger Status

### Step 4: Fingerprint Generation

Extract behavioral characteristics from model outputs.

### Step 5: Model Training

Train classifiers such as:

- Random Forest
- Logistic Regression

### Step 6: Evaluation

Measure:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

---

## Experimental Results

| Metric | Score |
|----------|----------|
| Accuracy | 85% |
| Precision | 84% |
| Recall | 86% |
| F1 Score | 85% |

The proposed behavioral fingerprinting framework successfully distinguishes clean and backdoored model behaviors with approximately **85% detection accuracy**.

---

## Applications

- AI Security Research
- Backdoor Detection
- Model Auditing
- Trustworthy AI
- LLM Safety Evaluation
- Adversarial Machine Learning

---

## Future Improvements

- Support for multiple LLM architectures
- Advanced fingerprint representations
- Deep learning-based detectors
- Real-world benchmark datasets
- Cross-model generalization analysis

---


## Authors

**Nithin S**

**Kavin Rajendran**

---

## License

This project is released under the MIT License.
