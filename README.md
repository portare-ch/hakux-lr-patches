# hakuX-lr patches

Original Xbox patches for hakuX-lr in RetroArch. Each `.cht` is disabled by
default and targets a specific XBE revision. Use a core build with
[XBE patch support](https://github.com/portare-ch/hakuX-lr/pull/169).

## Use a patch

1. Start the game in RetroArch with hakuX-lr.
2. Open **Quick Menu → Cheats → Load Cheat File (Replace)** and select the
   `.cht`. Use **Load Cheat File (Append)** to keep existing cheats.
3. Enable the patch and select **Apply Changes**.
4. For widescreen, set the core's **Screen Format** to **Widescreen** and
   RetroArch's **Aspect Ratio** to **Core provided**.
5. Select **Quick Menu → Restart**.

The core checks the XBE's CRC-32 and size before applying a patch. It logs
revision mismatches and conflicts. Enable one patch per XBE, or use a combined
entry. To revert a patch, disable it, apply changes, and restart.

## Patches

| Game | Patches |
| --- | --- |
| Baldur's Gate: Dark Alliance (USA) | [Widescreen](Baldur%27s%20Gate%20-%20Dark%20Alliance%20%28USA%29/Widescreen.cht), [High LOD](Baldur%27s%20Gate%20-%20Dark%20Alliance%20%28USA%29/High%20LOD.cht), [Widescreen + High LOD](Baldur%27s%20Gate%20-%20Dark%20Alliance%20%28USA%29/Widescreen%20%2B%20High%20LOD.cht) |
| Baldur's Gate: Dark Alliance II (USA) | [Widescreen](Baldur%27s%20Gate%20-%20Dark%20Alliance%20II%20%28USA%29/Widescreen.cht) |
| Conker: Live & Reloaded (USA) | [60 fps](Conker%20-%20Live%20%26%20Reloaded%20%28USA%29/60%20fps.cht) |
| Crimson Skies: High Road to Revenge (USA) | [60 fps](Crimson%20Skies%20-%20High%20Road%20to%20Revenge%20%28USA%29/60%20fps.cht) |
| Forza Motorsport (World) | [60 fps](Forza%20Motorsport%20%28World%29/60%20fps.cht) |
| Halo 2 (USA) | [60 fps](Halo%202%20%28USA%29/60%20fps.cht) |
| Halo: Combat Evolved (USA, Rev 2) | [60 fps](Halo%20-%20Combat%20Evolved%20%28USA%29%20%28Rev%202%29/60%20fps.cht) |
| Jet Set Radio Future (USA) | [Widescreen](JSRF%20-%20Jet%20Set%20Radio%20Future%20%28USA%29/Widescreen.cht) |
| Otogi 2: Immortal Warriors (USA) | [60 fps](Otogi%202%20-%20Immortal%20Warriors%20%28USA%29/60%20fps.cht) |
| Spider-Man (USA) | [Widescreen](Spider-Man%20%28USA%29/Widescreen.cht) |
| Turok: Evolution (USA) | [Widescreen](Turok%20-%20Evolution%20%28USA%29/Widescreen.cht) |

The widescreen and High LOD patches come from [icup321's XboxGraphicalPatches](https://github.com/icup321/XboxGraphicalPatches). The 60 fps patches are hakuX's mods, converted from [`mods/`](mods/README.md).
Each file records the tested build and result. Widescreen expands the 3D view
to 16:9. The HUD remains stretched.

## Contribute a patch

From the hakuX-lr checkout, convert the stock XBE and an IPS, BPS, or patched
XBE. IPS and BPS inputs require Floating IPS (`flips`).

```sh
python3 tools/mods/xbe-to-cht.py default.xbe widescreen.ips > Widescreen.cht
```

Put the file in the folder for its game release. Use `--note` to record the
region, revision, XBE filename, original author, source, and test results.
Include the core build and what you checked in-game, including any visible
issues.

## Android mods

[`mods/`](mods/README.md) holds the hakuX-lr Android app's mods and cheats,
one folder per title ID and version. hakuX-lr includes this repository as its
`patches` submodule and packs that folder into the APK. Some mods need more
than byte patches (`refresh: 120`, title-update sections), so not every mod
has a `.cht` yet. Convert a mod's XBE patches with hakuX-lr's
`tools/mods/mod-to-cht.py`.
