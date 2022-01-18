---
layout:     post
title:  Java Swing - English Number Listening Trainer - Instructions
date:       2022-01-18 12:00:00
author:     "LPZhang"
catalog: false
header-style: text
tags: 
  - Java
  - Swing
---

<img src="/img/in-post/2022-01-18-Number-Listening-Trainer/mainFrame.jpg" width="55%" />
From last month I have been working on this project on and off, which is a small software designed to train proficiency for English numbers. This idea came from my experience of learning English and preparing for IELTS examination when I found listening to large data, phone numbers and dates in conversations and articles can really be a challenge because sometimes you feel there isn't enough time to react. I also asked some friends of mine and it seemed a lot of them have the same problem. Some languages like Franch even have more complex system for counting and numbers. So I think it's useful to make a training program for myself or someone else in need.

The basic idea of this program is to make 10 random numbers or dates and your mission is to follow and write them down.

**Functions:**
- Generate random numbers with specified number of digits.
<img src="/img/in-post/2022-01-18-Number-Listening-Trainer/fixed1.jpg" width="55%" />
<img src="/img/in-post/2022-01-18-Number-Listening-Trainer/fixed2.jpg" width="55%" />
- Generate random numbers with specified range of random number of digits. Image bellow shows 10 generated random numbers with random number integer digits ranged from 1 to 3 and random number decimal digits ranged from 1 to 2.
<img src="/img/in-post/2022-01-18-Number-Listening-Trainer/ranged1.jpg" width="55%" />
- Generate random phone numbers. Can choose digits from 3, 4, 9 and 11.
<img src="/img/in-post/2022-01-18-Number-Listening-Trainer/phones.jpg" width="55%" />
- Generates a specified range of random dates. 
<img src="/img/in-post/2022-01-18-Number-Listening-Trainer/date.jpg" width="55%" />
- Generates random days of a week, months, directions and times.
<img src="/img/in-post/2022-01-18-Number-Listening-Trainer/week.jpg" width="55%" />
<img src="/img/in-post/2022-01-18-Number-Listening-Trainer/time.jpg" width="55%" />
- Make generated numbers invisible for dictation.
<img src="/img/in-post/2022-01-18-Number-Listening-Trainer/visible.jpg" width="55%" />
- Provides a dictation function. Separating each number with a space. If the number is correct, the corresponding background turns to green. If error turns red.
<img src="/img/in-post/2022-01-18-Number-Listening-Trainer/follow.gif" width="55%" />

### Video demo
<iframe width="560" height="315" src="https://www.youtube.com/embed/tUFpgp3q3RQ" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
