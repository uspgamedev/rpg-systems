
# **Tiered Bounded Accuracy** Proposal

## Tier 1

This is classic bounded accuracy. Most of it is based on the following table,
copied from [this article][1]:

| DC/AC | Difficulty         | To Break           | Armor | To Hit        |
| ----- | ------------------ | ------------------ | ----- | ------------- |
| 5     | Very Easy          | glass bottle       |       | inanimate obj |
| 10    | Easy               | wooden chair       | None  | badger        |
| 15    | Medium             | simple door        | Light | troll         |
| 20    | Hard               | small chest        | Full  | dragon        |
| 25    | Very Hard          | treasure chest     |       | tarrasque     |
| 30    | Nearly Impossible  | masonry wall 1 ft  |       | deity         |

### Player growth

| Aspect        | Range/Growth                  |
| ------------- |:-----------------------------:|
| Level         | 1..20                         |
| AC¹           | 11..12 / 12..15 / 14..18 / 2  |
| Hit Points    | 11..163 (1d8, CON 15)         |
| Attack Bonus  | +2/+3..+6/+5 (prof/attr)      |
| Damage/Round  | 9..125(90-160)                |
| Proficiency   | +2..+6                        |

¹ light/medium/heavy/shield

Each line in the table is explained below.

#### Level

Self explanatory.

#### Armor Class

TODO

#### Hit Points

TODO

#### Attack Bonus

TODO

#### Damage Per Round (DPR)

Following the procedure to calculate a monster's "overall damage output"
(DMG 278), we consider a player's DPR to be the average of the damage outputs of
its first three rounds in a battle immediately after a long rest choosing the
most effective attacks greedily. Let's consider a few concrete cases of level
20 characters.

First, a Battle Master Fighter. There are four attacks per round, plus two
extra Attack actions due to Action Surge. Additionally, the first six attacks
may be enhanced by maneuvers that add a superiority die to the damage roll and
are triggered when a target is hit (e.g. Distracting Strike). Let's assume a
Maul (2d6 blunt damage) is used for the attack. The damage is thus calculated:

+ First round (two actions => eight attacks, first six maneuvered):
  + 6x (2d6 + 5 + 1d12) = 6x (7 + 5 + 6.5) = 6x (18.5) = 111
  + 2x (2d6 + 5) = 2x (7 + 5) = 2x (12) = 24
  + Total: 135
+ Second round (two actions => eight attacks, no maneuvers):
  + 8x (2d6 + 5) = 8x (7 + 5) = 8x (12) = 96
+ Third round (four attacks):
  + 4x (2d6 + 5) = 4x (7 + 5) = 4x (12) = 48
+ Overall damage output: (135 + 96 + 48)/3 = 93

Next, we'll analyze an Evocation Wizard. This means Empowered Evocation is in
play, adding +5 (WIS modifier) to all evocation damage rolls. Since there is
only one 9th and 8th level spell slot, and the most damaging high-level spells
are:

+ Meteor Swarm (9th level, AoE): 20d6 fire damage + 20d6 blunt damage
+ Sunburst (8th level, AoE): 12d6 radiant damage
+ Delayed Blast Fireball (7th level, AoE): 12d6 fire damage
+ Mordenkainen's Sword (7th level): 3d10 force damage at first and as bonus
  action during concentration (1 minute)
+ Prismatic Spray (7th level, AoE): 10d6 random type damage

Considering that AoE spells have double the damage output (which assumes they
hit at least two enemies), the most effective three-round sequence is to cast
Mordenkainen's Sword, Meteor Swarm then Sunburst, using the bonus actions to
deal extra damage with the summoned Sword:

+ First round (Mordenkainen's Sword, two attacks):
  + 2x (3d10 + 5) = 2x (16.5 + 5) = 2x (21.5) = 43
+ Second round (Meteor Swarm + Sword):
  + 2x (20d6 + 5) = 2x (70 + 5) = 150
  + 3d10 + 5 = 21.5
  + Total: 2x150 + 21.5 = 321.5
+ Third round (Sunburst + Sword):
  + 12d6 + 5 = 42 + 5 = 47
  + 3d10 + 5 = 21.5
  + Total: 2x47 + 21.5 = 115.5
+ Overall damage output: (43 + 321.5 + 115.5)/3 = 160

#### Proficiency

As per the "Character Advancement" Table (PHB 15).

---

### Environment growth

TODO

---

---

## Tier 2

### Player growth

| Aspect        | Range/Growth                  |
| ------------- |:-----------------------------:|
| Level         | 21-30                         |
| AC            | +5 armors / +2 shields        |
| Hit Points    | 2 hit die per level (200-400) |
| Attack Bonus  | +10 (+3 prof/+5 attr/+2 ???)  |
| Damage/Round  | 125(90-160) to 260(130-400)   |
| Proficiency   | 7-9 (+3)                      |

### Environment growth

| Aspect        | Range/Growth                  |
| ------------- |:-----------------------------:|
| CR            | 30-50                         |
| AC/DC         | +10 to difficulty ranks       |
| Ht Points     | +135 per CR (985-2150)        |
| Attack Bonus  | +15 to +21                    |
| Damage/Round  | 400-600                       |
| Proficiency   | 9-14 (+5)                     |

[1]:https://olddungeonmaster.wordpress.com/2014/08/30/bounded-accuracy/
