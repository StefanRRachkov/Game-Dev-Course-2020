# Knight's Vow

## Description
The game was made to be clone of the famous The Binding of Isaac, so it resembles it a bit. It's a rouglike adventure game by genre. You are a knight which should enter a dungeon go through it and beat the final boss which is a Death Knight. After that the game ends and sends the player to the main menu. The dungeons are generated on the go and also are the positions of the enemies which makes the game slightly more replayable.

## PCG - Why and How
The procedural generated content gives the programmer the ability to make certain rules that when applied will save you a great ammount of time. For the project the dungeon creation was proceduraly generated and this helped me with the lack of level designing experience. For the generation of the dungeon I used the concept of Regualar Grammars.

## What is a regular grammar
A Regular grammar is a grammar that produces a regular language it's a structure G = <N = Variables, E = Set, S = Starting Variable, P = Rules>. In the theory E is also called terminal variables and N are non-terminal variables. P = (N x N) u (N x E). So what does that mean - one non-terminal variable will lead to another non-terminal variable or to one terminal variable. The S is the first rule or where the grammar will start and to finish it needs to end in an element of E (the Set).

## How is it implemented
| Part of the grammar | What is it in the game |
| :-: | :-: |
| N - non-terminal variables | In our case all the rooms that can lead to another room are part of the non-terminal variables because the generation will not stop with them |
| E - terminal variables | The set is constructed of all the possible rooms and E is constructed by all the rooms that don't have room for avaible spawn points for another room, because with them the generation will stop |
| S - starting variable | If we follow the rule that S should be an element of N we are okay because S is also a room that can lead to another room and it is the only one that can lead to room in all directions |
| P - Rules | The rules are actually codded into the spawn points - If one point collides with another it spawnes a terminal variable (a closed room), if one point collides with a room it destroys the point and the room becomes a terminal variable, in one point doesn't collide it will remain still until on it the algorithm spawns anoter room so it remains in the set of non-terminal variables |

## Enemies
| Enemy | Attack type | Image |
| :-: | :-: | :-: |
| Orc | Melee | ![3_enemies_1_idle_001](https://user-images.githubusercontent.com/25185815/132091495-7298a218-836e-4d79-80cb-823fc3408e66.png) |
| Murder Ghost | Range | ![9_enemies_1_idle_000](https://user-images.githubusercontent.com/25185815/132091520-c28e6b3b-a0bf-48b6-a734-64ec3cc8e4d0.png) |
| Scorpio | Melee | ![1_enemies_1_idle_000](https://user-images.githubusercontent.com/25185815/132091556-f0d16ef5-fc18-4461-b01b-bdb90e64611a.png) |
| Death Knight | Melee | ![10_enemies_1_idle_000](https://user-images.githubusercontent.com/25185815/132091587-95ebe4c3-9cf8-424e-9972-7b714eda7d2d.png) |

## Images
### Main Menu
![Main Menu](https://user-images.githubusercontent.com/25185815/132091618-9caeaa43-102f-4091-986e-a08541a52f6f.PNG)
### Starting Position
![Knight's Vow](https://user-images.githubusercontent.com/25185815/132091632-0b3a5faf-7fbe-417b-ab62-2c3eeea548e4.PNG)
### Fight aftermath
![Knight's Vow Enemies](https://user-images.githubusercontent.com/25185815/132091640-a72a6b09-b65b-4215-a899-096e04a3b07f.PNG)
### Final Boss Fight
![Boss Fight](https://user-images.githubusercontent.com/25185815/132091648-daa59025-0aaa-4793-8824-14432fe404d4.PNG)

