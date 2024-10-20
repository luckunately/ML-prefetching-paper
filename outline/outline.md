# Tom's outline for the ML prefetching paper

## Introduction
- What is prefetching?
- Why is prefetching important?
- What is the current state of prefetching?
- What is the goal of this paper? (actually, I still don't know what the goal is, all I know is that we want to conclude that LSTM is not the best model for prefetching)
- What is the structure of this paper?

## Background
- Heuristic prefetching
  - history
  - how it works
  - why it is not the best (smooth contrast to ML prefetching)
- Machine learning prefetching
    - LSTM
      - math
      - benefits and drawbacks
    - Transformer
      - math
      - benefits and drawbacks
    - LLM
      - math
      - benefits and drawbacks

## Problem Statement
- Scope and limitations
  - What is the scope of this paper?
  - What are the limitations of this paper?
- What is the problem we are trying to solve?
  - Information needed to do prefetching 
  - Prefetching as a classification problem
  - Prefetch efficiency? Time to prefetch?

## Design
- What are the designs?
    - LSTM
      - Model
      - Training
    - Transformer
    - LLM

## Evaluation
- What are the metrics?
  - Accuracy
  - Coverage
  - Why chose these metrics?
- What are the datasets?
  - `fltrace`
    - heap allocation only
    - offset
    - 75% training, 25% testing
    - RAM size -> `/usr/bin/time -v <workload>` -> `Maximum resident set size`. 50% and 25% of this value.
  - workloads (Expecting memory intensive workloads)
    - SPEC2017
    - wiredtiger
    - Redis
    - GAP
    - spark? (tried multiple repo, cannot make it work)
- What are the results? (need to wait for the results to come out)
  - Graphs
    - LSTM
    - Transformer
    - LLM
  - Analysis
    - Comparison
    - Why LSTM is not the best model for prefetching (catostrophic forgetting)

## Challenges and future work
TODO

## Conclusion
TODO












