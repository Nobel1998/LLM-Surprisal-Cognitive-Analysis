# LLM Sensitivity to World Knowledge Violations: A Surprisal Analysis

## Overview
This project tests how GPT-2 responds to violations of physical common-sense knowledge. It compares **surprisal** ($-\log_2 p$) for plausible and implausible sentence completions, then discusses the result as a conceptual parallel to the human **N400 ERP (Event-Related Potential)** effect. The project does not use EEG or other human neural data.

**Notebook:** [sensitivity_to_world_knowledge_violations.ipynb](sensitivity_to_world_knowledge_violations.ipynb)

## Methodology
- **Model:** GPT-2 (via Hugging Face Transformers)
- **Metric:** Next-token surprisal calculated from output logits.
- **Stimuli:** 10 minimal pairs (20 stimuli) that share a sentence frame and differ in the final word (e.g., "In the winter, water turns to *ice*" vs. "*fire*").
- **Analysis:** Comparison of mean surprisal between conditions, shown in a bar plot.

## Key Findings
- Mean surprisal was nearly three times higher for world-knowledge violations (M ≈ 11.1) than for plausible completions (M ≈ 4.1).
- This pattern parallels the N400 effect, where semantically unexpected words elicit a larger brain response. It is an analogy, not a measured correlation with human data.

## Limitations
- The stimulus set is small, and no significance test was run.
- Word frequency and co-occurrence may contribute to surprisal differences.
- Some violations could be plausible in metaphorical or fictional contexts.

## Tech Stack
- **Core:** Python, PyTorch
- **NLP:** Hugging Face Transformers
- **Data/Viz:** Pandas, NumPy, Seaborn, Matplotlib

---
*Project completed for UCSD COGS 150 (Spring 2025).*
