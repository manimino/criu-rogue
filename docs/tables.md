# Rogue Tables

## Monsters

There are five special types that a monster can have.

- M for "mean". Mean monsters may attack without provocation.
- F for "flying". Flying monsters are more difficult to hit.
- R for "regeneration". These monsters can regenerate health.
- G for "greedy". Greedy monsters attempt to pick up gold when you enter a room.
- I for "invisible".

| Name           | Treasure  | Types  | Exp   | HP    | AC  | Damage        | Range  | Notes                     |
|----------------|-----------|--------|-------|-------|-----|---------------|--------|---------------------------|
| Aquator        | 0         | M      | 20    | 5d8   | 2   | 0d0/0d0       |        | Rusts armor               |
| Bat            | 0         | F      | 1     | 1d8   | 3   | 1d2           |        | Flies randomly            |
| Centaur        | 15        |        | 17    | 4d8   | 4   | 1d2/1d5/1d5   |        |                           |
| Dragon         | 100       | M      | 5000  | 10d8  | -1  | 1d8/1d8/3d10  |        | Ranged 6d6 flame attack   |
| Emu            | 0         | M      | 2     | 1d8   | 7   | 1d2           |        |                           |
| Venus Flytrap  | 0         | M      | 80    | 8d8   | 3   | special       |        | Traps player              |
| Griffin        | 20        | MFR    | 2000  | 13d8  | 2   | 4d3/3d5       |        |                           |
| Hobgoblin      | 0         | M      | 3     | 1d8   | 5   | 1d8           |        |                           |
| Ice monster    | 0         |        | 5     | 1d8   | 9   | 0d0           |        | Freezes player            |
| Jabberwock     | 70        |        | 3000  | 15d8  | 6   | 2d12/2d4      |        |                           |
| Kestrel        | 0         | MF     | 1     | 1d8   | 7   | 1d4           |        |                           |
| Leprechaun     | 0         |        | 10    | 3d8   | 8   | 1d1           |        | Steals gold               |
| Medusa         | 40        | M      | 200   | 8d8   | 2   | 3d4/3d4/2d5   |        | Confuses Hero             |
| Nymph          | 100       |        | 37    | 3d8   | 9   | 0d0           |        | Steals magic item         |
| Orc            | 15        | G      | 5     | 1d8   | 6   | 1d8           |        | Greedy - runs toward gold |
| Phantom        | 0         | I      | 120   | 8d8   | 3   | 4d4           |        | Invisible                 |
| Quagga         | 0         | M      | 15    | 3d8   | 3   | 1d5/1d5       |        |                           |
| Rattlesnake    | 0         | M      | 9     | 2d8   | 3   | 1d6           |        | Reduces Strength          |
| Snake          | 0         | M      | 2     | 1d8   | 5   | 1d3           |        |                           |
| Troll          | 50        | RM     | 120   | 6d8   | 4   | 1d8/1d8/2d6   |        |                           |
| Ur-vile        | 0         | M      | 190   | 7d8   | -2  | 1d9/1d9/2d9   |        |                           |
| Vampire        | 20        | RM     | 350   | 8d8   | 1   | 1d10          |        | Drains Max HP             |
| Wraith         | 0         |        | 55    | 5d8   | 4   | 1d6           |        | Drains exp                |
| Xeroc          | 30        |        | 100   | 7d8   | 7   | 4d4           |        | Imitates an object        |
| Yeti           | 30        |        | 50    | 4d8   | 6   | 1d6/1d6       |        |                           |
| Zombie         | 0         | M      | 6     | 2d8   | 8   | 1d8           |        |                           |

### Special Monsters

Ice monsters have a freeze rate based on your level, HP, strength, and armor. Each time they freeze you, you have a small chance to instantly die of hypothermia. Ranged weapons are preferred here.

The Aquator does no damage, so remove your armor if you see one.

The Nymph is guaranteed to drop an item. It's often a good potion or scroll. Worth using your ranged weapons there.

The Vampire has a low chance to drain 1HP each time it hits.
Not too scary.

## Weapons

