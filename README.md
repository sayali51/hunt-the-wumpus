# 🐉 Hunt the Wumpus

> A classic Artificial Intelligence game based on the **Wumpus World** — a knowledge-based agent problem formalized by Stuart Russell & Peter Norvig in *Artificial Intelligence: A Modern Approach (AIMA)*.

---

## 🎮 Live Demo

**[▶ Play the Game](https://github.com/sayali51.github.io/hunt-the-wumpus/)**

> Replace `YOUR-USERNAME` with your GitHub username after deploying.

---

## 📖 About the Game

Hunt the Wumpus was originally created by **Gregory Yob in 1973** and later became the canonical example of a **knowledge-based agent** in AI education. The player explores a dark cave grid, using sensory clues to logically deduce the locations of hazards and hunt down the deadly Wumpus.

This implementation features:
- **5 × 6 cave grid** (30 rooms) with fog-of-war exploration
- **Sensory perception system** — stench, breeze, and glimmer cues
- **Stochastic Wumpus** — moves to a random room when disturbed by a missed arrow
- **Score system** — rewards for gold collection and Wumpus kill, penalties per step
- **Keyboard + mouse controls**
- **Single-file HTML** — zero dependencies, runs in any browser

---

## 🧠 AI Concepts Demonstrated

| Concept | How it appears |
|---|---|
| **Knowledge-Based Agent** | Player acts as the inference engine, using a mental KB |
| **Partial Observability** | Fog of war — only adjacent rooms are sensed |
| **Logical Inference** | Deduce Wumpus/pit location from stench/breeze cues |
| **Uncertainty** | Wumpus moves randomly after a missed shot |
| **PEAS Framework** | Performance, Environment, Actuators, Sensors all defined |
| **Sequential Environment** | Each action permanently changes the world state |

---

## 🗺️ How to Play

### Controls

| Key | Action |
|---|---|
| `W` / `↑` | Move North |
| `S` / `↓` | Move South |
| `A` / `←` | Move West |
| `D` / `→` | Move East |
| `Space` / `F` | Toggle shoot mode |
| Click arrow buttons | Move or shoot in that direction |

### Symbols

| Symbol | Meaning |
|---|---|
| 🧑 | You (the agent) |
| 👾 | Wumpus (kill it to win!) |
| 💰 | Gold (+100 pts when collected) |
| 🕳️ | Bottomless pit (instant death) |
| 🦨 | Stench — Wumpus is in an adjacent room |
| 💨 | Breeze — a pit is in an adjacent room |
| ✨ | Glimmer — gold is in an adjacent room |
| ■ (dark) | Fog of war — unexplored room |

### Scoring

| Event | Points |
|---|---|
| Each step taken | −1 |
| Each arrow fired | −5 |
| Collecting gold | +100 |
| Killing the Wumpus | +200 |

### Win / Lose

- ✅ **Win** — Kill the Wumpus with an arrow
- ❌ **Lose** — Enter the Wumpus's room, or fall into a pit

---

## 💡 Strategy Guide

1. **Start safe** — if no stench or breeze in your starting room, all adjacent rooms are safe to enter.
2. **Use logic** — stench means Wumpus is adjacent; breeze means pit is adjacent. Cross-reference from multiple rooms to narrow down exact locations.
3. **No cue = safe** — a room with neither stench nor breeze guarantees all its neighbors are hazard-free.
4. **Save arrows** — you only have 5. Only shoot when you are highly confident about the Wumpus location.
5. **Wumpus moves** — if you miss, the Wumpus relocates randomly. Re-sense after every missed shot.
6. **Gold first** — collect gold (+100) whenever you find it, then focus on the Wumpus.

---

## 🗂️ Project Structure

```
hunt-the-wumpus/
│
├── index.html      ← Entire game (HTML + CSS + JS, single file)
└── README.md       ← This file
```

---

## 🔧 Run Locally

No installation required. Just open `index.html` in any modern browser:

```bash
# Clone the repo
git clone https://github.com/YOUR-USERNAME/hunt-the-wumpus.git

# Open in browser
cd hunt-the-wumpus
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

---

## 📐 Technical Details

| Property | Value |
|---|---|
| Grid size | 5 rows × 6 columns = 30 rooms |
| Starting arrows | 5 |
| Pits | 2 (randomly placed) |
| Wumpus | 1 (randomly placed) |
| Gold | 1 (randomly placed) |
| Arrow range | Up to 3 rooms in a straight line |
| Wumpus behavior | Moves to random neighbor on missed shot |
| Rendering | HTML5 Canvas API |
| Dependencies | None — pure HTML/CSS/JS |

---

## 📚 References

1. Russell, S. J., & Norvig, P. (2020). *Artificial Intelligence: A Modern Approach* (4th ed.). Pearson. — Chapter 7 (Logical Agents)
2. Yob, G. (1975). Hunt the Wumpus. *Creative Computing*, 1(5), 51–54.
3. [Wumpus World — Wikipedia](https://en.wikipedia.org/wiki/Wumpus_world)
4. [Hunt the Wumpus — Wikipedia](https://en.wikipedia.org/wiki/Hunt_the_Wumpus)

---

## 👨‍💻 Developed For

**Artificial Intelligence Assignment**


---

*Built as a single-file browser game. No frameworks. No backend. Just pure AI logic.*
