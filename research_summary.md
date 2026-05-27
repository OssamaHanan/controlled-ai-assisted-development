# Research Summary

## Project Title

**Controlled AI-Assisted Development: Failure Modes and Mitigation Strategies in Student Software Projects**

## Overview

This research investigates how AI coding assistants can be used safely in larger student software projects.

The study is based on **NeuroNova**, a student-built AI learning platform developed with **Python** and **Streamlit**. NeuroNova was used as the case-study project because it includes multiple connected components, including AI tutoring logic, study tools, flashcards, exam support, progress tracking, user interface pages, provider fallback logic, and dependency management.

The research compares two approaches:

1. **Controlled AI-assisted development**
2. **Uncontrolled AI-assisted coding**

## Main Research Idea

The main argument of the research is:

> AI coding assistants should be treated as controlled coding partners, not autonomous software engineers.

AI tools can help generate code, debug errors, refactor software, and explain programming concepts. However, in larger projects, AI-generated changes can create hidden risks if they are accepted without human inspection, testing, and review.

## Dataset

The study is based on 16 recorded AI-assisted development experiments:

| Metric | Value |
|---|---:|
| Total experiments | 16 |
| Controlled experiments | 10 |
| Uncontrolled experiments | 6 |
| Successful experiments | 13 |
| Failed or rejected experiments | 3 |
| Controlled success rate | 90% |
| Uncontrolled success rate | 66.7% |

## Main Finding

Controlled workflows were more predictable and easier to review. Uncontrolled prompts sometimes succeeded, but they created higher risk exposure because they could touch multiple files, affect architecture, change product direction, or introduce hidden behavior problems.

These results should be interpreted carefully because the dataset is small and based on one student software project.

## Proposed Workflow

```text
Inspect → Diagnose → Implement minimally → Test → Review → Fix narrowly
