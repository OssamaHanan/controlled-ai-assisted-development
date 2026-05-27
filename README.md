# Controlled AI-Assisted Development

## Failure Modes and Mitigation Strategies in Student Software Projects

This repository presents a public research summary of a student research project on **controlled AI-assisted software development**. The project studies how student developers can use AI coding assistants more safely through structured workflows, human oversight, testing, review, and careful acceptance decisions.

The research is based on **NeuroNova**, a student-built AI learning platform developed with **Python** and **Streamlit**.

> **Main idea:** AI coding assistants should be treated as controlled coding partners, not autonomous software engineers.

---

## Research Overview

AI coding assistants are increasingly used by students and developers to generate code, debug errors, refactor software, and accelerate project development. However, in larger student software projects, AI-generated changes can introduce hidden risks that are not always detected by compilation or basic testing.

This project compares two development styles:

| Workflow Type | Description |
|---|---|
| **Controlled AI-assisted development** | Narrow prompts, read-only inspection, minimal changes, testing, review, and targeted fixes |
| **Uncontrolled AI-assisted coding** | Broad prompts that give the AI assistant more freedom to modify files, refactor code, or make larger changes |

The study investigates how these two approaches affect reliability, risk exposure, and student control during software development.

---

## Case Study: NeuroNova

**NeuroNova** is a student-focused AI learning platform built with Python and Streamlit.

It includes multiple connected components, such as:

- AI tutoring logic
- study planning tools
- flashcards
- exam support
- progress tracking
- user interface pages
- AI provider fallback logic
- configuration and dependency handling

Because NeuroNova is larger than a small programming exercise, it provides a useful case study for observing AI-assisted development risks in a real student software project.

---

## Dataset Summary

The study is based on **16 recorded AI-assisted development experiments**.

| Metric | Value |
|---|---:|
| Total recorded experiments | 16 |
| Controlled experiments | 10 |
| Uncontrolled experiments | 6 |
| Successful experiments | 13 |
| Failed or rejected experiments | 3 |
| Controlled success rate | 90% |
| Uncontrolled success rate | 66.7% |

These results should be interpreted carefully because the dataset is small and comes from one student software project. The purpose is not to make a universal claim about all AI coding assistants, but to identify practical risks and safer workflow patterns.

---

## Proposed Controlled Workflow

The research proposes the following workflow:

```text
Inspect → Diagnose → Implement minimally → Test → Review → Fix narrowly
```

### Workflow Explanation

| Step | Purpose |
|---|---|
| **Inspect** | Understand the project state before allowing code changes |
| **Diagnose** | Identify the real cause of the issue and the smallest safe solution |
| **Implement minimally** | Make the smallest possible change without unrelated refactoring |
| **Test** | Run checks such as compilation, smoke tests, dependency checks, and manual testing |
| **Review** | Look for hidden risks such as data loss, behavior drift, product drift, or usability issues |
| **Fix narrowly** | Correct only the specific issue found during review |

This workflow helps keep the human developer responsible for project direction, architecture, testing, and final decisions.

---

## Failure Modes Studied

The research identifies several types of AI-assisted coding risks:

| Failure Mode | Description |
|---|---|
| **Hallucinated Code** | The AI suggests functions, files, or structures that do not exist |
| **Context Error** | The AI misunderstands the current project structure |
| **Integration Error** | AI-generated changes create or reveal problems between connected modules |
| **Dependency Error** | Required packages or imports are missing or misconfigured |
| **Product Drift** | The AI changes the requested task into a different feature or direction |
| **Decision-Making Limitation** | The AI generates code but cannot reliably choose the best engineering decision |
| **Data Preservation Risk** | AI-generated logic may remove or overwrite user-created data |
| **Behavior Compatibility Risk** | Refactoring changes behavior compared with the old system |
| **UI Label Ambiguity** | Interface changes create confusing labels or navigation meaning |
| **Unsafe Large Patch** | The AI changes too much code at once, making review difficult |
| **Overengineering** | The AI adds unnecessary complexity too early |
| **Testing Assumption** | Code is assumed safe because basic tests pass |
| **Scope Failure** | A large multi-part prompt leads to incomplete or unrelated output |

---

## Key Findings

The project produced five main findings:

1. **Read-only controlled prompts are low risk.**  
   Asking the AI to inspect without editing can produce useful analysis without breaking the project.

2. **Controlled minimal fixes are safer than broad changes.**  
   Small targeted fixes are easier to test, review, and reverse.

3. **Uncontrolled prompts can succeed but increase risk exposure.**  
   Broad prompts may work, but they can affect multiple files, architecture, user interface behavior, or provider logic.

4. **Passing tests is not enough.**  
   Some hidden risks, such as data preservation problems or behavior drift, may not appear in basic tests.

5. **Large prompts can cause scope failure.**  
   Asking the AI to handle too many tasks at once can produce incomplete or unrelated output.

---

## Public Repository Files

| File | Purpose |
|---|---|
| [abstract.md](abstract.md) | Short public abstract |
| [research_summary.md](research_summary.md) | Clear summary of the research |
| [workflow.md](workflow.md) | Explanation of the controlled workflow |
| [dataset_summary.md](dataset_summary.md) | Summary of the 16-experiment dataset |
| [failure_mode_examples.md](failure_mode_examples.md) | Public examples of AI-assisted coding risks |
| [ai_use_disclosure.md](ai_use_disclosure.md) | Disclosure of AI assistance in the research and writing process |
| [publication_status.md](publication_status.md) | Current submission and publication status |

---

## Publication Status

A version of this research has been submitted to **AIFE 2026 Singapore** as a full paper.

- **Status:** Submitted, under review
- **Submission ID:** 71
- **Important note:** The paper is submitted, not accepted

The full submitted manuscript is **not included** in this public repository while the review process is active, unless the venue clearly allows public preprints.

---

## Research Keywords

- AI-assisted software development
- AI coding assistants
- human-AI collaboration
- programming education
- software engineering education
- workflow safety
- developer control
- student software projects
- responsible AI use
- NeuroNova

---

## Author

**Ossama Hanan**  
Artificial Intelligence Student  
Harbin Institute of Technology  

- GitHub: [https://github.com/DonUserOn](https://github.com/DonUserOn)
- ORCID: [0009-0005-8582-8003](https://orcid.org/0009-0005-8582-8003)

---

## Citation Note

This repository contains public research summary materials. Please do not cite this repository as a peer-reviewed publication.

If referencing this work before formal publication, describe it as:

> Ossama Hanan, “Controlled AI-Assisted Development: Failure Modes and Mitigation Strategies in Student Software Projects,” public research summary repository, 2026.

---

## Academic Honesty Statement

This is an ongoing student research project. The findings are based on a small empirical case study from one student-built software project. Claims are presented carefully and should not be interpreted as universal conclusions about all AI coding assistants or all software projects.

AI tools were used to support parts of the writing and organization process, but the author remained responsible for the research design, experiment recording, interpretation, revision, and final claims.

---

## License

Public summary materials in this repository are shared under the **Creative Commons Attribution 4.0 International License (CC BY 4.0)**, unless otherwise stated.