| Weapon            | Damage      | Notes                                  |
|-------------------|-------------|----------------------------------------|
| Mace              | 2d4         |                                        |
| Long sword        | 3d4         |                                        |
| Short bow         | 1d1         |                                        |
| Arrow             | 2d3         | Takes bonuses from equipped short bow. |
| Dagger            | 1d6         | 1d4 thrown                             |
| Two handed sword  | 4d4         |                                        |
| Dart              | 1d3 thrown  |                                        |
| Shuriken          | 2d4 thrown  |                                        |
| Spear             | 2d3         | 1d6 thrown                             |

Finding an early Long Sword or Two Handed Sword will make the game much
easier. 

Wielding a cursed short bow will utterly cripple you. Just stick with your starting bow, don't try on a new one.

## Armor

| Name             | Armor    |
|------------------|----------|
| Leather          | 3        |
| Ring mail        | 4        |
| Studded leather  | 4        |
| Scale mail       | 5        |
| Chain mail       | 6        |
| Splint mail      | 7        |
| Banded mail      | 7        |
| Plate mail       | 8        |

## Scrolls

| Item                          | %chance  | Description                                                                                                               |
|-------------------------------|----------|---------------------------------------------------------------------------------------------------------------------------|
| Monster confusion             | 7        | Your hands begin to glow red. Next melee attack confuses a monster.                                                       |
| Magic mapping                 | 4        | Reveals the entire map; objects are still hidden                                                                          |
| Hold monster                  | 2        | Freezes adjecent monsters.                                                                                                |
| Sleep                         | 3        | Sleepts reader for 4-8 turns.                                                                                             |
| Enchant armor                 | 7        | Your armor glows blue for a moment. Improved protection by 1.                                                           |                                                                                           |
| Identify scroll  | 10       | Identifies any item.                                                                                         |
| Scare monster                 | 3        | When read, you hear maniacal laughter in the distance. To use the scroll, drop it; monsters can't hit you on that spot. |
| Food detection                | 2        | Your nose tingles. Detects food on the current level.                                                                     |
| Teleportation                 | 5        | Teleports to a random location on the map.                                                                                |
| Enchant weapon                | 8        | Your (weapon) glows blue for a moment. Increases hit or damage bonus by 1.                                                |
| Create Monster                | 4        | Summons a monster on an adjecent tile. If it fails, you hear a faint cry of anguish in the distance.                      |
| Remove curse                  | 7        | You feel as if somebody is watching over you. Removes curses from equipped items.                                         |
| Aggravate monsters            | 3        | You hear a high pitched humming noise.. Alerts all monsters on the map.                                                   |
| Protect armor                 | 2        | Your armor is covered by a shimmering gold shield. Prevents rust damage from aquators.                                    |

## Potions

| Item               | %chance  | Description                                                                             |
|--------------------|----------|-----------------------------------------------------------------------------------------|
| Confusion          | 7        | Confuses the player for 19-21 turns                                                     |
| Hallucination      | 8        | Causes hallucinations for 850 turns - can't recognize monsters or items                 |
| Poison             | 8        | Reduces strength by 1-3 points.                                                         |
| Gain strength      | 13       | Increases strength by 1.                                                                |
| See invisible      | 3        | This potion tastes like slime mold juice. Reveals Phantoms.                             |
| Healing            | 13       | Heals 1df per character level. Increase max HP by 1 if you are at full health.          |
| Monster detection  | 6        | Reveals monsters on the map.                                                            |
| Magic detection    | 6        | Reveals magic items on the map.                                                         |
| Raise level        | 2        | Increases experience level by 1.                                                        |
| Extra healing      | 5        | Heals 1d8 per character level. Increase max HP by 1, or by 2 if you are at full health. |
| Haste self         | 5        | Hastens player for 4-8 turns.                                                           |
| Restore strength   | 13       | Hey, this tastes great. It make you feel warm all over. Restores strength to maximum.   |
| Blindness          | 5        | Blinds player for 807-892 turns                                                         |
| Levitation         | 6        | Levitates for 29-32 turns                                                               |

## Rings

