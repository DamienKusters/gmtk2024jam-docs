![](attachments/Pasted%20image%2020240817125308.png)

## Pitch
You play as a kraken, having to eat entities in order to grow the max length of your body.
The growth will be significant, reaching far into the sky and eventually in space where you need to eat cosmic constructions like other planets in order to keep growing your body.
You need to grab and pull entities out of the air and drag them back to a mouth on the bottom of the screen in order to grow.
- Evade projectiles
- Grow by eating anything in your path
You start off small as a single cell organism, eventually growing to cosmic sizes.

Gameplay: Bullethell

## Inspiration
- [Feed Me](https://www.gameflare.com/online-game/feed-me/)
- [Shooting and Controls](https://www.youtube.com/watch?v=Ny5L3QVMOf8)
- [Effing Worms](https://www.crazygames.com/game/effing-worms)

## Audience
The game will contain gore as objects & entities are consumed.

## Concept
### Gameplay Overview
The Kraken's mouth stays on the bottom of the screen.
You can control one of its tentacles with the mouse, where the mouse goes is; where the tentacle tries to go.
The tentacle can only reach what's visible on screen.
Navigate the tentacle to entities with the mouse to grab hold of it, drag it back to the central mouth to consume the entity and grow in size/length.
![alt text](<attachments/Pasted image 20240817094559.png>)
![alt text](<attachments/Pasted image 20240817094710.png>)
### GMTK theme
The theme: **Built to Scale**
Grow the kraken to cosmic scale by devouring everything it comes across. Maybe even looping around space/time to get back to the original starting position.
### Game Mechanics
#### Primary
##### Entities
Navigate the tentacle to an entity and grab hold of it to drag it back to the central mouth to consume it. There are multiple types of entities.
###### Static Entities
Static entities consist of:
- Blood cells
- Ants
- Houses/ trees/ flats / buildings
- Planets
- Solar systems
None of them can attack or defend themselves, but are there to allow quicker growth. Some of them may try to get away.
###### Dangerous Entities
Dangerous entities consist of:
- White blood cells (fighters)
- Birds
- Planes/Helicopters
- ~~Comets~~
	- Comets will become non-dangerous entities
	- Use UFOs instead as enemies in space
- Gods/Celestial beings?

Such entities can attack with projectiles

- Birds will fly over and dump their 'droppings' above the player's tentacle.
- Planes, same as birds will also shoot forward, requiring more skill to evade.
- Helicopters may hover in place and shoot directly at the tentacle
- Comets will randomly appear from different angles
	- https://www.youtube.com/watch?v=DF5_k5TAZPc

##### Projectiles
Projectiles are emitted from dangerous entities. They can't be grabbed and will damage the Kraken when coming into collision with the `tip of the tentacle`.
The arm of the tentacle & the mouth piece is not damaged by projectiles.
- Reasons for this decision:
	- Evading projectiles is player skill based. If the mouth piece was included this could be unfair and needs to be balanced with an option to block.
	- Only the tip of the tentacle is affected, the rest of the tentacle is too large and also acts just as decoration.

Projectiles **MUST** be highly visible to be distinguished from entities. Use: shaders and/or trails

##### Stages
Stages of the game (Levels)
- Cell stage
	- Blood cells
		- Only float around (like comets, random angles)
	- White blood cells
		- Slow moving with slow moving dropping projectiles
- Grass/bug stage???
	- Flies
	- ants
	- Birds?
	- Grasses
- Civ stage
	- Houses/ Buildings
	- Birds
	- Airplanes
	- Helicopters
- Star system stage (combine with Galaxy stage?)
	- Planets
	- Comets
	- Ufos
- Galaxy stage
	- Galaxies
	- Dyson spheres
	- Black holes
- Celestial Stage
	- Gods
- Cell stage -> wraps back to beginning
##### Stage progression
A stage is essentially a particular amount of distance you will need to travel in order to continue.
Eating will add to that distance. This is in-game known as `dna score`.<br />
Different entities will periodically spawn based on the current `dna score` thus altitude.<br />
For simplicity, all stages require the same amount of `dna score`?
Based on spawning of entities, a stage could go faster.
Taking damage will always lower your `dna score` so you will shrink.

##### Eatable entities
Grab hold, and eat entities in order to grow in size.
##### Eatable dangerous entities
Will sometimes fly across the screen.
- Birds: horizontal, will do its 'droppings' as soon as the tentacle piece is below the bird.
- Planes: Same as birds will show up in higher altitudes. Droppings are bombs/packets, may also shoot forward?
- Different patterns to create a bullet-hell effect
##### Growth
The more you eat the larger you'll become. This is done by scaling the background and setting a requirement of how much you must eat in order to go to the next stage.
Taking damage will shrink you back down.
While growing, entities will stay in place relative to the scaling background, this causes certain entities to accidentally touch the mouth piece and be consumed. 
##### Taking damage
Questions:
- Should the mouth piece take damage?
	- Pros:
		- Tentacle must defend mouth piece by grapping or slapping projectiles away.
	- Cons:
		- You could play the game more wreck less, more slapping movement results in more projectiles being slapped away
- Should the tentacle take damage?
	- Pros:
		- During gameplay you must be agile and have quick mouse movements, seems to improve the risk/reward factor when trying to eat an Dangerous entity
		- Tentacle could be stunned 
	- Cons:
		- Differentiate between eatable entities and projectiles 
#### Secondary
##### Tentacle slows down when grabbing entities
Entities will have a weight factor influencing the speed of the tentacle. An planet for example, can be very heavy but will make you grow faster.
##### ~~Sizes of mouths~~
~~Your mouth will grow at set intervals during stages. It will increase the hitbox you have to eat entities,  but it will also make you more vulnerable to projectile damages.~~
##### Mouth grows based on size
The mouth will only grow for astatic purposes
##### ~~Shooting?~~
~~Add this to tentacle abilities?~~
##### Upgrades?
#todo Get to choose offense/defence upgrades?
Powerup: eat everything on screen.
##### Bosses?
#todo On certain altitudes bosses may appear, being defeated will lower you to a previous altitude?

## Art
Retro Flash game style?

## Audio
Cosmic/dread?

## User Experience
Mobile friendly
### Controls
The game is played by the mouse, you control the tip of the beast's tentacle.

## Game names
- The Cosmic Maw
- Eater of Eternity
- Harbinger of Hunger
- Cosmic Consumption
- Tentacle Tyrant

- Tendril
- Devourer of Worlds
- Eternal Hunger
- Perish
- cosmological horror 
- Kraken
- Kraking the Universe
- Kraken's Tentacular Adventures

---
## Remaining features
<u>**✅ = done**</u><br/>
<u>**🟦 = being worked on**</u>

| Prio | Asset                           | In game | State                 |
|------|---------------------------------|---------|-----------------------|
| M    | <u>**Name of the game**</u>     | ❌       | ❌                     |
| M    | <u>**Kraken sound: eating**</u> | ❌       | ❌                     |
| M    | <u>**Entity: Octopus**</u>      | ✅       | ❌Temporary asset used |
| M    | <u>**Entity: Drone**</u>        | ✅       | ❌Temporary asset used |
| S    | Entity: Sun                     | ❌       | ❌                     |
| S    | Kraken sound: hurt/damage       | ✅       | ❌Temporary asset used |
| S    | Kraken sound: roar              | ❌       | ❌                     |
| C    | Explosion sound                 | ❌       | ❌                     |
| C    | Stage icon: Cell stage          | ✅       | ❌Temporary asset used |
| C    | Stage icon: Ocean stage         | ✅       | ❌Temporary asset used |
| C    | Stage icon: Civilisation stage  | ✅       | ❌Temporary asset used |
| C    | Stage icon: Solar stage         | ✅       | ❌Temporary asset used |
| C    | Stage icon: Cosmic stage        | ❌       | ❌Temporary asset used |
| C    | - BGM Civilisation Stage        | ❌       | ❌                     |
| C    | - BGM Credits Stage             | ❌       | ❌                     |
| C    | Entity: Galaxy                  | ❌       | ❌                     |
| C    | Entity: Godlike being           | ❌       | ❌                     |
| W    | Mouth closed                    | ❌       | ❌                     |

| Prio | Asset                        | In game | State |
|------|------------------------------|---------|-------|
| M    | Tentacle neutral             | ✅       | ✅     |
| M    | Tentacle closed              | ✅       | ✅     |
| M    | Mouth neutral                | ✅       | ✅     |
| M    | Mouth open                   | ✅       | ✅     |
| M    | Background music             | ✅       | 🟦    |
| M    | Entity: Red blood cell       | ✅       | ✅     |
| M    | Entity: White blood cell     | ✅       | ✅     |
| M    | Entity: Killer Whale         | ✅       | ✅     |
| M    | Entity: Blowfish             | ✅       | ✅     |
| M    | Entity: Jet fighter          | ✅       | ✅     |
| M    | Entity: Attack helicopter    | ✅       | ✅     |
| M    | Entity: Planet               | ✅       | ✅     |
| M    | Entity: UFO                  | ✅       | ✅     |
| M    | Entity: Meteorite            | ✅       | ✅     |
| S    | Kraken sound: grabbing       | ✅       | ✅     |
| S    | Kraken sound: let go         | ✅       | ✅     |
| C    | Unique Background music(BGM) | ✅       | 🟦    |
| C    | - BGM Cell Stage             | ✅       | ✅     |
| C    | - BGM Ocean Stage            | ✅       | ✅     |
| C    | - BGM Solar Stage            | ❌       | 🟦    |

### External assets
Temporary assets used:
- https://godotshaders.com/shader/2d-outline-inline-configured-for-sprite-sheets/
- https://www.flaticon.com/free-icon/globe_13645767?term=planet&page=1&position=14&origin=search&related_id=13645767
- https://www.flaticon.com/free-icon/whale_2622034?term=whale&page=1&position=11&origin=search&related_id=2622034
- https://www.flaticon.com/free-icon/plane_723978?term=plane&page=1&position=51&origin=search&related_id=723978
- https://www.flaticon.com/free-icon/red-blood-cells_3055459?term=cell&page=1&position=12&origin=search&related_id=3055459
- https://opengameart.org/content/deep-sea-creatures
