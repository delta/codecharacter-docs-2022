---
sidebar_position: 2
---

# Constants

All are similarly named variables just with similar type signatures in all the languages. The usage will be different depending on the language.

- NO_OF_TURNS
- MAX_NO_OF_COINS
- NO_OF_ATTACKER_TYPES
- ATTACKER_TYPE_ATTRIBUTES
- MAP_NO_OF_ROWS
- MAP_NO_OF_COLS

import Tabs from "@theme/Tabs";
import TabItem from "@theme/TabItem";

<Tabs>
  <TabItem value="C++" label="C++" default>
  <ul>
  <li><code>size_t Constants::MAP_NO_OF_ROWS </code> </li>
  <li><code>size_t Constants::MAP_NO_OF_COLS </code> </li>
  <li><code>size_t Constants::NO_OF_ATTACKER_TYPES </code> </li>
  <li><code>size_t Constants::NO_OF_TURNS </code> </li>
  <li><code>size_t Constants::MAX_NO_OF_COINS </code> </li>
  <li><code>std::unordered_map{`<`}size_t, Attributes{`>`} Constants::ATTACKER_TYPE_ATTRIBUTES</code></li>
  </ul>

  </TabItem>
  <TabItem value="Python" label="Python">
  <ul>
    <li><code>Constants.MAP_NO_OF_ROWS: int</code></li>
    <li><code>Constants.MAP_NO_OF_COLS: int</code></li>
    <li><code>Constants.NO_OF_ATTACKER_TYPES: int</code></li>
    <li><code>Constants.NO_OF_TURNS: int</code></li>
    <li><code>Constants.MAX_NO_OF_COINS: int</code></li>
    <li><code>Constants.ATTACKER_TYPE_ATTRIBUTES: Dict[int, AttackerType]</code></li>
  </ul>
  </TabItem>
  <TabItem value="Java" label="Java">
  <ul>
    <li><code>int Constants.MAP_NO_OF_ROWS</code></li>
    <li><code>int Constants.MAP_NO_OF_COLS</code></li>
    <li><code>int Constants.NO_OF_ATTACKER_TYPES</code></li>
    <li><code>int Constants.NO_OF_TURNS</code></li>
    <li><code>int Constants.MAX_NO_OF_COINS</code></li>
    <li><code>Map{`<`}Integer, Attributes{`>`} Constants.ATTACKER_TYPE_ATTRIBUTES</code></li>
  </ul>
  </TabItem>
</Tabs>
