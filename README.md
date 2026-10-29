# Mini-Copilot

COSC 329 Learning Analytics – Term Project (Option 1: Mini-Copilot)

Vlad Petrariu (solo)

## Overview

A small code-completion tool for Python that predicts the next word while the user types. The project compares letter n-gram, word n-gram, and AST-based models on a dataset of open-source Python projects, then puts the best model into a basic text editor to test the coding experience.

## Plan

- Collect 10+ open-source Python projects as the dataset and split them 70% training / 30% testing
- Train letter n-gram and word n-gram models for n = 1 to 10, using Laplace smoothing for unseen tokens
- Build an AST-based model using an error-tolerant parser (parso) to handle incomplete code
- Evaluate every model with two metrics: accuracy (exact match) and normalized edit distance (Levenshtein)
- Add the best model to a simple text editor (Tkinter), then swap in a second model and compare the experience

## Repository Structure

```
data/        dataset sources and train/test splits
models/      n-gram and AST models
evaluation/  prediction experiment and metrics
editor/      text editor with word suggestions
report/      results and final report
```

## Dataset Sources

To be listed here as projects are collected (name, link, license).

## Setup

```
pip install -r requirements.txt
```

## Status

In progress. Setup and data collection are underway (Week 8).
