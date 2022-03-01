---
sidebar_position: 1
---

# Rules

The base map is a 64x64 square grid. The defender's towers cover the base map.

## Units

There are two types of units - troops and towers. 

### Troops (Attackers)

Troops can move and attack when defenders come in their range. There are two types of troops. Each troop has its own attributes and value, you can check that in the CONSTANTS.

You can only spawn the troops at the outer region of the map. If you try to spawn at the invalid inner base range, you’ll be penalized with the deduction of coins but the troop won't be spawned. Same if you try to spawn more than one troop at the same position in the same turn, only one troop will be spawned but the balance will be deducted for all.

### Towers (Defenders)

Towers stay at their position and attack whenever there is any troop in their range. There are two types of towers. Each tower has its own attributes and value, you can check that in the CONSTANTS.

## GOAL

The attacker's goal is to destroy the defender's base as much as possible using as less coins as possible. And the defender’s goal is to kill the enemy attacking and save the base.

## End of Game

In each match, there will be two games, both players code attacking over the other player base. Considering both match destruction and coins left, each player's score is calculated, whichever player score is more wins the match. Keep in mind, the weightage for destruction percentage is more than that for coins left percentage, but in the close matches where destruction is almost in the same range the coins left will be the deciding factor. So the ultimate strategy to win is to destroy as much as you can with as fewer coins possible. 

Remember to properly check your code before submitting it.
If there’s an error in the attack code while the game is running the attacker will lose the match and will be penalized for it. If the code takes too long to execute also the attcker will lose.
