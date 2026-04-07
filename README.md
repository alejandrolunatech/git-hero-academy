# 🚀 Git Hero Academy

🎮 **[Play it live → https://alejandrolunatech.github.io/git-hero-academy/](https://alejandrolunatech.github.io/git-hero-academy/)**

A fun, multilingual, interactive game that teaches kids Git from the ground up — from the basics of the three working areas all the way to rebasing, cherry-picking, stashing, and recovering lost work with reflog.

No installation. No server. No dependencies. Open the HTML file in any browser and play.

---

## What it is

Git Hero Academy is a single-file browser game where kids learn Git by typing real commands into a simulated terminal. Every lesson follows a **teach → try** flow:

1. **Learn panel** — concept cards explain the idea, a static ASCII diagram shows how it works visually, and a real-world analogy makes it click
2. **Terminal panel** — the kid types the actual command, gets feedback, and moves on

Progress is tracked with a star counter and a chapter progress bar. Getting a command wrong shakes the screen and plays an error sound. Getting it right triggers confetti, floating star emojis, and a success chime.

---

## Features

- **Multilingual** — English, Spanish, and Dutch. Language can be switched at any time from the top bar, or chosen at the start screen. All lesson text, feedback messages, terminal prompts, level names, and UI labels are fully translated.
- **Personalised** — kids enter their name at setup. The game greets them by name throughout: in the terminal prompt, in success messages, and on the final win screen.
- **Character selection** — 6 heroes to choose from: 🧑‍🚀 Astronaut, 🥷 Ninja, 🧙‍♀️ Witch, 🤖 Robot, 🐲 Dragon, 🦄 Unicorn. The chosen character appears as the lesson mascot and in the top bar.
- **5 colour themes** — Space (dark blue), Jungle (dark green), Ocean (deep navy), Candy (purple/pink), Fire (deep red/orange). Chosen at setup; all UI colours update instantly.
- **Sound effects** — Web Audio API, no external files. Ascending chimes on success, fanfare on chapter completion, a punchy error buzz on wrong answers, gentle clicks on navigation, and quiet taps while typing the name.
- **Static ASCII diagrams** — 9 colour-coded terminal diagrams appear in lessons where a visual helps. No animations, no cycling — just the clearest single diagram for that concept, always visible.
- **Confetti celebrations** — completing a mission drops coloured confetti and pops emoji bursts. Finishing the final mission adds a full-screen win banner with the kid's name and character emoji.

---

## Curriculum — 6 Chapters, 21 Missions

### 📦 Chapter 1 — The Three Git Areas

| Mission | Command |
|---|---|
| 🗺️ The 3 Areas | `git status` |
| 🚀 Initialise a repo | `git init` |
| 📥 Clone a project | `git clone` |
| 📸 Stage and commit | `git add .` / `git commit -m` |
| ↩️ Restore files | `git restore --staged` |
| 🗑️ Remove from tracking | `git rm --cached` / `git rm --force` |

The centrepiece of Chapter 1 is a colour-coded ASCII diagram showing how files move between the **Working Area** (🔴 modified), **Staging Area** (🟢 staged), and **Repository** (committed forever), with `git add` and `git commit` labelled on the arrows.

### 📜 Chapter 2 — History & Log

| Mission | Command |
|---|---|
| 📜 Reading history | `git log --oneline` / `--name-only` / `-n 3` |

### 🌿 Chapter 3 — Branching

| Mission | Command |
|---|---|
| 🌿 Create a branch | `git branch` / `git branch -d` |
| 🔄 Switch branches | `git checkout` / `git checkout -b` |
| 🔗 Merge branches | `git merge` |
| 📊 Visual graph | `git log --graph --decorate --oneline` |

ASCII diagrams show: a commit graph with a branch point, and the before/after of a merge creating a merge commit.

### 🌐 Chapter 4 — GitHub & Remote

| Mission | Command |
|---|---|
| 🌐 Connect to GitHub | `git remote add origin` / `git remote -v` |
| 📤 Sync with remote | `git fetch origin` / `git push` / `git pull origin master` |
| 🌍 List all branches | `git branch -a` |
| 🍴 Forking | Fork concept + cloning your fork |

ASCII diagram shows local ↔ GitHub sync with push/pull/fetch labelled.

### ⚡ Chapter 5 — Advanced Moves

| Mission | Command |
|---|---|
| ♻️ Rebase | `git rebase master` / `git rebase -i HEAD~` (pick, squash) |
| 🍒 Cherry-pick | `git cherry-pick <hash>` |
| ↩️ Undo strategies | `git revert` / `git reset --soft HEAD~` / `git reset --hard HEAD~` |

ASCII diagrams show: rebase before/after with replayed commits D' E', cherry-pick copying a single commit to another branch, and all three undo strategies compared side-by-side.

### 🎒 Chapter 6 — Stash & Reflog

| Mission | Command |
|---|---|
| 🎒 Stash your work | `git stash` |
| 📚 Manage stashes | `git stash list` / `git stash show stash@{1}` / `git stash pop stash@{1}` |
| 🕰️ The safety net | `git reflog` |

ASCII diagrams show: the stash cycle (dirty → stashed → restored) and the reflog output with a recovery command.

---

## How to use

### Just open the file

```
git clone https://github.com/your-username/git-hero-academy.git
cd git-hero-academy
open git-hero-academy-v5.html        # macOS
xdg-open git-hero-academy-v5.html   # Linux
start git-hero-academy-v5.html       # Windows
```

Or double-click the file in Finder / Explorer. That is all — no npm, no build step, no server required.

### Use it in a classroom

Because it is a single self-contained HTML file, you can:

- Share it over a local network or USB stick
- Host it on GitHub Pages with zero configuration
- Email it directly to students
- Open it on tablets and Chromebooks (any browser with Web Audio API support)

### GitHub Pages

```
# Push to a repo, then in Settings → Pages → Source: main branch / root
# The file will be live at:
https://your-username.github.io/git-hero-academy/git-hero-academy-v5.html
```

---

## The teach → try flow

Every mission follows the same two-panel structure:

```
┌─────────────────────────────────────┐
│  LEARN PANEL                        │
│  ─────────────────────────────────  │
│  🧑‍🚀  Lesson title                  │
│      Intro paragraph                │
│                                     │
│  ┌─ ASCII diagram (if applicable) ─┐│
│  │  colour-coded terminal art      ││
│  └─────────────────────────────────┘│
│                                     │
│  📦 Concept card 1                  │
│  📦 Concept card 2  (animate in)    │
│  📦 Concept card 3                  │
│                                     │
│  Real-world analogy                 │
│  The command you'll use             │
│                                     │
│  [ I get it — let me try it! ➜ ]   │
└─────────────────────────────────────┘

        ↓ kid clicks

┌─────────────────────────────────────┐
│  TERMINAL PANEL                     │
│  ─────────────────────────────────  │
│  Mission prompt                     │
│                                     │
│  ● ● ●  ~/project                   │
│  > Ready, Alex! Type the command.   │
│  $ _                      [ Run ]   │
│                                     │
│  [ ← Review the lesson ]            │
└─────────────────────────────────────┘
```

The "Review the lesson" button is always present so kids can flip back without losing their place.

---

## Project structure

```
git-hero-academy/
├── git-hero-academy-v5.html   ← the entire app
└── README.md
```

Everything — HTML, CSS, JavaScript, all lesson content in three languages, all ASCII diagrams, the audio engine, and the celebration system — lives in one file. No external dependencies, no CDN calls, no network requests at runtime.

---

## Extending the app

All lessons live in the `LEVELS` array in the `<script>` tag. Each entry looks like this:

```js
{
  ch: 1,                          // chapter number
  ce: '📦',                       // chapter emoji
  icon: '🚀',                     // mission icon
  asciiHtml: `...`,               // static ASCII diagram (or null)
  name:        { en: '...', es: '...', nl: '...' },
  learnTitle:  { en: '...', es: '...', nl: '...' },
  intro:       { en: '...', es: '...', nl: '...' },
  concepts: [
    { icon: '📁', title: { en: '...', ... }, desc: { en: '...', ... } },
  ],
  analogy:      { en: '...', es: '...', nl: '...' },
  cmdPreview:  'git init',        // shown in the command preview box
  termPath:    '~/project',       // terminal path label
  accept:      ['git init'],      // array of accepted command prefixes
  successMsg:  '...',             // terminal output on success
  story:       { en: '...', es: '...', nl: '...' },
  missionTitle:  { en: '...', es: '...', nl: '...' },
  missionPrompt: { en: '...', es: '...', nl: '...' },
  done: false,
}
```

To add a new language, add a key to every `{ en: ..., es: ..., nl: ... }` object and add an entry to the `i18n` object at the top of the script.

To add a new character, add an entry to the `CHARS` array. To add a theme, add to `THEMES` and add a matching CSS class `.theme-yourname` with the colour variables.

---

## Browser support

Works in any modern browser with Web Audio API support:

| Browser | Supported |
|---|---|
| Chrome 66+ | ✅ |
| Firefox 76+ | ✅ |
| Safari 14+ | ✅ |
| Edge 79+ | ✅ |

Sound effects require a user interaction before the browser allows audio (the start button click satisfies this automatically). On browsers without Web Audio API, all sounds are silently skipped — the game works fine without them.

---

## Licence

MIT — free to use, modify, and share in classrooms, workshops, and anywhere else kids are learning to code.
