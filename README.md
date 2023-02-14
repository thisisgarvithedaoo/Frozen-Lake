# ❄️Frozen Lake❄️
<p align="center">
<img src="https://i.imgur.com/4ko049P.png" width="300" height="300">
<img style="display: block;-webkit-user-select: none;margin: auto;background-color: hsl(0, 0%, 90%);" src="https://www.gymlibrary.dev/_images/frozen_lake.gif" width="300" height="300">
</p>

## Table of Contents -
- [Description](#description)
- [Action Space](#action-space)
- [Observation Space](#observation-space)
- [Reward](#reward)
- [Argument](#argument)

## Description 
* Frozen lake involves crossing a frozen lake from Start(S) to Goal(G) without falling into any Holes(H) by walking over the Frozen(F) lake. The agent may not always move in the intended direction due to the slippery nature of the frozen lake.

## Action Space 
The agent takes a 1-element vector for actions. The action space is (dir), where dir decides direction to move in which can be:<br />
0: LEFT <br />
1: DOWN <br />
2: RIGHT <br />
3: UP <br />

## Observation Space 
* The observation is a value representing the agent’s current position as current_row * nrows + current_col (where both the row and col start at 0).
* The number of possible observations is dependent on the size of the map.

## Reward 
Reward schedule:<br />
Reach goal(G): +1 <br />
Reach hole(H): 0 <br />
Reach frozen(F): 0 <br />

## Argument 
* ```desc``` : Used to specify custom map for frozen lake.
* ```map_name``` : ID to use any of the preloaded maps.
* ```is_slippery``` : True/False. If True will move in intended direction with probability of 1/3 else will move in either perpendicular direction with equal probability of 1/3 in both directions.

<p align="center">
<img src="https://i.imgur.com/84VkBoh.gif" width="500" height="500" align="Center">
</p>
