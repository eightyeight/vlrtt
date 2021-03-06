# vlrtt TODO

**Spoilers.** Don't read this if you want to be shocked and amazed by the final product.

## Gameplay

Need to make some gameplay :P.

### Less shooting

 * Focus on melee combat
 * A melee engagement should be based on stamina/skill
 * High skill makes enemy's stamina decrease faster
 * When a character's stamina is gone, they take a blow
 * Blows do _lots_ of damage
 * After taking a blow a character regains some stamina (adrenaline)

Stamina is on the order of 0-100 for normal combatants.
Skill is on the order of 0-10.
In single combat, loss of stamina per second `sps = 5 * max(1, skill of enemy - skill)`.

For example, fresh opponents of stamina 100 and equally-matched skill will take 10 seconds to come to blows.
In the case that two characters reach zero stamina at the same moment, a random character takes a blow,
or they may both take a light blow.
If one character had a skill of 10 and the other of 0, the combat would be over in 2 seconds,
and the more-skilled character would have lost 10 stamina.

Possibility: random 'blunders' dependent on character skill and weapons?
Could be frustrating.
Effects could be anything from an instant blow to a stamina reduction.

### Special abilities

Not sure how much I want to get into this, but there could be some cool ideas:

 * Invisibility for a character allowing them to ambush
 * Instant blow against enemies who are attacking someone else and are interrupted
 * Defensive move that replenishes stamina
 * Strike a blow when an enemy disengages
 * Enemies flee when outnumbered or when their buddy is killed

### Weapons

Using different weapons could be cool.
Different statistics could be expressed in terms of a stamina penalty for using them.
Although what would be the benefits?

 * Stamina penalty on enemies as well
 * Increased damage (but I want every blow to be potentially deadly anyway)
 * Special effects like stunning?

### Mage

 * Healing spell
 * Magic missile that reduces stamina (and health?) (instantly drains stamina?)
 * Possible: missile takes time to recharge... how long?
 * Possible: missile prevents healing for some time

## Environment

The linear level has been replaced with a circular arena, but it needs to be filled with stuff.
It's also got rocks to cover the ground, so you can sort of see what's going on in all the white.

 * Henge: rocks arranged in a ring
 * Trees: randomly placed
 * Ruins: somehow

### Scenarios

The scenario defines how enemies spawn in the arena.
Scenarios should probably be wave-based so they can switch at defined intervals.

 * Ambush - enemies spawn from inside some sort of object?
 * Camp - enemies are clustered somewhere and not really paying attention to you
 * Barricade - enemies are entrenched, and wait for you to come to them
 * Charge - enemies spawn at the other end and attack you

Maybe implement a high-level state machine that throws some sequence of scenarios at you to provide an overall engagement.
And finish with a final boss.

### Enemies

 * Normal guys with melee combat
 * Big guys with low skill but high stamina

### Final boss

 * Unique spells
 * Unique-ish environment
