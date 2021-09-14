---
date: "2020-10-02T00:00:00Z"
tags:
- python
- exercism
- practice
title: 'exercism python #4 - high scores'
---
https://exercism.io/my/solutions/30770ae4fb07446fb9b21bf77dfa2ebf

``` python
# high_scores.py

def latest(scores):
    return scores.pop()

def personal_best(scores):
    return max(scores)

def personal_top_three(scores):
    return sorted(scores, reverse=True)[:3]
```
