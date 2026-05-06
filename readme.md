# 🐭 Micromouse Maze Viewer & Validator

A lightweight, browser-based visualizer and strict rule validator for classic ASCII Micromouse mazes. 

**🚀 [Launch the Live Web App Here](https://derekchall.github.io/MicroMouse-Maze-viewer/)**

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-323330?style=for-the-badge&logo=javascript&logoColor=F7DF1E)

## ✨ Features

*   **Instant Rendering:** Converts classic ASCII text grids into high-quality visual mazes instantly.
*   **Strict Rule Validation:** Automatically scans the maze for competition legality. It checks for intact perimeter walls, exact start (`S`) and goal (`G`) placements, illegal freestanding posts, and correct text formatting.
*   **Interactive Error Spotlighting:** If an error is found, click on it in the generated list to instantly cast a neon cyan "spotlight" on the exact broken wall, post, or cell on the canvas!
*   **Drag & Drop Support:** Simply drag a `.txt` file from your computer directly into the browser to load it.
*   **Web Link Importer:** Load mazes directly from other GitHub repositories or URLs using web parameters.
*   **Print-Friendly Light Mode:** Toggle between "Dark Maze" (high-contrast black background) and "Light Maze" (pure black-and-white mode, perfect for printing mazes to paper).

## 🛠️ How to Use

There are three ways to load a maze into the viewer:

### 1. Paste or Type
Go to the [Live Viewer](https://derekchall.github.io/MicroMouse-Maze-viewer/) and simply paste your ASCII maze text directly into the text box. The canvas will render and validate it automatically.

### 2. Drag & Drop
Drag a valid `maze.txt` file from your desktop and drop it into the dashed box at the top of the left panel.

### 3. Load via Web Link (Great for sharing!)
You can instantly load a maze hosted anywhere on GitHub by appending `?maze=` followed by the GitHub link to the viewer URL. 

*Example:*
```text
https://derekchall.github.io/MicroMouse-Maze-viewer/?maze=https://github.com/micromouseonline/mazefiles/blob/master/classic/alljapan-011-1990-frsh.txt