# Telm

**A text-based lighting control console for theatre.**

> 🚧 Early development. Nothing here is usable yet. Watch or star the repo to follow along.

Telm is a lighting console where cues are written as short, readable code instead of being hidden behind menus. The same language runs in cue files and on the live command line, so what you type is exactly what the stage does.

```
---
id: 12
name: Kitchen, morning
up: 3s
---
own = baseline
kitchen = 70
movers.position = upstage
201.cct = 3200K
```

## Goals

- **Readable cues.** Cue and preset code describes *what* changes; timing lives in the cue header. One statement per line, with an editor that gives completions, diagnostics and hints.
- **Predictable playback.** Tracking and from-live cue lists, cue groups, linked lists and GOTO that always produces the same look in a tracking list.
- **Runs anywhere.** One headless core engine, used by a small Raspberry Pi appliance and a desktop app.
- **Open protocols.** sACN, Art-Net and USB DMX output; MIDI, OSC and GPIO input.
- **Honest colour.** Colour values are stored exactly as written. Native formats pass through untouched; translation between fixtures uses CIE XYZ and OKLab.
- **Portable shows.** A single, versioned show file with fixture types embedded.

## Status

Telm is in the design stage. The core engine, cue language and playback model are being specified before implementation begins.

## Built with

Rust for the core engine; Tauri with a web-based UI for the desktop app.

## The name

*Telm* (pronounced "telm") is the Catalan form of Saint Elmo, patron of sailors. St. Elmo's fire is the blue-violet glow that appears on ships' masts during storms: light where you don't expect it. It's an old Catalan name, short, and easy to say in Catalan, Spanish and English.

## Licence

MIT.
