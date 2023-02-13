# Elzda
*A videogame inspired by the original 1986 Legend of Zelda, written entirely in MIPS Assembly Language*
## Objective:
The goal of Elzda is to reach the golden, shiny bell, located behind three locked doors. Each door can be unlocked with a key; the three keys are hidden
throughout the world. Be careful, though, because dangerous monsters wander the world, ready to stop you. You can use a sword or a bomb to defeat these enemies. 
Additionally, you can use the bomb to destroy bushes or fences that stand in the way between you and a key. Like enemies, bombs can damage you. If you are damaged
three times, the game will end. If you manage to succeed and reach the bell, you've beat the game!

## Demo
https://www.youtube.com/watch?v=83sVATSKDxE

**Controls**: 
 * Arrow keys: Move. Press to change direction or step, hold to walk.
 * Z key: Use the sword. The sword can defeat enemies and clear bushes.
 * X key: Place a bomb. The bomb explodes after a short delay and destroys fences, enemies, and bushes in a '+' shape around where it detonated.
 * C key: Use key. The C key can unlock doors if you are facing the door and have a key.


## Implementation:
This game was written entire in MIPS Assembley language, using the MARS IDE.
The game consists of 8 files:
  * `constants.asm`: Holds constants including colors, display dimensions, and input keys
  * `display.asm`: Keypad and LED Display Simulator driver/API file
  * `game.asm`: Gameplay logic
  * `game_constants.asm`: Defines player constants (number of frames until the sword is done slashing, how many frames it takes for a player to move 1 tile, etc.), 
  tile types (brick, grass, flower, bush, etc.), and more
  * `macros.asm`: Includes macros such as `print_str` (prints a string to console) and `lstr` (puts a string literal into the .data segment and loads its address into a register
  * `map.asm`: Includes ASCII representation of the world map, maps characters to tile types, maps characters to object types, and loads the map
  * `obj.asm`: Allocates, frees objects such as keys, enemies, and bombs
  * `textures.asm`: Includes all textures, such as player and sword textures (for multiple directions, NESW), texture for hearts, tiles, etc
