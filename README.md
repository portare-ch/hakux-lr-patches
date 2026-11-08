# hakuX-lr patches

XBE patches for [hakuX-lr](https://github.com/portare-ch/hakuX-lr) as
RetroArch cheat files: one folder per game release, one `.cht` per patch.
Each file holds one emulator-handled entry whose code is an `xbe-patch-v1`
patch, off by default. hakuX-lr's
[`native/README.linux.md`](https://github.com/portare-ch/hakuX-lr/blob/master/native/README.linux.md)
describes the format.

## Using a patch

1. Start the game in RetroArch with hakuX-lr.
2. Open **Quick Menu → Cheats → Load Cheat File (Replace)** and pick the `.cht`.
3. Enable the entry, choose **Apply Changes**, then **Quick Menu → Restart**.
4. For widescreen patches, set the core option **Screen Format** to
   **Widescreen** and RetroArch's aspect ratio to **Core provided**.

A patch applies only to the XBE whose CRC-32 and size it names. Another
revision boots unpatched, and the log says why. To return to the original,
disable the entry and restart.

Enable only one patch per XBE: if two enabled patches match the same
executable, neither applies. To combine edits, use a single entry, as in
`Widescreen + High LOD.cht`.

## Patches

| Game | Patch | Source | Tested |
| --- | --- | --- | --- |
| Baldur's Gate: Dark Alliance (USA) | Widescreen, High LOD, both | icup321 | yes |
| Baldur's Gate: Dark Alliance II (USA) | Widescreen | icup321 | yes |
| JSRF: Jet Set Radio Future (USA) | Widescreen | icup321 | yes |
| Spider-Man (USA) | Widescreen | icup321 | yes |
| Turok: Evolution (USA) | Widescreen | icup321 | yes |

The test notes are at the top of each `.cht`. icup321's patches come from
[XboxGraphicalPatches](https://github.com/icup321/XboxGraphicalPatches). The
widescreen patches change the 3D view only; the HUD stays stretched. Its
Dark Summit patch is missing: on the USA disc's XBE it writes back the
bytes that are already there.

## Contributing

Convert the patch with hakuX-lr's `tools/mods/xbe-to-cht.py`. It needs the
stock XBE and either the IPS or BPS patch (applied with Floating IPS) or the
patched XBE. Use `--note` to add these comment lines at the top of the file:

- the game, region and revision, and the XBE's file name;
- the patch's original author and source (a link);
- test results: the hakuX-lr build, and what was checked (scene, HUD, menus,
  cutscenes) and what still looks wrong.

```sh
python3 tools/mods/xbe-to-cht.py default.xbe "Game (16-9 Widescreen Patch).ips" \
  --note "Game (USA), default.xbe" --note "Patch: author, https://..." \
  --note "Tested: hakuX-lr ..., the scene at 16:9, HUD ..." > "Game (USA)/Widescreen.cht"
```
