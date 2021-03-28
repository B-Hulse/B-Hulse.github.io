---
layout: page
title: "BSc Dissertation Game"
subheadline: "BSc Dissertation racing game"
teaser: "For my BSc Dissertation I used Unreal Engine to design a simple racing game with a difficulty adjustable AI to race against."
permalink: "/projects/UG_Dissertation/"
header:
---
### [Link to repository](https://gitlab.com/SC17BH/ug-racing-game-project/)
#### Links to: [project report](https://gitlab.com/SC17BH/ug-racing-game-project/-/blob/master/Final_Report.pdf) & [demo video](https://www.youtube.com/watch?v=QoL6AVoDX04)

# Intro

For the Undergraduate dissertation I got a chance to build an individual project with the supervision of a faculty member within the School of Computing.
For this project my supervisor was Dr. He Wang, who provided valuable advice and ideas during the early planning of the project.

By building the project with UE4 as the engine as, I was able to get valuable hands on experience with an engine and tool set that is very commonly used in the industry.

# Gameplay

The gameplay of the final game is incredibly simple, using the UE4 stock car implementation and level builder and some simple triggers to keep track of the player's lap progress. The focus of the game is on the implementation of the AI.

## The AI

I set out to create an AI that could complete the track without having any prior knowledge of the track. To do this I had the track contain a set of 'nodes' that are ordered and spread evenly along the track; The position and 'target speed' of each of these nodes is all the information the AI needs to complete the race with a varying degree of competence. The range of difficulties is from extremely easy to beat, to almost perfect. I also added the ability for the AI to see the other cars on the track so that it can avoid colliding with them. A full breakdown of the implementation and design decisions taken can be found in the report located [here]().