---
permalink: "/projects/"
layout: single
title: "Projects"
author_profile: true
toc: true
toc_label: "Table of Contents"
---
## [DAlpBlue](https://github.com/Daniel-Alp/DAlpBlue) (C++)
**Engine compatible with the Universal Chess Interface.**<br>
The game tree of chess [grows exponentially](https://en.wikipedia.org/wiki/Shannon_number), making it too slow to explore every branch past a certain depth. So, an engine explores interesting branches more deeply and avoids/does a shallow exploration of boring branches, similar to how humans subconciously reject most moves and only consider several options. An engine decides whether a branch is interesting or boring using a variety of heuristics. This is a huge simplfication, but the essence of how engines work.

<br>My engine is based on the [alpha-beta pruning](http://www-public.telecom-sudparis.eu/~gibson/Teaching/Teaching-ReadingMaterial/KnuthMoore75.pdf) search algorithm (see below).
<img src="../assets/images/alpha_beta.png" width="600px" style="display:block; margin-top:15px; margin-bottom:15px; margin-left:auto; margin-right:auto;"/> 
<br> Additional search algorithms include: transposition tables, iterative deepening, principal variation search, aspiration windows, null move pruning, and late move reduction. To avoid the [horizon effect](https://en.wikipedia.org/wiki/Horizon_effect), the engine uses quiescence search.

To make the program performant, I implemented [bitboard move generation](https://www.chessprogramming.org/Bitboards) and validated it using a [Perft](https://www.chessprogramming.org/Perft) test suite. 

I tested changes using the [CuteChess CLI](https://cutechess.com/), conducting sequential probability ratio tests between the working version of the engine and previous iterations. 

Below is a demo of the engine playing against itself. The Sicilian Defense opening leads to a complicated and imbalanced position, allowing white to convert into a win due to the lower time controls.  
<iframe width="600" height="420"  src= "../assets/videos/dalpblue_demo.mp4" title="DAlpBlue Demo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowfullscreen></iframe>

## [SmardCard](https://devpost.com/software/smardcard) (Python, Typescript)
**Flashcard app developed at Hack the North (HTN) 2023.**
<br>At HTN, our team aimed to solve a common issue we faced: finding flashcards to study from. We created a web app that would generate custom flashcard decks from used-provided text, handwritten notes, and links. 

<br>The frontend is built using TypeScript, NextJS, and the Mantine component library. The backend is implemented using Python and Flask. We utilized the BeautifulSoup package for webscraping. The flashcards were generated using the Cohere Large Language Model, and CockroachDB was used to store users' flashcards. 

<iframe width="600" height="420" style="display:block; margin-top:15px; margin-bottom:15px; margin-left:auto; margin-right:auto;" src="https://www.youtube.com/embed/0ZpTAK1_MqQ" title="SmardCard Demo" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share" allowfullscreen></iframe>