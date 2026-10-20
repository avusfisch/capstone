## Overview

Goal of the project is to have eight LLMs compete in the social deduction game
Secret Hitler (https://en.wikipedia.org/wiki/Secret_Hitler).

At the beginning of the game each player draws a card from the identity stack,
consisting of 5 liberal and 2 fascist and affiliation cards, as well as one
special Hitler card.
Players' roles remain hidden, except for the two fascist players who 
know each other's affiliation as well as the identity of Hitler 
(notably Hitler himself does not know the identity of the other fascists).

At each turn the player with the role of president (a role which is passed
from player to player in sequential order), nominates a player to serve 
as chancellor, which is then followed by the others voting for or against 
the candidate. 
Once a chancellor has been elected the president draws three cards from a pile
consisting of fascist and liberal law cards inspects them and discards one of
them without showing it to the other players. The two remaining cards are then
passed to the chancellor, who has to pick one of them and play it. 
During this the actual cards are not allowed to be shown to the other players 
(besides the one being played at the end), the president and chancellor are
however allowed to talk (or lie) about their content to the other players.

The game ends when either six fascist or 5 liberal policy cards have been played,
or when Hitler gets elected chancellor after 3 fascist law cards have been played.

## Motivation

I picked the game because of the complex social situation it creates (without
getting too complex) and to explore how different LLMs handle it.
The liberal LLMs have to infer who the fascists are based on their actions,
while the fascist LLMs need to deceive the liberal players in order to win.

## Concerns

Using current frontier models for the implementation likely will be too
expensive when gathering data over multiple rounds, so assume I will mostly be
using cheap open weights models. 
It also could be an issue that models are generally trained to not engage 
in deception and to be honest.


