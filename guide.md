# AI Agent Vault 9000
### Build a Retro Vault Command Dashboard with AI Prompts

![The finished dashboard](images/hero.png)

**Paste a few prompts. Get the dashboard above. ~30 minutes. No coding.**

This guide doesn't make you write code. You copy the prompts on the next pages into a free AI builder, and it builds the whole thing for you. Then you generate the artwork with the image prompts and drop it in. That's it.

*Inspired by classic shelter-management games. An original product — not affiliated with any game or its trademarks.*

---

## Page 1 — What You Need & How It Works

**You need two free tools:**

1. **An AI app builder** — one of: **v0.dev** (easiest, by Vercel), **Bolt.new**, **Cursor**, or **Claude**. These take a written prompt and generate a working web app you can preview instantly.
2. **An AI image generator** — whatever you already use: Midjourney, DALL·E, Adobe Firefly, Stable Diffusion, etc. (Only needed if you want custom room/character art — Step 2.)

**The three steps:**

- **Step 1 — Build it.** Paste the Build Prompt (Page 2) into your AI builder. It generates the entire dashboard: the glowing rooms, the top status bar, the animations. Use the refinement prompts (Page 3) to fine-tune.
- **Step 2 — Make the art.** Use the image prompts (Page 4) to generate your room characters and icons.
- **Step 3 — Drop it in & make it yours.** Add your art, rename rooms, recolor (Page 5).

No prior coding experience required. If you can copy and paste, you can build this.

---

## Page 2 — Step 1: The Build Prompt

Open your AI builder (v0.dev is the simplest place to start). Paste this **entire prompt** in and let it generate. This is the core of the whole product — it describes the dashboard precisely so the AI builds it right the first time.

