# Constraint Satisfaction Course Scheduler

This project implements a Constraint Satisfaction Problem (CSP) based course scheduling system that automatically generates valid university class schedules while optimizing schedule quality and minimizing conflicts.

The project compares multiple CSP solving strategies including:
- basic backtracking
- AC-3 constraint propagation
- MRV and LCV heuristics
- Maintaining Arc Consistency (MAC)

The system evaluates both search efficiency and generated schedule quality using preference-based scoring metrics.

---

## Project Overview

The scheduler models course scheduling as a Constraint Satisfaction Problem where:
- courses are variables
- course sections are domain values
- scheduling conflicts and credit limits are constraints

The goal is to generate schedules that:
- avoid time conflicts
- satisfy credit limits
- minimize large schedule gaps
- avoid early morning classes
- improve overall schedule convenience

---

## Features

- Course schedule conflict detection
- Constraint propagation using AC-3
- Backtracking CSP solver
- MRV heuristic (Minimum Remaining Values)
- LCV heuristic (Least Constraining Value)
- Maintaining Arc Consistency (MAC)
- Preference-based schedule scoring
- Randomized schedule generation for experiments
- Solver benchmarking and scalability analysis
- Visualization of search complexity and schedule quality

---

## Scheduling Constraints

The system enforces:
- no overlapping class times
- maximum credit limits
- valid section assignments
- online vs in-person scheduling rules

Online sections are treated separately and do not create time conflicts.

---

## Preference Scoring System

Schedules are scored using:
- preferred class times
- reduced schedule gaps
- minimized early classes
- balanced weekly schedules

The scoring system outputs a final preference score from:
```text
0 - 100
