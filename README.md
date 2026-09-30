#  Marble Tilt Maze

This project is a terminal-based marble tilt maze using **Pygame**. It introduces students to interactive game design using object-oriented principles and real-time graphical rendering.

---

## What’s Provided

A partially working version of a tilt maze with:

- A marble that accelerates toward wherever the mouse cursor is, simulating tilting the whole maze
- A simple hand-built maze of walls with a goal in the far corner
- A countdown timer

You are expected to **analyze**, **interact with an AI assistant**, and **complete/fix** the game to make it fully functional.

### **Use an LLM (e.g. ChatGPT or Claude) as your debugging and pair-programming partner for this lab.**

---

## Getting Started

### Setup

1. Clone the repo or download the project folder.
2. Make sure you have Python 3.10+ installed.
3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Run the game:

```bash
python main.py
```

---

## Tasks to Complete

Each task must be completed using an iterative process involving LLM suggestions and your critical code review.

### Task 1: Refine Collision Detection

> Near a wall's corner, the marble sometimes bounces off empty space before it visually touches the wall. Investigate and enhance collision accuracy so bounces only happen when the round marble actually touches a wall.


### Task 2: Implement Game Over Condition

> Add a screen that displays whether the maze was solved (with the finish time) or the timer ran out, then gracefully waits for input instead of just printing to the console.


### Task 3: Add Replay Option

> After the end screen, allow the user to play again by choosing a difficulty (Easy, Medium, or Hard tilt strength/friction/time limit), or exit.



### Task 4: Add Sound Feedback

> Add basic sound effects for bouncing off a wall, reaching the goal, and the timer running out.


---

## Expected Behavior

- The marble accelerates toward the mouse cursor's direction relative to the screen center, simulating a physical tilt
- Friction gradually slows the marble down, and its top speed is capped
- The marble bounces off walls instead of passing through them
- Reaching the goal circle ends the round as a win; running out of time ends it as a loss
- A countdown timer is visible at all times

---

## Folder Structure

```
marble-tilt-maze-main/
├── main.py
├── requirements.txt
├── game/
│   ├── game_engine.py
│   ├── marble.py
│   └── wall.py
└── README.md
```

---

## Submission Checklist

Submission is only the following three things:

- [] A 10-second video of gameplay **before** your changes, showing the bug/broken behavior
- [] A 10-second video of gameplay **after** your changes, showing the bug fixed and the new features working
- [] The Chat/LLM used page link, with the complete chat history



---

## My Lab 4 Submission

**Name:** B. Kodandapaani Reddy  |  **SRN:**  PES2UG24CS108

### Changes made (with AI assistance)

| Task | What I did |
|------|-----------|
| 1. Collision | Replaced the collision check with circle-vs-rectangle collision (closest point on the rect), so bounces only happen on real contact, including at corners. |
| 2. Game over | Added PLAYING / GAME_OVER states and an in-window overlay showing "You Win!" with the finish time, or "Time's Up!". |
| 3. Replay | Added a menu after the end screen: 1 Easy, 2 Medium, 3 Hard, Q/Esc to quit. Difficulty changes tilt strength, friction, and time limit. |
| 4. Sound | Added generated sound effects for wall bounces, reaching the goal, and timer expiry (no external audio files). |

### How to run

    pip install -r requirements.txt
    python main.py

On Python 3.14, `pygame` may fail to build. Use `pip install pygame-ce` instead.

### Controls

- Move the mouse: tilt the maze (the marble accelerates toward the cursor)
- After a round: 1 / 2 / 3 to pick a difficulty, Q or Esc to quit

### Files in this submission

- `Lab-4/before.mp4`: gameplay before changes
- `Lab-4/after.mp4`: gameplay after changes
- `Lab-4/chat_history.pdf`: full AI chat history
- Chat link: https://claude.ai/share/2df44d7b-aea3-4bb5-b222-1b8e346d8457