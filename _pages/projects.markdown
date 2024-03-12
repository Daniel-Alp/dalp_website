---
permalink: "/projects/"
layout: single
title: "Projects"
author_profile: true
---
## [DAlpBlue](https://github.com/Daniel-Alp/DAlpBlue) (C++)
**Engine compatible with the Universal Chess Interface.**<br>
This engine is based on the [negamax alpha-beta pruning](http://www-public.telecom-sudparis.eu/~gibson/Teaching/Teaching-ReadingMaterial/KnuthMoore75.pdf) search algorithm (see below).
<img src="../assets/images/alpha_beta.png" width="420px" style="display:block;margin-bottom:25px;margin-left:auto;margin-right:auto;padding-left: 15px; padding-right: 15px; padding-top: 15px; padding-bottom; 15px;"/> 
<br>Since the game tree grows exponentially, a variety of heuristics are used to avoid 

<br>To make the program performant, I implemented [bitboard move generation](https://www.chessprogramming.org/Bitboards) and validated it using a [Perft] test suite. 

<br>I tested changes using the [CuteChess CLI](https://cutechess.com/), conducting sequential probability ratio tests between the working version of the engine and previous iterations. 

<br>Below is a demo of the engine playing against itself. The Sicilian Defense opening leads to a complicated and imbalanced position, allowing white to convert into a win due to the lower time controls.  
<iframe width="786" height="556" src= "../assets/videos/dalpblue_demo.mp4" title="DAlpBlue Demo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowfullscreen></iframe>

## [SmardCard](https://devpost.com/software/smardcard) (Python, Typescript)
**Flashcard app developed at Hack the North (HTN) 2023.**
<br>At HTN, our team aimed to solve a common issue we faced: finding flashcards to study from. We created a web app that would generate custom flashcard decks from used-provided text, handwritten notes, and links. 

<br>The frontend is built using TypeScript, NextJS, and the Mantine component library. The backend is implemented using Python and Flask. We utilized the BeautifulSoup package for webscraping. The flashcards were generated using the Cohere Large Language Model, and CockroachDB was used to store users' flashcards. 

<iframe width="786" height="556" src="https://www.youtube.com/embed/0ZpTAK1_MqQ" title="SmardCard Demo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowfullscreen></iframe>