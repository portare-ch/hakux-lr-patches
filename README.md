# hakuX-lr patches

Original Xbox patches for hakuX-lr in RetroArch: one `.cht` per game, with an
entry for each patch. Every entry is disabled by default and targets a
specific XBE revision. Use a core build with
[XBE patch support](https://github.com/portare-ch/hakuX-lr/pull/169).

## Use a patch

1. Start the game in RetroArch with hakuX-lr.
2. Open **Quick Menu → Cheats → Load Cheat File (Replace)** and select the
   game's `.cht`. Use **Load Cheat File (Append)** to keep existing cheats.
   RetroArch loads the file by itself when it is in its cheats folder for
   the core under the game file's name.
3. Enable the patches you want and select **Apply Changes**.
4. For widescreen, set RetroArch's **Aspect Ratio** to **Core provided**.
   The core's **Screen Format** is **Auto** by default, which sets the console
   to widescreen while a widescreen patch is applied; with a core older than
   that option, set **Screen Format** to **Widescreen** yourself.
5. Select **Quick Menu → Restart**.

The core checks the XBE's CRC-32 and size before applying a patch, and logs
revision mismatches and conflicts. A game's patches go on together: enable
any of its entries. Two patches conflict only when they write different
bytes to the same place, and then neither is applied. To revert a patch,
disable it, apply changes, and restart.

Applying several patches of one game together needs hakuX-lr newer than
0.33.3. An older core applies none when two are on: enable one entry at a
time there.

The widescreen patches end their code with `screen=widescreen`, which tells
the core's **Screen Format: Auto** to set the console to widescreen. This
needs hakuX-lr newer than 0.33.3: an older core refuses a code with that
marker and logs it. Remove ` screen=widescreen` from the entry's code to use
it with an older core.

## Patches

| Game | Patch | Credit |
| --- | --- | --- |
| [Baldur's Gate: Dark Alliance (USA)](Baldur%27s%20Gate%20-%20Dark%20Alliance%20%28USA%29.cht) | Widescreen (16:9) | [icup321](https://github.com/icup321/XboxGraphicalPatches) |
|  | Force High LOD | [icup321](https://github.com/icup321/XboxGraphicalPatches) |
| [Baldur's Gate: Dark Alliance II (USA)](Baldur%27s%20Gate%20-%20Dark%20Alliance%20II%20%28USA%29.cht) | Widescreen (16:9) | [icup321](https://github.com/icup321/XboxGraphicalPatches) |
| [Burnout 3: Takedown (USA)](Burnout%203%20-%20Takedown%20%28USA%29.cht) | 720p (1280x720) | [hakuX-lr](https://github.com/portare-ch/hakux-lr-patches/pull/9) |
| [Conker: Live & Reloaded (USA)](Conker%20-%20Live%20%26%20Reloaded%20%28USA%29.cht) | 60 fps | [hakuX](https://github.com/portare-ch/hakux-lr-patches/blob/be5d88c/mods/4D530051.2/60fps/mod.txt) |
| [Crimson Skies: High Road to Revenge (USA)](Crimson%20Skies%20-%20High%20Road%20to%20Revenge%20%28USA%29.cht) | 60 fps | [hakuX](https://github.com/portare-ch/hakux-lr-patches/blob/be5d88c/mods/4D530021.1/60fps/mod.txt) |
| [Dead or Alive 3 (USA)](Dead%20or%20Alive%203%20%28USA%29.cht) | 128 MB memory | [hakuX-lr](https://github.com/portare-ch/hakux-lr-patches/pull/5) |
|  | 720p (1280x720) | [hakuX-lr](https://github.com/portare-ch/hakux-lr-patches/pull/5) |
| [Forza Motorsport (World)](Forza%20Motorsport%20%28World%29.cht) | 60 fps | [hakuX](https://github.com/portare-ch/hakux-lr-patches/blob/be5d88c/mods/4D53006E.1/60fps/mod.txt) |
| [Halo 2 (USA)](Halo%202%20%28USA%29.cht) | 60 fps | [hakuX](https://github.com/portare-ch/hakux-lr-patches/blob/be5d88c/mods/4D530064.3/60fps/mod.txt) |
| [Halo: Combat Evolved (USA, Rev 2)](Halo%20-%20Combat%20Evolved%20%28USA%29%20%28Rev%202%29.cht) | 60 fps | [hakuX](https://github.com/portare-ch/hakux-lr-patches/blob/be5d88c/mods/4D530004.9/60fps/mod.txt) |
| [Jet Set Radio Future (USA)](JSRF%20-%20Jet%20Set%20Radio%20Future%20%28USA%29.cht) | Widescreen (16:9) | [icup321](https://github.com/icup321/XboxGraphicalPatches) |
| [Need for Speed: Underground (USA)](Need%20for%20Speed%20-%20Underground%20%28USA%29.cht) | Widescreen | [Nemesis2000](https://github.com/JayYardley/Xbox-Magic-Patches-by-Jay) |
|  | 60 fps | [Jao12345](https://github.com/JayYardley/Xbox-Magic-Patches-by-Jay) + [hakuX](https://github.com/portare-ch/hakux-lr-patches/blob/be5d88c/mods/45410047.1/60fps/mod.txt) |
|  | 720p (1280x720) | [hakuX-lr](https://github.com/portare-ch/hakux-lr-patches/pull/7) + [Nemesis2000](https://github.com/JayYardley/Xbox-Magic-Patches-by-Jay) |
| [Need for Speed: Underground 2 (USA)](Need%20for%20Speed%20-%20Underground%202%20%28USA%29.cht) | Widescreen | [Nemesis2000](https://github.com/JayYardley/Xbox-Magic-Patches-by-Jay) |
|  | 60 fps | [hakuX](https://github.com/portare-ch/hakux-lr-patches/blob/be5d88c/mods/4541005A.1/60fps/mod.txt) |
| [Otogi 2: Immortal Warriors (USA)](Otogi%202%20-%20Immortal%20Warriors%20%28USA%29.cht) | 60 fps | [hakuX](https://github.com/portare-ch/hakux-lr-patches/blob/be5d88c/mods/46530004.2/60fps/mod.txt) |
| [Project Gotham Racing 2 (USA)](Project%20Gotham%20Racing%202%20%28USA%29.cht) | 60 fps | [hakuX](https://github.com/portare-ch/hakux-lr-patches/blob/be5d88c/mods/4D53004B.2/60fps/mod.txt) |
| [Spider-Man (USA)](Spider-Man%20%28USA%29.cht) | Widescreen (16:9) | [icup321](https://github.com/icup321/XboxGraphicalPatches) |
| [Turok: Evolution (USA)](Turok%20-%20Evolution%20%28USA%29.cht) | Widescreen (16:9) | [icup321](https://github.com/icup321/XboxGraphicalPatches) |

## Contribute a patch

From the hakuX-lr checkout, convert the stock XBE and an IPS, BPS, or patched
XBE. IPS and BPS inputs require Floating IPS (`flips`).

```sh
python3 tools/mods/xbe-to-cht.py --widescreen default.xbe widescreen.ips > Widescreen.cht
```

`--widescreen` marks a patch for a 16:9 picture (`screen=widescreen`); leave
it out for other patches.

Use `--note` to record the region, revision, XBE filename, original author,
source, and test results. Include the core build and what you checked
in-game, including any visible issues.

Each game has one `.cht`, named after its release. Add the new entry to it
with `cht-join.py`, which keeps every entry's notes and refuses two patches
that write different bytes to the same place:

```sh
python3 tools/mods/cht-join.py --title "Game (USA)" "Game (USA).cht" Widescreen.cht > joined.cht
mv joined.cht "Game (USA).cht"
```

Make one entry per feature. Do not add an entry that repeats two others
combined: the core applies the enabled entries together.

## Memory cheats

A cheat entry's code can also be memory cheat lines instead of an XBE patch,
joined by `+` or new lines. They run in order every frame while the entry is
on:

| Line | Does |
|---|---|
| `w8 A V`, `w16 A V`, `w32 A V` | writes the 8 / 16 / 32-bit value V at A |
| `wf A F` | writes the float F at A |
| `if8 A C V`, `if16`, `if32`, `iff` | runs the lines up to `else` / `end` only if the value at A compares to V; C is `==`, `!=`, `<`, `>`, `<=`, `>=` (unsigned; signed floats for `iff`) or `&` (all of V's bits set) |
| `else`, `end` | the other branch; the end of an `if` (up to 8 deep) |


- An address A is a virtual address of the game (as a debugger or Cheat
  Engine on the console shows it: the XBE at 0x00010000, its heap above, the
  contiguous memory at 0x80000000). `[A]+N` (or `-N`) reads the 32-bit
  pointer at A and adds N; they nest: `[[0x00456700]+4]+0x10`. A pointer to
  unmapped memory skips the line; an unmapped address skips a write and
  makes an `if` false.
- Values are written only when they differ, little-endian as the Xbox
  stores them.
