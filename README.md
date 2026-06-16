# Last Lab Defender

Last Lab Defender is a 3D survival shooter game built with Python and PyOpenGL. The player takes the role of the final guardian of a laboratory capsule containing a secret biological substance. Enemy aliens attack in waves, and the objective is to defend both the player and the capsule through multiple levels until the final boss is defeated.

## Project Overview

The game uses OpenGL, GLUT, and GLU to render a real-time 3D arena with a controllable protagonist, enemy waves, bullets, health bars, camera movement, level transitions, and a final boss battle. It is implemented as a single Python program and demonstrates core computer graphics concepts such as 3D object rendering, transformations, collision detection, animation loops, keyboard/mouse interaction, and HUD overlays.

## Features

- 3D laboratory arena with grid floor, walls, capsule, player, enemies, bullets, and boss model
- Multi-stage story introduction before gameplay starts
- Three-level gameplay system
- Level 1 with unarmed enemy waves
- Level 2 with armed enemies and projectile attacks
- Level 3 final boss battle with cannonball attacks
- Player movement, rotation, shooting, reloading, and camera switching
- First-person and third-person view modes
- Health system for both player and capsule
- Boss health bar during the final level
- Magazine and reload system
- Weapon upgrade system based on level progress and kill count
- Special red enemies that can restore player health
- Pause, restart, and cheat mode support
- Real-time HUD showing player HP, capsule HP, level, kills, time, ammo, and boss HP

## Technologies Used

- Python
- PyOpenGL
- OpenGL
- GLUT
- GLU
- Math and random modules for movement, spawning, and collision logic

## Requirements

Make sure Python is installed on your computer. Then install the required Python packages:

```bash
pip install PyOpenGL PyOpenGL_accelerate
```

If the game does not open because of a GLUT-related error, install a GLUT/freeglut library for your operating system.

For Ubuntu or Debian-based Linux:

```bash
sudo apt install freeglut3-dev
```

For Windows, install Python first, then install the PyOpenGL packages using pip. If GLUT is still missing, install a compatible freeglut package and ensure it is available in your system path.

## How to Run

Clone the repository:

```bash
git clone https://github.com/your-username/your-repository-name.git
```

Go inside the project folder:

```bash
cd your-repository-name
```

Install dependencies:

```bash
pip install PyOpenGL PyOpenGL_accelerate
```

Run the game:

```bash
python Last_Lab_Defender.py
```

If your system uses Python 3 as `python3`, run:

```bash
python3 Last_Lab_Defender.py
```

## Game Objective

Protect the secret capsule from alien enemies while keeping the protagonist alive. Enemies move toward the capsule and can damage it on contact. In later levels, enemies can also shoot at the player. The player must survive each stage, defeat enough enemies to upgrade the weapon, and finally destroy the boss.

## Controls

| Control | Action |
|---|---|
| `W` | Move forward |
| `S` | Move backward |
| `A` | Move left/strafe |
| `D` | Move right/strafe |
| `Q` | Rotate left |
| `E` | Rotate right |
| Left mouse button | Shoot |
| Right mouse button | Toggle first-person/third-person view |
| `R` | Reload weapon |
| `P` | Pause/resume game |
| `F` | Restart game |
| `C` | Toggle cheat mode |
| `Z` | Decrease field of view |
| `X` | Increase field of view |
| Arrow left/right | Rotate external camera |
| Arrow up/down | Move external camera up/down |

## Level System

### Level 1

The first level introduces basic alien waves. Enemies move toward the capsule and damage either the capsule or player on contact. The player must kill enough enemies before the level timer ends.

### Level 2

The second level increases difficulty by introducing armed enemies. These enemies can fire projectiles toward the player while continuing to pressure the capsule.

### Level 3

The final level introduces a boss enemy with a separate health bar. The boss moves across the arena and fires cannonballs. The player must avoid attacks, shoot down incoming cannonballs when necessary, and reduce the boss health to zero.

## Health and Combat Rules

- The player starts with limited health.
- The capsule has its own health bar.
- If the player health reaches zero, the game ends.
- If the capsule health reaches zero, the game ends.
- Special red enemies can restore player health.
- Enemy bullets and boss cannonballs can damage the player.
- Boss cannonballs can also damage the capsule.
- Destroying cannonballs can reward the player with health recovery.

## Project Structure

```text
Last_Lab_Defender.py
README.md
```

The current version is implemented mainly in a single Python file. The main class, `Last_Lab_Defender`, manages the game state, rendering, input handling, enemy behavior, collisions, HUD, level progression, and main loop.

## Key Concepts Demonstrated

- 3D rendering with OpenGL primitives
- Camera setup using perspective projection
- Keyboard and mouse event handling with GLUT
- Object transformation using translation, rotation, and scaling
- Enemy spawning and movement logic
- Bullet and projectile collision detection
- Real-time game loop and animation updates
- HUD rendering using 2D overlay text and health bars
- Level progression and boss fight mechanics

## Future Improvements

- Add sound effects and background music
- Add start menu and settings menu
- Add difficulty selection
- Improve enemy AI and pathfinding
- Add more weapon types
- Add score saving or leaderboard system
- Separate the code into multiple modules for better maintainability
- Add textures, lighting, and particle effects for a richer visual experience

## Author

Developed as a Python OpenGL game project.

## License

This project is intended for educational and academic use. You may add a specific license such as MIT if you plan to make the repository public.
