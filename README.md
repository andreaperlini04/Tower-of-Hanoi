# Tower of Hanoi 3D 

A 3D simulation of the classic Tower of Hanoi puzzle built with a custom C++ graphics engine based on OpenGL/GLUT.

## Description
This project implements the Tower of Hanoi game in a 3D environment. It features a custom-built engine (`Eng::Base`) that handles scene graph management, OVO model loading, dynamic lighting, and reflections.

## Features
- **3D Graphics**: Realistic rendering with textures and real-time reflections on the table surface.
- **Game Logic**: Full implementation of Hanoi rules with support for up to 7 disks.
- **Undo/Redo System**: Reverse or re-apply your moves at any time.
- **Multiple Cameras**: Toggle between a free-roaming camera and fixed cinematic presets.
- **Custom Engine**: Uses a Singleton pattern for engine management and a PIMPL approach to hide implementation details.

## Installation & Build
The project uses a hierarchical Makefile system to build both the engine and the client.

1. **Prerequisites**: Ensure you have `make`, a C++ compiler (supporting C++17 or higher), and the necessary dependencies (FreeGLUT, GLM, FreeImage) installed.
2. **Build everything**:
   ```bash
   make all
   ```
3. **Run the game**:
   Navigate to the binary folder or use the provided `run.sh` script (for Linux).

## Controls
The game offers two main interaction modes: **Movement** and **Rotation**.

### General Controls
- `M`: Toggle between Movement and Rotation modes.
- `R`: Reset the game and reload the scene.
- `U`: Undo last move.
- `Y`: Redo move.
- `1-4`: Select Camera Presets.
- `P`: Reset to Main Mobile Camera.
- `ESC`: Exit the game.

### Camera Controls (WASD)
- `W / S`: Move forward/backward (Move Mode) or Rotate X-axis (Rotate Mode).
- `A / D`: Move left/right (Move Mode) or Rotate Y-axis (Rotate Mode).
- `Q / E`: Move up/down (Move Mode) or Rotate Z-axis (Rotate Mode).

### Gameplay Controls
- `Left / Right Arrows`: Select a peg.
- `Up Arrow`: Pick up the top disk from the selected peg.
- `Down Arrow`: Place the held disk onto the selected peg.

## Project Structure
- `/engine`: The core rendering library.
- `/client`: Game logic and main entry point.
- `/dependencies`: External libraries (GLM, FreeGLUT, etc.).
- `/demo`: Pre-compiled binaries and assets.

