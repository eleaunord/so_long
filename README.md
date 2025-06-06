# so\_long

## Project Overview

**so\_long** is a simple 2D game project where the player navigates through a map, collects all the collectibles, and reaches the exit. The game is built using the **MiniLibX** graphics library, and focuses on fundamental programming concepts like file parsing, game loops, rendering, and memory management.

---

## What I Learned

This project taught me a lot about how 2D games work under the hood. Some of the key things I learned include:

* How to parse and validate text-based maps.
* How to manage 2D graphics with **MiniLibX**, including rendering images and handling user input.
* Implementing basic **game logic**, like movement, collisions, and win conditions.
* The importance of **memory management** in C—avoiding leaks, handling clean exits, and freeing dynamically allocated resources.
* Writing a **flood fill/pathfinding algorithm** to check if the map is solvable.

---

## Game Rules (Mandatory Requirements)

* The player must be able to move in four directions (W, A, S, D or arrow keys).
* The player cannot pass through walls (`1`).
* The game map must contain:

  * At least one collectible (`C`)
  * One player starting position (`P`)
  * One exit (`E`)
* The game ends only if all collectibles are gathered and the player reaches the exit.
* The map must be:

  * Rectangular
  * Surrounded by walls
  * Solvable (i.e., there's a valid path from `P` to all `C` and to `E`)
* Every move by the player should increment and display a move counter in the terminal.
* The window must close cleanly on `ESC` or red cross click.

---

## Map Format

Maps are stored in `.ber` files and consist of the following characters:

* `0` - Empty space
* `1` - Wall
* `C` - Collectible
* `E` - Exit
* `P` - Player

Example:

```
11111
1P0C1
10001
1E001
11111
```

---

## Graphics and Controls

* The game uses MiniLibX to render a 2D top-down view.
* The screen should update correctly when the player moves.
* Assets must not break or behave incorrectly when switching or minimizing the window.

---

## Difficulties Faced

* Writing the **map validator** was one of the most complex parts. I had to ensure the map met all the project rules, including being rectangular and solvable.
* Handling **input events** and keeping the game loop smooth took some time to get right.
* Learning to work with **MiniLibX** was new for me, especially understanding how image rendering and event hooks worked.
* Preventing **memory leaks** required careful attention to how and when resources were allocated and freed.
* Making sure that everything exited cleanly (even after errors or user quit) helped me practice writing robust C code.

---

## Bonus Features (Optional)

If the mandatory part is completed perfectly, bonus features can include:

* Displaying the move counter directly in the game window.
* Animating sprites.
* Adding enemies that move or patrol.
* Adding sound or other aesthetic improvements.

---

## How to Run

```bash
make
./so_long maps/example.ber
```

---

## Final Thoughts

so\_long was a great introduction to game development basics. I now have a better understanding of rendering, user input, pathfinding, and working with external libraries like MiniLibX. It was challenging, especially at first, but incredibly rewarding to see the game come together piece by piece.

