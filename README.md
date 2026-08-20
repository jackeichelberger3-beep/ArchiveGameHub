# 🎮 Game Hub

A simple, beginner-friendly game hub built with plain HTML, CSS, and JavaScript.
No frameworks, no build step — just open `index.html` or host it on GitHub Pages.

## What's inside

```
index.html            ← the menu + the game player (all features live here)
games/
  snake.html
  tictactoe.html
  memory.html
```

## Features

- **Main menu** of game cards that scrolls when you add lots of games.
- **Each game is its own HTML file** in the `games/` folder — easy to write and manage.
- **Window-style controls** in the corner while playing:
  - 🔴 **red** — close, back to the menu
  - 🟡 **yellow** — opens a blank tab to hide the game (the game keeps running here)
  - 🟢 **green** — fullscreen the game

---

## 🕹️ How to add a new game (for GitHub)

You only need to do two things: **add your game's HTML file**, and **add one line to the games list**.

### Step 1 — Create your game file

1. Open the `games/` folder (the one next to `index.html`).
2. Create a new HTML file inside it, for example `games/mygame.html`.
3. Put your game's code in that file. It should be a complete, self-contained
   web page — here's a minimal template you can copy:

   ```html
   <!DOCTYPE html>
   <html lang="en">
   <head>
     <meta charset="UTF-8" />
     <meta name="viewport" content="width=device-width, initial-scale=1.0" />
     <title>My Game</title>
     <style>
       body { background: #0f172a; color: #fff; font-family: system-ui, sans-serif;
              display: flex; align-items: center; justify-content: center; min-height: 100vh; }
     </style>
   </head>
   <body>
     <h1>My Game</h1>
     <!-- your game code goes here -->
   </body>
   </html>
   ```

   You can look at `games/snake.html`, `games/tictactoe.html`, and
   `games/memory.html` for working examples.

### Step 2 — Add your game to the menu

1. Open `index.html` in any text editor.
2. Scroll to the bottom and find the `GAMES` list, which looks like this:

   ```js
   const GAMES = [
     { title: "Snake",       emoji: "🐍", description: "Eat the fruit, grow longer, don't crash.", file: "games/snake.html" },
     { title: "Tic-Tac-Toe", emoji: "❌", description: "Classic 3-in-a-row against the computer.",  file: "games/tictactoe.html" },
     { title: "Memory",      emoji: "🧠", description: "Flip the cards and match every pair.",       file: "games/memory.html" },
   ];
   ```

3. Add a new line for your game. For example, to add `games/mygame.html`:

   ```js
   const GAMES = [
     { title: "Snake",       emoji: "🐍", description: "Eat the fruit, grow longer, don't crash.", file: "games/snake.html" },
     { title: "Tic-Tac-Toe", emoji: "❌", description: "Classic 3-in-a-row against the computer.", file: "games/tictactoe.html" },
     { title: "Memory",      emoji: "🧠", description: "Flip the cards and match every pair.",      file: "games/memory.html" },
     { title: "My Game",     emoji: "🎯", description: "A short description of your game.",         file: "games/mygame.html" },
   ];
   ```

   Each line needs four things:
   - **title** — the name shown on the card
   - **emoji** — a small icon for the card
   - **description** — a short one-line description
   - **file** — the path to your game's HTML file (must match the file you created in Step 1)

4. Save `index.html`. Your game now appears on the menu automatically.

### Step 3 — (optional) Put it on GitHub

1. Create a new repository on GitHub.
2. Upload everything in this folder — keep `index.html` at the root and
   `games/` next to it.
3. In the repo, go to **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**,
   select the **main** branch and **/ (root)**, then **Save**.
5. Wait a minute — your game hub will be live at
   `https://your-username.github.io/your-repo-name/`.

That's it. Have fun! 🕹️