| Item               | %chance  | Description                                                                       |
|--------------------|----------|-----------------------------------------------------------------------------------|
| protection         | 9        | Adds to defense and magical saving throws                                         |
| Add strength       | 9        | Adds to strength                                                                  |
| Sustain strength   | 5        | Prevents poison from reducing strength                                            |
| Searching          | 10       | Helps detect secret doors and traps.                                              |
| See invisible      | 10       | Reveals Phantoms.                                                                 |
| Adornment          | 1        | Worth 10 gold.                                                                    |
| Aggravate monster  | 10       | Cursed. Causes monsters to attack more agressively.                               |
| Dexterity          | 8        | Improves weapon accurracy.                                                        |
| Increase damage    | 8        | Increases weapon damage.                                                          |
| Regeneration       | 4        | Heals 1 hp per turn                                                               |
| Slow digestion     | 9        | Reduces food consumption by about 50%. Two rings can cancel out food consumption. |
| Teleportation      | 5        | Cursed. Randomly teleports the player around the map.                             |
| Stealth            | 7        | Allows player to move without rousing sleeping monsters.                          |
| Maintain armor     | 5        | Prevents rust damage                                                              |


## Wands and Staves

| Item           | %chance  | Description                                                                                        |
|----------------|----------|----------------------------------------------------------------------------------------------------|
| Light          | 12       | Has 10-19 charges. Illuminates the room.                                                           |
| Invisibility   | 6        | Makes a monster invisible.                                                                         |
| Lightning      | 3        | Inflicts 6d6 damage for up to 6 tiles. Bounces off walls.                                          |
| Fire           | 3        | Inflicts 6d6 damage for up to 6 tiles. Bounces off walls. Dragons are immune.                      |
| Cold           | 3        | Inflicts 6d6 damage for up to 6 tiles. Bounces off walls. Yetis are immune.                        |
| Polymorph      | 15       | Changes a monster type.                                                                            |
| Magic missile  | 10       | Inflicts 1d4 damage on a single target.                                                            |
| Haste monster  | 10       | Hastens a monster.                                                                                 |
| Slow monster   | 11       | Slows a monster.                                                                                   |
| Drain life     | 9        | Drains half of the hero's hp, then removes the same amount of health evenly from visible monsters. |
| Nothing        | 1        | Doesn't do anything.                                                                               |
| Teleport away  | 6        | Teleports a monster randomly on the map.                                                           |
| Teleport to    | 6        | Causes the monster to teleport next to the player.                                                 |
| Cancellation   | 5        | Supresses monster's special abilities.                                                             |

## Level Up

Each level gives you 3 to 9 more HP (average 6).


