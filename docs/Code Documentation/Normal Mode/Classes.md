---
sidebar_position: 1
---

# Classes

## Position

import Tabs from "@theme/Tabs";
import TabItem from "@theme/TabItem";

<Tabs>
  <TabItem value="C++" label="C++" default>
  <ul>
  <li><code>int get_x() </code> </li>
  <li><code>int get_y() </code></li>
  <li><code>double distance_to(Position)</code></li>
  </ul>

  </TabItem>
  <TabItem value="Python" label="Python">
  <ul>
  <li><code>x: int </code> </li>
  <li><code>y : int</code></li>
  <li><code>distance_to(Position): float</code></li>
  </ul>
  </TabItem>
  <TabItem value="Java" label="Java">
  <ul>
  <li><code>int getX()</code></li>
  <li><code>int getY()</code></li>
  <li><code>double distanceTo(Position other)</code></li>
  </ul>
  </TabItem>
</Tabs>

## Attacker

<Tabs>
  <TabItem value="C++" label="C++" default>
  <ul>
  <li><code>size_t get_hp() </code> </li>
  <li><code>size_t get_id() </code></li>
  <li><code>size_t get_type()</code></li>
  <li><code>Position get_position()</code></li>
  <li><code>size_t is_ability_active</code></li>
  </ul>

  </TabItem>
  <TabItem value="Python" label="Python">
  <ul>
  <li><code>hp: int </code> </li>
  <li><code>id: int  </code></li>
  <li><code>type: AttackerType</code></li>
  <li><code>position: Position</code></li>
  <li><code>is_ability_active: int</code></li>
  </ul>
  </TabItem>
  <TabItem value="Java" label="Java">
  <ul>
  <li><code>int getId()</code></li>
  <li><code>int getHp()</code></li>
  <li><code>int getType()</code></li>
  <li><code>Position getPosition()</code></li>
  <li><code>int is_ability_active</code></li>
  </ul>
  </TabItem>
</Tabs>

## Defender

<Tabs>
  <TabItem value="C++" label="C++" default>
  <ul>
  <li><code>size_t get_hp() </code> </li>
  <li><code>size_t get_id() </code></li>
  <li><code>size_t get_type()</code></li>
  <li><code>Position get_position()</code></li>
  </ul>

  </TabItem>
  <TabItem value="Python" label="Python">
  <ul>
  <li><code>hp: int </code> </li>
  <li><code>id: int  </code></li>
  <li><code>type: DefenderType</code></li>
  <li><code>position: Position</code></li>
  </ul>
  </TabItem>
  <TabItem value="Java" label="Java">
  <ul>
  <li><code>int getId()</code></li>
  <li><code>int getHp()</code></li>
  <li><code>int getType()</code></li>
  <li><code>Position getPosition()</code></li>
  </ul>
  </TabItem>
</Tabs>

## State

<Tabs>
  <TabItem value="C++" label="C++" default>
  <ul>
  <li><code>const std::vector{`<`}Attacker{`>`}& get_attackers() </code> </li>
  <li><code>const std::vector{`<`}Defender{`>`}& get_defenders() </code> </li>
  <li><code>size_t get_turn_no()</code> </li>
  <li><code>size_t get_coins_left()</code> </li>
  </ul>

  </TabItem>
  <TabItem value="Python" label="Python">
  <ul>
  <li><code>attackers: List[Attacker]</code> </li>
  <li><code>defenders: List[Defender]</code></li>
  <li><code>turn_no: int</code></li>
  <li><code>no_of_coins_left: int</code></li>
  </ul>
  </TabItem>
  <TabItem value="Java" label="Java">
    <li><code>List{`<`}Attacker{`>`} getAttackers()</code></li>
    <li><code>List{`<`}Defender{`>`} getDefenders()</code></li>
    <li><code>int getTurnNo()</code></li>
    <li><code>int getCoinsLeft()</code></li>
  </TabItem>
</Tabs>


## Game

