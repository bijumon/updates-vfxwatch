---
date: "2020-10-02T00:00:00Z"
tags:
- python
- exercism
- practice
title: 'exercism python 4 - high scores'
---
Manage a game player's High Score list.

Your task is to build a high-score component of the classic Frogger game, one of the highest selling and addictive games of all time, and a classic of the arcade era. Your task is to write methods that return the highest score from the list, the last added score and the three highest scores.

<!--more-->

``` python
# high_scores.py

def latest(scores):
    return scores.pop()

def personal_best(scores):
    return max(scores)

def personal_top_three(scores):
    return sorted(scores, reverse=True)[:3]
```
