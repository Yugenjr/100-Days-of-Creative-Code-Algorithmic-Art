# 🧬 Interactive Game of Life (p5.js)

A beautiful, interactive implementation of **Conway's Game of Life** built with JavaScript and the [p5.js](https://p5js.org/) library. This project explores **Emergent Complexity**: how simple rules can lead to organic, life-like patterns.

## 🚀 Quick Start

1. **Download** the `index.html` file.
2. **Open** it in any modern web browser (Chrome, Firefox, Safari).
3. **Interact**: Drag your mouse across the screen to "seed" new life into the system.

## 🕹️ Controls

* **Mouse Drag:** Birth new cells at the cursor position.
* **Key 'R':** Randomize the entire board with a new generation.
* **Key 'C':** Clear the board (extinction event).
* **Window Resize:** The grid automatically adapts to your screen size.

## 🧠 How it Works

The "Game" is a cellular automaton that evolves frame-by-frame based on four simple rules applied to every cell and its 8 neighbors:

| Rule | Description | Result |
| --- | --- | --- |
| **Underpopulation** | Any live cell with fewer than 2 neighbors dies. | 💀 |
| **Survival** | Any live cell with 2 or 3 neighbors lives on. | 🧬 |
| **Overpopulation** | Any live cell with more than 3 neighbors dies. | 💀 |
| **Reproduction** | Any dead cell with exactly 3 neighbors becomes alive. | ✨ |

### Implementation Details

* **Toroidal Grid:** The edges of the screen are wrapped. If a pattern moves off the right side, it reappears on the left.
* **Age-Based Coloring:** Cells change hue based on their "age" (how many frames they have survived), creating a rainbow heat-map of stable vs. chaotic areas.
* **Performance:** Built using a 2D array buffer system to ensure smooth 60 FPS calculation.

## 🛠️ Built With

* [p5.js](https://p5js.org/) - A JS library for creative coding.
* HTML5/CSS3 - For the container and UI overlays.

---

### Customizing the Simulation

If you want to change the "feel" of the simulation, look for this variable in the code:

```javascript
let res = 10; // Change this to 5 for high-detail, or 20 for chunky retro blocks

```