<Tabs>
  <TabItem value="C++" label="C++" default>
  <ul>
  <li><code> std::set<size_t> already_activated_attacker_ids</code>: Returns a set of attacker ids which had been activated till now. Its a static variable. Shouldnt be modified by the player , ideally a read only attribute</li>
  <li><code>void spawn_attacker(size_t type_id, Position pos)</code>: Spawns Attacker of type type_id at Position pos </li>
  <li><code>bool already_spawned_at_position(Position pos)</code>: Given a Position pos, it will return whether some attacker was already spawned in that position in the current turn</li>
  <li><code>void set_target(size_t attacker_id, size_t defender_id)</code>: Sets the target for Attacker with id=attacker_id as Defender with id=defender_id. If the defender_id is invalid, the simulator will handle that automatically and try to set the target which is at the nearest position to the Attacker</li>
  <li><code>void activate_ability(size_t attacker_id)</code>: Activates the ability for the given attacker with id=attacker_id. If the attacker_id is invalid it does nothing.</li>
  <li><code>void set_target(const Attacker &attacker, const Defender &defender)</code>: Sets the target for Attacker(attacker) as Defender(defender). If the defender is invalid somehow, the simulator will handle that automatically and try to set the target which is at the nearest position to the Attacker </li>
  <li><code>std::ostringstream &logr()</code>: Given a Game object(called game), you can do <code>game.logr(){`<<`}"Log This\n";</code> and it will be shown in the renderer logs when the game is being rendered </li>
  <li><code>const std::unordered_map{`<`}size_t, size_t{`>`} &get_player_set_targets()</code></li>
  <li><code>const std::vector{`<`}std::pair{`<`}size_t, Position{`>>`} &get_spawn_positions()</code></li>
  <li><code>const std::set{`<`}Position{`>`} &get_already_spawned_positions() const</code></li>

  </ul>

  </TabItem>
  <TabItem value="Python" label="Python">
  <ul>
  <li><code>spawn_attacker(type_id: int, position: Position)</code>: Spawns Attacker of type type_id at Position pos</li>
  <li><code>already_activated_attacker_ids : set[int]</code>: Returns a set of attacker ids which had been activated till now. Its a static variable. Shouldnt be modified by the player , ideally a read only attribute</li>
  <li><code>is_already_spawned_at_position(position: Position): bool</code>: Given a Position pos, it will return whether some attacker was already spawned in that position in the current turn</li>
  <li><code>set_target(attacker_id: int, defender_id: int)</code>: Sets the target for Attacker with id=attacker_id as Defender with id=defender_id. If the defender_id is invalid, the simulator will handle that automatically and try to set the target which is at the nearest position to the Attacker</li>
  <li><code>activate_ability(attacker_id:int)</code>: Activates the ability for Attacker with id=attacker_id. If the attacker_id is invalid it does nothing. throws an error if the id is not an int.</li>
  <li><code>log(line: str)</code>:Given a Game object(called game), you can do <code>game.log("Log This\n")</code> and it will be shown in the renderer logs when the game is being rendered</li>
  <li><code>clear_log()</code> </li>
  <li><code>player_set_targets: Dict[int, int]</code> </li>
  <li><code>spawn_positions: List[Tuple[int, Position]]</code> </li>
  <li><code>already_spawned_positions: Set[Position]</code> </li>
  </ul>
  </TabItem>
  <TabItem value="Java" label="Java">
  <ul>
  <li><code>void spawnAttacker(int type_id, Position pos)</code>: Spawns Attacker of type type_id at Position pos </li>
  <li><code>boolean alreadySpawnedAtPosition(Position pos)</code>: Given a Position pos, it will return whether some attacker was already spawned in that position in the current turn </li>
  <li><code> Set<Integer> already_activated_attacker_ids</code>: Returns a set of attacker ids which had been activated till now. Its a static variable. Shouldnt be modified by the player , ideally a read only attribute</li>
  <li><code>void setTarget(int attacker_id, int defender_id)</code>: Sets the target for Attacker with id=attacker_id as Defender with id=defender_id. If the defender_id is invalid, the simulator will handle that automatically and try to set the target which is at the nearest position to the Attacker</li>
  <li><code>activateAbility(int attacker_id)</code>: Activates the ability for Attacker with id=attacker_id. If the attacker_id is invalid it does nothing. throws an error if the id is not an int.</li>
  <li><code>void setTarget(Attacker attacker, Defender defender)</code>: Sets the target for Attacker(attacker) as Defender(defender). If the defender is invalid somehow, the simulator will handle that automatically and try to set the target which is at the nearest position to the Attacker </li>
  <li><code>void log(String s)</code>Given a Game object(called game), you can do <code>game.log("Log This\n")</code> and it will be shown in the renderer logs when the game is being rendered </li>
  <li><code>void clearLog()</code> </li>
  <li><code>List{`<`}SpawnDetail{`>`} getSpawnPositions()</code> </li>
  <li><code>Map{`<`}Integer, Integer{`>`} getPlayerSetTargets()</code> </li>
  </ul>
  </TabItem>
</Tabs>

## AttackerType (Python Specific)

- `hp: int`
- `range: int`
- `attack_power: int`
- `price: int`
- `speed: int`
- `is_aerial: int`

## DefenderType (Python Specific)

- `hp: int`
- `range: int`
- `attack_power: int`
- `price: int`
- `is_aerial: int`

## Attributes (C++ and Java Specific)

This class stores the attributes for `Attacker` and `Defender` . This will be used as the value type in Constants for storing attributes of Attacker and Defender types.

<Tabs>
  <TabItem value="C++" label="C++" default>
    <ul>
      <li>
        <code>unsigned hp</code>
      </li>
      <li>
        <code>unsigned range</code>
      </li>
      <li>
        <code>unsigned attackPower</code>
      </li>
      <li>
        <code>unsigned speed</code> (to be ignored for Defender)
      </li>
      <li>
        <code>unsigned price</code>
      </li>
      <li>
        <code>unsigned is_aerial</code>
      </li>
      <li>
        <code>unsigned weight</code>
      </li>
      <li>
        <code>unsigned ability_activation_cost</code>
      </li>
    </ul>
  </TabItem>
  <TabItem value="Java" label="Java">
    <ul>
      <li>
        <code>int hp</code>
      </li>
      <li>
        <code>int range</code>
      </li>
      <li>
        <code>int attack_power</code>
      </li>
      <li>
        <code>int speed</code> (to be ignored for Defender)
      </li>
      <li>
        <code>int price</code>
      </li>
      <li>
        <code>int is_aerial</code>
      </li>
      <li>
        <code>unsigned weight</code>
      </li>
      <li>
        <code>unsigned ability_activation_cost</code>
      </li>
    </ul>
  </TabItem>
</Tabs>

## SpawnDetail (Java Specific)

- `int getTypeId()` : Returns the typeId of the spawn
- `Position getPos()`: Returns the position of the spawn
