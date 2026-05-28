Here is the updated `README.md` file, edited to remove the underlying algorithmic jargon and focus entirely on what the features do for the user.

```markdown
# 🐭 Micromouse Maze Viewer & Validator

A lightweight, browser-based visualizer, strict rule validator, and advanced route analyzer for classic ASCII Micromouse mazes. 

**🚀[Launch the Live Web App Here](https://derekchall.github.io/MicroMouse-Maze-viewer/)**

## ✨ Features

### 🏁 Advanced Pathfinding & Routing
*   **Optimal Path Extraction:** Discovers optimal and alternative routes to the center smoothly in the background without freezing your browser—even on wide-open "expert" mazes.
*   **True Physical Metrics:** Calculates the exact physical trajectory length (in millimeters) and total turn count for every discovered route, automatically sorting them by efficiency.
*   **Command Generation:** Generates standard Micromouse movement commands (`F#`, `D#`, `SS90`, `SD45`, `DS45`, `DD90`, `SS180`) for every route.
*   **Precision Geometric Rendering:** Draws precise physical racing lines directly on the maze canvas, seamlessly mapping exact entry and exit boundary offsets around corner posts.
*   **Interactive Route Explorer:** Click any route in the generated list to highlight it on the canvas, complete with precise start (green) and end (red) turn markers.
*   **Background Search UI:** Complex mazes search smoothly in the background with a real-time progress indicator and a "Stop Search" button to let you view early results instantly.

### 🛠️ Validation & Visuals
*   **Instant Rendering:** Converts classic ASCII text grids into high-quality visual mazes dynamically.
*   **Strict Rule Validation:** Automatically scans the maze for competition legality, checking for intact perimeter walls, exact start (`S`) and goal (`G`) placements, and illegal freestanding posts.
*   **Interactive Error Spotlighting:** If an error is found, click on it in the generated list to instantly cast a neon cyan "spotlight" on the exact broken wall, post, or cell on the canvas!
*   **Dead-end Spotlighting:** Toggle a visual overlay to instantly highlight all dead-end paths.
*   **Print-Friendly Light Mode:** Toggle between "Dark Maze" (high-contrast black background) and "Light Maze" (pure black-and-white mode, perfect for printing mazes to paper).

### 📂 File Management
*   **Drag & Drop Support:** Simply drag a `.txt` file from your computer directly into the browser to load it.
*   **Web Link Importer:** Load mazes directly from other GitHub repositories or URLs using web parameters.

## 🛠️ How to Use

There are four ways to use the viewer:

### 1. Paste or Type
Go to the [Live Viewer](https://derekchall.github.io/MicroMouse-Maze-viewer/) and simply paste your ASCII maze text directly into the text box. The canvas will render and validate it automatically.

### 2. Drag & Drop
Drag a valid `maze.txt` file from your desktop and drop it into the dashed box at the top of the left panel.

### 3. Load via Web Link (Great for sharing!)
You can instantly load a maze hosted anywhere on GitHub by appending `?maze=` followed by the GitHub link to the viewer URL. 

*Example:*
```text
https://derekchall.github.io/MicroMouse-Maze-viewer/?maze=https://github.com/micromouseonline/mazefiles/blob/master/classic/alljapan-011-1990-frsh.txt
```

### 4. Running Locally
Because this app is completely self-contained in a single file, you don't need any servers or dependencies to run it. Simply download the `index.html` file to your computer and double-click it to open it directly in Chrome, Edge, Firefox, or Safari!

## 📝 Accepted Maze Format

The ASCII maze should strictly conform to the specifications set out at [github.com/micromouseonline/mazefiles](https://github.com/micromouseonline/mazefiles).

The viewer parses this standard classic Micromouse ASCII layout, where:
*   `o` or `+` represents a post/peg
*   `---` represents a horizontal wall
*   `|` represents a vertical wall
*   `S` marks the Start cell (must be bottom-left)
*   `G` marks the Goal cells (must be 4 cells in the exact 2x2 center)

**Example Maze:**
```text
o---o---o---o---o---o---o---o---o---o---o---o---o---o---o---o---o
|       |   |                                   |               |
o   o---o   o---o   o---o   o---o---o   o---o   o   o---o---o   o
|   |           |   |           |           |   |   |       |   |
o   o---o   o   o   o   o---o   o   o---o   o   o   o   o   o   o
|       |   |   |           |       |           |   |   |   |   |
o   o   o   o   o   o---o---o---o---o---o---o   o   o   o   o   o
|   |       |   |       |                       |   |   |       |
o   o---o   o   o---o   o   o---o---o---o---o---o   o   o---o---o
|   |       |       |   |   |       |               |           |
o   o   o---o---o   o   o   o   o   o   o---o---o---o---o---o   o
|   |       |       |   |       |   |                       |   |
o   o---o   o   o---o   o---o---o   o---o---o---o---o---o   o   o
|   |       |   |       |               |                   |   |
o   o   o---o   o   o   o   o---o---o   o   o---o---o---o---o   o
|   |       |   |       |   | G   G |   |                   |   |
o   o---o   o   o---o   o   o   o   o   o---o---o---o---o   o   o
|       |   |       |   |   | G   G |   |       |           |   |
o   o---o   o---o   o   o   o   o---o   o   o   o   o---o---o   o
|   |       |       |   |       |       |   |   |   |           |
o   o   o---o   o---o   o---o   o   o   o   o   o   o   o---o---o
|   |       |       |       |       |       |       |           |
o   o---o   o---o   o---o   o---o---o---o---o---o---o---o---o   o
|   |           |       |                   |                   |
o   o   o---o   o   o   o---o   o---o---o   o   o---o---o---o---o
|       |   |   |   |       |   |           |                   |
o---o   o   o   o---o---o   o---o   o---o---o---o---o---o---o   o
|       |   |           |       |               |               |
o   o---o   o---o---o   o---o   o---o---o---o   o   o---o---o---o
|                           |                   |               |
o   o---o   o---o---o---o---o---o---o---o---o---o---o---o---o   o
| S |                                                           |
o---o---o---o---o---o---o---o---o---o---o---o---o---o---o---o---o
```

## 🖼️ Embedding the Viewer

You can embed the live maze viewer directly into your own website, blog, or project page using an HTML `<iframe>`.

### Standard Embed

This will embed the entire web app, including the editor and validation panels.

```html
<iframe 
    src="https://derekchall.github.io/MicroMouse-Maze-viewer/?maze=https://raw.githubusercontent.com/micromouseonline/mazefiles/master/classic/alljapan-011-1990-frsh.txt" 
    width="100%" 
    height="700" 
    frameborder="0">
</iframe>
```

### Clean Embed (Recommended)

For a cleaner look that shows **only the maze canvas**, add `&embed=true` to the end of the URL. This activates "Embed Mode," which automatically hides all UI elements.

```html
<iframe 
    src="https://derekchall.github.io/MicroMouse-Maze-viewer/?maze=https://raw.githubusercontent.com/micromouseonline/mazefiles/master/classic/alljapan-011-1990-frsh.txt&embed=true" 
    width="800" 
    height="800" 
    frameborder="0"
    style="border: 1px solid #ccc; border-radius: 8px;">
</iframe>
```
```