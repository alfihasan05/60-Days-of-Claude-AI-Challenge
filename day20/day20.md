# Day 20 — Build a Face Puzzle Game

## 🎯 Challenge

Build a fully functional browser-based **Face Puzzle Game** using HTML, CSS, and JavaScript.

The game allows users to:

- Access their webcam
- Take a selfie
- Convert the photo into a puzzle
- Choose between 3×3, 4×4, and 5×5 difficulties
- Drag and swap puzzle pieces
- Track time and moves
- Detect when the puzzle is solved
- Save the best results locally

---

## 🚀 Features

### 📷 Camera Access

- Requests webcam permission using `getUserMedia()`
- Prefers the front-facing camera
- Displays a live camera preview
- Captures the user's face using HTML Canvas
- Handles camera permission errors gracefully
- Supports HTTPS and localhost environments

### 🧩 Puzzle Generation

Three difficulty levels are available:

| Difficulty | Pieces |
|---|---:|
| Easy | 3 × 3 = 9 |
| Medium | 4 × 4 = 16 |
| Hard | 5 × 5 = 25 |

The captured image is divided into equal puzzle pieces and randomly scrambled.

The puzzle uses tile swapping, ensuring that every generated arrangement is solvable.

---

## 🖱️ Drag & Touch Controls

The game supports:

- Desktop mouse dragging
- Mobile touch interaction
- Pointer Events
- Dragging tiles between cells
- Automatic snapping to the nearest grid cell
- Tile swapping when dropped onto another piece
- Orange highlight while dragging
- Green border when a piece is correctly positioned

---

## ⏱️ Timer & Move Counter

The game tracks:

- Elapsed time
- Total moves
- Correctly positioned pieces

### Timer Format

```text
mm:ss.t