> **★ MASTER BUILD PROMPT — copy everything in this box ★**
>
> Build a single-page React dashboard styled as a **retro underground vault command center** — dark, glowing, like a cross-section of a bunker in a shelter-management video game. Use inline styles or Tailwind; no backend, mock data only.
>
> **Look & feel:** Near-black background (#050810) with a faint radial vignette and a subtle star-field of tiny dots. Everything uses a monospace font ("Courier New"). The palette is phosphor green (#22c55e, #4ade80, body text #a0ffa0). Each room has ONE accent color (amber #f59e0b, cyan #22d3ee, magenta #e879f9, red #f43f5e, violet #a855f7, lime #84cc16) used for its glow, border, and status light.
>
> **Top HUD bar (full width, ~58px, dark green gradient):** a gear/logo tile reading "VAULT 9000 / LVL 13"; a couple of small stat tiles (e.g. an emoji + "HAPPINESS 88%"); then horizontal resource bars labelled REVENUE, COSTS, NET PROFIT — each is a tiny label above a thin colored progress bar; on the right a small "● ONLINE" status and a couple of buttons.
>
> **Body — "floors":** stacked horizontal rows. Each floor has a tiny uppercase label (e.g. "COMMAND DECK") and a row of **room cards**.
>
> **Each room card (~170px wide, 150px tall):** a dark panel with a thin 1px accent-colored border. Inside, layered: (1) a background image slot (use a placeholder dark gradient if no image); (2) a soft radial "lamp glow" in the room's accent color from the top; (3) a darker vignette around the edges; (4) a character image slot centered near the bottom; (5) the room NAME in the accent color with a glow text-shadow, plus a small grey role line under it; (6) a small blinking status dot + status text top-right; (7) a thin activity-progress bar pinned to the bottom edge. On hover, lighten slightly.
>
> **Animations (CSS keyframes):** status dots blink; the character gently bobs up and down; the background image very slowly zooms/pans (Ken-Burns); the accent glow softly pulses; a faint horizontal scanline sweeps down the whole page. Respect prefers-reduced-motion.
>
> **Data:** a mock array of ~8–10 rooms (id, name, role, accentColor, status, activityPercent, image, character). Render them across 2–3 floors. Example rooms: COMMAND (Coordination, violet), INTERFACE (Display Systems, green), QUALITY (Quality Control, red), WORKSHOP (Fabrication, amber), STUDIO (Design, magenta), LAB (Research, lime), SERVERS (Compute, cyan), COMMS (Signals, red).
>
> **Interaction:** clicking a room opens a centered modal (dark panel, accent border, glow) showing the room name, role, status and activity. Click outside to close.
>
> Make it look polished and game-like, readable, and self-contained in one file I can preview immediately.

When it finishes, you'll have a working dashboard that looks like the screenshots in this guide — minus your custom art, which you add next.

![What the build prompt produces](images/rooms-closeup.png)

---

## Page 3 — Step 1 (continued): Refinement Prompts

After the first build, paste these **one at a time** to polish. Each is a follow-up message in the same AI builder chat.

> **Polish the retro feel:**
> "Add a faint CRT scanline that sweeps down the page, a subtle star-field of blinking dots in the background, and make each room's accent glow softly pulse. Keep it tasteful, not flashy."

> **Add more floors / rooms:**
> "Add a third floor called 'PRODUCTION DECK' with four more rooms: ARCHIVE (Records, steel blue), REACTOR (Power, teal), AUDIO (Sound, magenta), MARKETS (Analysis, amber). Match the existing card style exactly."

> **Make it responsive:**
> "Make the layout responsive: on narrow screens, hide the resource bars in the top bar and let room cards wrap to fewer per row. Keep everything readable on mobile."

> **Recolor a room:**
> "Change the WORKSHOP room's accent color to bright amber (#f59e0b) — update its border, glow, status light, and activity bar to match."

> **Add the empty 'build' slot:**
> "At the end of each floor, add a 'vacant' card with a dashed border and a '+ BUILD ROOM' label, as a placeholder for adding new rooms."

Stop whenever it looks the way you want. You can always ask the builder for more tweaks in plain English.

---

## Page 4 — Step 2: Generate Your Room Art

The dashboard works with placeholder gradients, but the custom **isometric room art** and **character sprites** are what make it look like a real game. Generate them with any AI image tool using these prompts. Fill in the `{BRACKETS}`.

> **ROOM BACKGROUND — master prompt:**
> "Isometric 3/4 overhead view of a `{ROOM THEME — e.g. electronics workshop, server room, research lab, command desk}` inside a retro underground bunker, camera looking down at ~60°, like a shelter-management game. Hand-painted 2D game art, NOT photorealistic, NOT 3D, NOT pixel art. Landscape. One dominant accent color reading as `{ACCENT — e.g. warm amber, electric cyan}` (glowing screens, LED rows, light pools on the floor). Moody low light, bright lamp pool in the center, dark edges. No text, no logos, no watermarks."

> **CHARACTER — prompt:**
> "Full-body cartoon character of a `{ROLE — e.g. bunker technician in a jumpsuit}`, front-facing, simple flat 2D game-art style, bold clean outlines, slightly large head, full body head-to-feet, plain transparent background, no shadow, no text. Consistent style for a matching set."

> **HUD ICON — prompt:**
> "Minimalist flat icon of a `{SUBJECT — e.g. lightning bolt, water drop, gear}`, solid `{ACCENT COLOR}`, transparent background, thick clean strokes, no text, centered, for a 24px UI icon."

**Tips for any tool:** ask for **landscape** room backgrounds (Midjourney: `--ar 5:4`); ask for a **transparent background** on characters/icons (if your tool can't, generate on flat magenta and remove it with a free background remover); generate a whole **set with the same style sentence** so your rooms and characters match. Aim for one character per room and one background per room.

---

## Page 5 — Step 3: Drop It In, Make It Yours, License

**Add your art.** In your AI builder, upload your generated images (or drag them into the project's image folder) and tell the builder: *"Use my uploaded images — set each room's background to its room image and its character to its character sprite."* Match each file to a room by name.

**Make it yours — just ask the builder in plain English:**
- "Rename the rooms to: `{your names}`."
- "Change the brand from VAULT 9000 to `{your name}`."
- "Add a room called `{name}` on `{floor}` with a `{color}` accent."
- "Make the top bar show `{your stats}`."

**Publish it.** Most AI builders (v0, Bolt) deploy with one click, or let you download the project to host anywhere free (Vercel, Netlify, GitHub Pages).

**License & originality.** Everything in this guide is yours to use for personal and commercial projects, and to build dashboards for clients. Don't resell the guide itself. Images you generate are yours per your image tool's terms (check its commercial-use policy). The "AI Agent Vault 9000" name and styling here are original and generic; this product is *inspired by* the look of classic shelter-management games and is **not** affiliated with, endorsed by, or derived from any specific game or its trademarks. Name your own build whatever you like.

**That's the whole system — paste the prompts, generate your art, and you've got a command center that looks like a video game and is entirely your own.**

![A full multi-floor vault in action](images/overview.png)
