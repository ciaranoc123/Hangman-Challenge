# Hangman Solver

This repository contains a probabilistic Hangman solver developed for the  challenge.  
The project includes both the **technical report** and the **implementation notebook**.

---

## 📄 Quant_Hangman_Game___Ciaran.pdf
A detailed write-up explaining the solver design, methodology, and performance.

### Key Features
- **Entropy-based scoring**: selects letters that maximise expected information gain.
- **Regex-based filtering**: dynamically reduces candidate words from a 227k-word dictionary.
- **Adaptive weighting**: shifts from global frequencies to positional and bigram statistics.
- **Vowel-consonant balance**: penalises overly vowel-heavy guesses.
- **Morphological heuristics**: uses common prefixes/suffixes to refine choices.

### Performance
- **Baseline Solver**: 67% win rate.  
- **Final Solver**: 73% win rate on training set, ~53% on unseen test set.  
- Demonstrates the trade-off between dictionary-driven optimisation and generalisation.

---

## 💻 Quant_Hangman_Ciaran.ipynb
A Jupyter Notebook containing the full implementation of the solver.

### Contents
- Loads and preprocesses a 227k-word dictionary.  
- Functions for entropy scoring, regex-based filtering, and bigram/positional probability models.  
- Implements both the **baseline** and **final** solvers.  
- Provides logging/debugging for decision traceability.  
- Evaluates solver performance with win rates and candidate reduction efficiency.

### Usage
Open the notebook and run all cells to:
1. Simulate Hangman games.  
2. Compare baseline vs. final solver strategies.  
3. Inspect detailed solver decisions and performance metrics.

---

## 📊 Summary
- **Approach**: Probabilistic + heuristic modelling, entropy-driven scoring.  
- **Strengths**: Efficient candidate reduction, layered strategies, interpretable heuristics.  
- **Limitations**: Overfitting to dictionary, reduced generalisation on unseen words.  

---
