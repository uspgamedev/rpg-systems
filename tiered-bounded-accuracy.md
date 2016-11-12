
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
| AC*           | 11..12 / 12..15 / 14..18 / 2  |
| Hit Points    | 11..163 (1d8, CON 15)         |
| Attack Bonus  | +2/+3..+6/+5 (prof/attr)      |
| Damage/Round  | 9..50                         |
| Proficiency   | +2..+6                        |

***** light/medium/heavy/shield

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

The hardest part to calculate from player growth is the damage output per round,
as it wildly varies from class to class. Here we considered to extremes:
Fighters and Wizards. While the former's main source of damage comes from its
multiple attacks and eventual maneuvers, the latter has a whole set of spells at
its disposal. At first, we considered the mean damage of a 9th level spell, but
that does not reflect damage per round properly, since each wizard has only one
9th level spell slot, and thus can only cast one 9th level spell between long
rests.

We do know that a Fighter has a Damage/Round mean of 50 because it has four
attacks and possibly some superiority die to add to the damage. That is:

+ Normal attack: 1d10 + 5/1d10 + 5/1d10 + 5/1d10 + 5 (mean 44)
+ Every maneuvered attack gets +1d12 damage (mean +6.5)

If we consider that a level 20 Fighter has six d12 superiority dies, and that
they recover every short rest, then a rough guess is that they can use maneuvers
60% of the time (10 rounds per short rest, 30 per day). The final mean damage
output per round is:

+ 0.6 x 50.5 + 0.4 x 44 = 47.9

By a similar logic, a Wizard with 30 rounds per long rest, fighting greedily,
would use up its spell slots from the strongest to the weakest until only
cantrips are left. Following the "One Target" column from the "Spell Damage"
Table (DMG 284), that makes:

+ (15d10 + 12d10 + 2 x (11 + 10)d10 + 3 x (8 + 6 + 5 + 3)d10 + 4 x 2d10 + 8 x 1d10)/30
+ = (15 + 12 + 2 x (11 + 10) + 3 x (8 + 6 + 5 + 3) + 4 x 4 + 8)d10/30
+ = (27 + 42 + 72 + 24) x 5.5 / 30
+ = (69 + 96) x 5.5 / 30
+ = 165 x 5.5 / 30
+ = 30.25

Which is actually lower than the Fighter's DPR!

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
| Damage/Round  | 120(60-180) to 260(130-400)   |
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
