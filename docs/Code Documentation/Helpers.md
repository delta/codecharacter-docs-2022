---
sidebar_position: 6
---

# Helper functions

import Tabs from "@theme/Tabs";
import TabItem from "@theme/TabItem";

<Tabs>
  <TabItem value="C++" label="C++" default>
  <ul>
  <li><code>bool is_valid_spawn_position(int x, int y)</code>: Given x and y coordinate value, it will return whether it is a valid spawn position coordinate or not</li>
  <li><code>bool is_valid_spawn_position(Position pos)</code>: Given a Position, it will return whether it is a valid spawn position</li>
  <li><code>std::vector{`<`}Position{`>`} get_all_valid_spawn_positions()</code>: Returns all the valid spawn positions</li>

  </ul>

  </TabItem>
  <TabItem value="Python" label="Python">
  <ul>
  <li><code>is_valid_spawn_position(pos: Position) -> bool</code>: Given a Position, it will return whether its a valid spawn position</li>
  </ul>
  <li><code>get_all_valid_spawn_positions() -> List[Position]</code>: Returns all valid spawn positions</li>
  </TabItem>
  <TabItem value="Java" label="Java">
  <ul>
  <li><code>boolean Helpers.isValidSpawnPosition(Position position)</code>: Given a Position,it will return whether its a valid spawn position</li>
  <li><code>Set{`<`}Position{`>`} Helpers.getAllValidSpawnPositions()</code>: Returns all valid spawn positions</li>
  </ul>
  </TabItem>
</Tabs>
