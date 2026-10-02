# SPRINT: 3D parkour speedrun

A bright, toy-like 3D parkour speedrun game in **one self-contained `index.html`**.
No build step and no local assets. The only dependency is Three.js r160, loaded from a CDN (jsDelivr, with unpkg as a fallback).
All art is procedural and all audio is synthesised with the Web Audio API.

**Play:** open `index.html` from any static host (GitHub Pages works as-is).

## Controls

| Action | Keyboard / mouse | Touch |
| --- | --- | --- |
| Move | `W` `A` `S` `D` / arrows | Left thumb (floating stick) |
| Look | Mouse (click to capture) | Drag on the right half |
| Jump (hold = higher) / wall-jump | `Space` | JUMP |
| Slide at speed / crouch (hold mid-air to tuck) | `Shift` or `C` | SLIDE |
| Air dash | `E` or `Q` | DASH |
| Instant restart | `R` | ↻ |
| First / third person | `V` | VIEW |
| Pause | `Esc` (or `P`) | II |
| Mute | `M` | n/a |

## Courses

1. **Warm-Up**: straight platforms, simple jumps
2. **Sky Steps**: bigger gaps, floating platforms, two turns
3. **Low Road**: slide tunnels and low barriers
4. **Wall Street**: wall-run corridors
5. **Springboard**: bounce pads and vertical routes
6. **Machine Room**: moving platforms and spinning bars
7. **Skyline**: wall-run, wall-jump chimneys and air dashes
8. **Gauntlet**: everything, back to back

Finish a course to unlock the next one (or toggle **Unlock all courses** in Settings).
Best times, splits, medals, ghosts and settings are saved in `localStorage`.

## Tuning

Every gameplay value lives in the `CONFIG` object at the top of the script.
Courses are plain data in `COURSES`. Each entry lists platforms, walls, barriers, hazards, movers, pads, spinners, checkpoints, start, finish, palette and **tunable** medal times.
Each course has comments noting the jump distances it was designed around.

Append `?debug` to the URL to expose a small `window.__sprint` API used for automated testing.
