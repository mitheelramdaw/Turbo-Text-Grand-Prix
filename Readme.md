
# 🏁 C++ Race Rampage : 🏆 Mini-Hackathon Week 1: Turbo Text Grand Prix 🏁


A wild, chaotic, and entertaining racing simulator in the terminal. Two racers. A track. Hazards. Power-ups. Random events. All wrapped in classic ASCII flair and streetwise commentary.

---

## 🎮 Gameplay Features

* **Lap-Based Racing**: First to **3 laps** wins.
* **Power-ups (P)** give +3 speed boosts.
* **Hazards (H)** knock you back −2.
* **Racer initials are colour-coded** (Green vs Cyan).
* **Track commentary** in real-time — now with proper *roadman* energy.
* **Colourful countdown**: Red → Yellow → Green → GO!
* **Multiple themes** for different vibes:
  `space`, `snow`, `desert`, `city`, `jungle`

---

## 🧪 Example Gameplay

```
Enter the race track length (minimum 20): 30
Enter name for Racer One: Tio
Enter name for Racer Two: Rio
How often do you want updates (seconds, (e.g.) 0.25): 0.25
Race Code (0 = random): 123456
Use colours? (y/n): y
Track theme ('space', 'snow', 'desert', 'city', 'jungle'): snow

=== ASCII Race Track ===
Tio (T) VS  Rio (R) • First to 3 laps wins!
Track Length: 30 | Race Code: 123456

3...
2...
1...
GO!

Tio: ****P************H********| [Lap 1/3]
Rio: ****R***************P****| [Lap 0/3]

=== COMMENTARY ===
Tio is pulling ahead!
```

---

## ❄ Track Theme Symbols

| Theme   | Track Symbol |
| ------- | ------------ |
| default | `-`          |
| space   | `@`          |
| snow    | `*`          |
| desert  | `~`          |
| city    | `#`          |
| jungle  | `+`          |

---

## 💻 Compilation Instructions

Make sure you have a C++17-compliant compiler (like `g++`, `clang++`, or MSVC).

### 🐧 Linux/macOS:

```bash
g++ -std=c++17 -o racetrack racetrack.cpp
./racetrack
```

### 🪟 Windows (using MinGW):

```bash
g++ -std=c++17 -o racetrack.exe racetrack.cpp
racetrack.exe
```

---

## ⚙️ Core Mechanics

* `baseStep`: Every racer moves 1–6 spaces per turn.
* `nitroChance`: 1 in 8 chance to get a +3 nitro boost.
* `powerup` and `hazard` tiles are randomly distributed.
* Racers wrap back to 0 when crossing the finish line, gaining a lap.
* Game ends once a racer hits 3 laps — or both tie.

---

## 🧠 Fun Details

* Racer names are uppercased at the start.
* If initials clash, they're replaced with '1' and '2'.
* Power-ups and Hazards are colour coded:

  * `P` → yellow (boost)
  * `H` → red (hazard)
* Racer symbols:

  * Racer 1 → **Green**
  * Racer 2 → **Cyan**
* Terminal-clearing between frames for smooth updates.

---

## 🎤 Commentary System

At each turn, real-time banter appears:

* **If tied:**

  * “It’s bunds and bunds!”
  * “Locked together!”

* **If one leads:**

  * “Takes control of the track!”
  * “Surges forward! Pile first”

Also includes hazard/powerup shoutouts like:

```
 >> BOOST <<  Tio smashed a power-up! +3!
 >> HAZARD << Rio mbonzied a hazard! -2!
```

---

## 🧯 Failsafes

* Input validation for numbers and text.
* Defaults to 0.25s delay and random race code if input is invalid.
* Minimum track length is **20**.

---

## 📂 Files

* `racetrack.cpp` → Main source code.
* `README.md` → This file.

> No external dependencies. Just standard C++.

---

## 🏁 End Message

```
Result: Tio wins! 🏆

Go home now the hell!
```

---