## Messages

 - A cloak of darkness falls around you. (! Blindness)
 - A gush of water hits you on the head. (^ Rust)
 - A small dart just hit you in the shoulder. (^ Poison Dart)
 - A small dart whizzes by your ear and vanishes. (^ Poison Dart)
 - A sting momentarily weakens you. (= Sustain Strength)
 - A strange white mist envelops you and you fall asleep. (^ Sleeping Gas)
 - An arrow shoots past you. (^ Arrow)
 - Bummer, this food tastes awful. (: Ration of Food. Only if it tastes awful.)
 - Hey, this tastes great. It makes you feel warm all over. (! Restore Strength)
 - My, that was a yummy ... (: Slime-Mold)
 - Nothing happens. (/ Any. Only if its charges are exhausted.)
 - Oh, bummer! Everything is dark! Help! (! Blindness)
 - Oh no! An arrow shot you. (^ Arrow)
 - Oh, now this scroll has a map on it. (? Magic Mapping)
 - Oh, wow! Everything seems so cosmic! (! Hallucination)
 - Oh, wow, that tasted good. (: Food.)
 - Oh, wow! You're floating in the air! (= Levitation)
 - The ... appears confused (? Monster Confusion. Only after you hit a monster.)
 - The ... freezes. (? Hold Monster. V5 only.)
 - The bolt bounces. (/ Lightning)
 - The bolt whizzes by you (/ Lightning. Only if it bounces off a wall or monster.)
 - The corridor glows and then fades. (/ Light. Only if you are standing in a passage.)
 - The flame bounces (/ Fire. Only if it bounces off a wall or monster.)
 - The flame whizzes by you (/ Fire. Only if it bounces and misses you.)
 - The ice bounces (/ Cold. Only if it bounces off a wall or monster.)
 - The ice whizzes by you (/ Cold. Only if it bounces and misses you.)
 - The missile vanishes with a puff of smoke. (/ Magic Missile. Only if the monster counters your magic.)
 - The monsters around you freeze. (? Hold Monster.)
 - The room is lit by a shimmering blue light. (/ Light)
 - The rust vanishes instantly. (= Maintain Armor; ? Protect Armor.)
 - The scroll turns to dust as you pick it up. (? Scare Monster. Only if you previously dropped it.)
 - The veil of darkness lifts. (! Blindness. Only when the potion wears off or you drink ! Healing, ! Extra Healing, or in V5 ! See Invisible.)
 - This potion tastes extremely dull (! Thirst Quenching)
 - This potion tastes like ... juice. (! See Invisible)
 - This scroll is an identify scroll. (? Identify)
 - This scroll seems to be blank. (? Blank Paper)
 - Wait, what's going on here. Huh? What? Who? (! Confusion)
 - What a trippy feeling! (! Confusion)
 - You are caught in a bear trap. (^ Bear Trap)
 - You are hit by the bolt. (/ Lightning. Only when the bolt bounces off a wall.)
 - You are too weak to use it. (/ Drain Life. Only when you are down to 1 hit point.)
 - You begin to feel better (! Healing)
 - You begin to feel greedy and you sense gold. (? Gold Detection)
 - You begin to feel much better. (! Extra Healing)
 - You can move again. (! Paralysis. Only after the potion wears off.)
 - You can't move. (! Paralysis)
 - You feel a pull downward. (? Gold Detection. Only when there is no gold on the current level.)
 - You feel a strange sense of loss. (? Enchant Armor or ? Enchant Weapon. Only if you are not using any. In V5 also ? Protect Armor or ? Hold Monster.)
 - You feel a wrenching sensation in your gut. (, Amulet of Yendor)
 - You feel as if somebody is watching over you. (? Remove Curse)
 - You feel in touch with the Universal Oneness. (? Remove Curse)
 - You feel momentarily sick. (! Poison. Only if you are wearing = Sustain strength.)
 - You feel stronger, now. What bulging muscles! (! Gain Strength)
 - You feel very sick now. (! Poison)
 - You feel yourself moving much faster. (! Haste Self)
 - You feel yourself slowing down (! Haste Self. Only when the potion wears off.)
 - You fell into a trap! (^ Trap Door)
 - You have a strange feeling for a moment, then it passes. (! Magic Detection or Monster Detection. Only when there is nothing to detect.)
 - You have a tingling feeling. (/ Drain Life. Only when no monsters are in the room.)
 - You have been granted the boon of genocide. (? Genocide)
 - You hear a faint cry of anguish in the distance. (? Create Monster. Only when you are already surrounded.)
 - You hear a high-pitched humming noise. (? Aggravate Monsters)
 - You hear maniacal laughter in the distance. (? Scare Monster)
 - You sense the presence of magic on this level. (! Magic Detection)
 - You start to float in the air. (= Levitation)
 - You suddenly feel much more skillful. (! Raise Level)
 - Your ... glows blue for a moment. (? Enchant Weapon)
 - Your armor glows faintly for a moment. (? Enchant Armor)
 - Your armor glows silver for a moment. (? Enchant Armor)
 - Your armor is covered by a shimmering gold shield. (? Protect Armor)
 - Your hands begin to glow red (? Monster Confusion)
 - Your hands stop glowing red (? Monster Confusion. Only after you hit a monster.)
 - Your nose tingles and you smell food. (? Food Detection)
 - Yuk, this food tastes awful (: Ration of Food. Only if it tastes awful.)
 - Yum, that tasted good. (: Ration of Food) 