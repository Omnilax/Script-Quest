# Script Quest

A game-style way for students to learn JavaScript. Students work through stages on a map, write real code in an in-browser editor, earn XP, take quizzes, and build playable arcade games out of the functions they write.

## Running it

It's a single self-contained page. Open `index.html` in a browser; no build step or server needed. (Fonts load from Google Fonts, so it looks best online.)

## What's inside

- **22 sections, 948 stages**
  - Main path: Variables, Arithmetic & Logic, Data Types & Structures, Conditionals, Loops, Functions.
  - Fun: Puzzle Vault, Arcade Builds.
  - Advanced: Array Mastery, Objects/Classes/Prototypes, Scope/Closures/`this`, Modern Syntax (ES6+), Errors & Debugging, Async, DOM & Events, Algorithms.
  - Bonus: Hello, World! Tutorial, Game Engine Bridge, Regular Expressions, Binary/Bits & Flags, Game Math (Vectors & Trig), Procedural Generation.
- **50 quizzes** (302 questions), a **283-term reference glossary**, and a **snippet library**.
- **Arcade games** driven by student-written functions: Snake, Pong, Breakout, Rain Dodge, Tic-Tac-Toe, Minesweeper, Game of Life, Space Miner, Dice Rogue.
- A top-bar dock with Continue, mute and player chip; it collapses on phones.
- **Sandbox**, profile, and settings (skins: cartridge, pocket, blueprint, night, contrast).
- Student code runs in a Web Worker (or a loop-guarded main-thread runner for DOM/canvas/game code), with plain-English error explanations.
- Progress is saved in `localStorage` (keys prefixed `sq3_`).

## How the file is laid out

| Part | What it is |
| --- | --- |
| First `<style>` block | CodeMirror 5 CSS, then the app's own "handheld cartridge" UI styles |
| App shell | `#app` with header, `#view`, tab bar, overlay, toast, and an `#fx` canvas |
| First `<script>` | CodeMirror 5.65.16 (MIT) with JavaScript, Python, Lua and other modes |
| Second `<script>` | `SQDATA` (all lessons, quizzes, reference, snippets as one JSON object), the code runner, error explainer, arcade engines, storage, and the views (`viewMap`, `viewSection`, `viewStage`, `viewQuiz`, `viewSandbox`, `viewRef`, `viewMe`, `viewSettings`) |

`modules/` holds the source JSON for the bonus sections; their content is already embedded in `SQDATA` inside `index.html`.

CodeMirror is copyright Marijn Haverbeke and others, distributed under the MIT license.
