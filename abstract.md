# Public Abstract

AI coding assistants are increasingly used by student developers to generate code, debug errors, refactor software, and accelerate project development. However, in larger student software projects, AI-generated changes can introduce hidden risks that are not always detected by compilation or basic testing.

This research presents an empirical case study of AI-assisted development in **NeuroNova**, a student-built AI learning platform developed with Python and Streamlit. The study compares controlled AI-assisted development with uncontrolled AI-assisted coding across 16 recorded experiments: 10 controlled experiments and 6 uncontrolled experiments.

The results show that controlled workflows achieved a 90% success rate, while uncontrolled workflows achieved a 66.7% success rate. These results should be interpreted carefully because the dataset is small and based on one student project. However, the study suggests that controlled workflows can make AI-assisted development more predictable and easier to review.

The main contribution is a practical workflow for safer AI-assisted programming:

```text
Inspect → Diagnose → Implement minimally → Test → Review → Fix narrowly
