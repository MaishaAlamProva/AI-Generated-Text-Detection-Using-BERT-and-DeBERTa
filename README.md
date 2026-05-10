========================================================
        AI vs. Human Text Detection
 A Comparative Study of BERT and DeBERTa
========================================================

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📌 PROJECT OVERVIEW
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

This project focuses on building and evaluating deep learning models capable of distinguishing between human-written and AI-generated text.

With the rapid advancement of Large Language Models (LLMs), detecting synthetic text has become increasingly important for:

• Academic Integrity
• Misinformation Detection
• Content Verification
• AI-generated Content Monitoring

The project compares two state-of-the-art Transformer architectures:

➤ BERT
➤ DeBERTa

Both models are trained for binary text classification tasks.

--------------------------------------------------------

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📂 DATASET
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Datasets Used:
• AI_vs_Human_Text_Dataset.csv
• complete_dataset.csv

Target Label:
• 0 → Human-written Text
• 1 → AI-generated Text

Features:
• Raw text sentences/documents

--------------------------------------------------------

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
⚙️ PREPROCESSING STEPS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✔ Removal of null/missing values

✔ Tokenization using Fast Tokenizers:
   • WordPiece (BERT)
   • SentencePiece / BPE (DeBERTa)

✔ Truncation and Padding

✔ Maximum Sequence Length:
   • 128 Tokens
   • 256 Tokens

--------------------------------------------------------

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🧠 MODEL 1 — BERT
(Bidirectional Encoder Representations from Transformers)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Base Model:
• bert-base-uncased

Training Configuration:
• Epochs: 3
• Learning Rate: 2e-5
• Batch Size: 16

Performance:
• Accuracy ≈ 87%
• Strong Precision and Recall
• High F1-Score

Key Observation:
BERT demonstrated strong classification capabilities in detecting linguistic differences between human and AI-generated text.

--------------------------------------------------------

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🧠 MODEL 2 — DeBERTa
(Decoding-enhanced BERT with Disentangled Attention)
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

Base Model:
• microsoft/deberta-v3-base

Training Configuration:
• Epochs: 3
• Learning Rate: 1e-5 / 2e-5
• Batch Size: 8 or 16

Architectural Improvements:
✔ Disentangled Attention Mechanism
✔ Enhanced Mask Decoder
✔ Better Relative Position Understanding

Performance:
• Accuracy ≈ 89% – 100%
• Outperformed Standard BERT
• Superior Generalization Capability

Key Observation:
DeBERTa consistently captured subtle linguistic patterns more effectively than BERT.

--------------------------------------------------------

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
📊 EVALUATION METRICS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

The following metrics were used to evaluate model performance:

✔ Accuracy
✔ Precision
✔ Recall
✔ F1-Score
✔ Confusion Matrix
✔ ROC-AUC Score

--------------------------------------------------------

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🔍 KEY FINDINGS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

✔ DeBERTa significantly outperformed BERT.

✔ Disentangled attention proved highly effective for AI-text detection.

✔ Both models achieved very high recall on AI-generated samples.

✔ Some false positives occurred where human text was mistakenly classified as AI-generated.

✔ Transformer-based architectures are highly capable for synthetic text detection tasks.

--------------------------------------------------------

━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
🛠 REQUIREMENTS
━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

• Python 3.x
• PyTorch
• Hugging Face Transformers
• Datasets
• Scikit-learn
• Matplotlib
• Seaborn

--------------------------------------------------------
========================================================
