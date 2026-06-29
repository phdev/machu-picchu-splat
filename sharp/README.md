# PlayCanvas Single-Image Research Viewer

This generated preview package serves the existing PlayCanvas/SuperSplat viewer with the Machu Picchu single-image research candidates: SHARP, SEVA + InstantSplat, and one-image fallback baselines.

Research label: SHARP, SEVA, and InstantSplat outputs are research feasibility only; not cleared for Supernatural production/commercial use.

Public Pages URL after deploy:

```text
https://phdev.github.io/machu-picchu-splat/sharp/?scene=sharp-full
https://phdev.github.io/machu-picchu-splat/sharp/?scene=seva-instantsplat-full
```

Scenes:
- `sharp-full`: full SHARP SOG, about 11.25 MB.
- `sharp-lod50`: 50% SHARP LOD SOG, about 6.49 MB.
- `sharp-lod25`: 25% SHARP LOD SOG, about 3.38 MB.
- `seva-instantsplat-full`: SEVA synthetic views trained with InstantSplat, about 11.38 MB.
- `seva-instantsplat-lod50`: 50% SEVA + InstantSplat LOD SOG, about 5.75 MB.
- `seva-instantsplat-lod25`: 25% SEVA + InstantSplat LOD SOG, about 2.88 MB.
- `curved-shell`: smoother 1024-grid spherical curved-shell one-image baseline, about 4.8 MB.
- `curved-shell-lite`: original 256-grid curved-shell diagnostic, about 0.42 MB.
- `billboard`: one-image billboard baseline.

Serve from this directory with:

```sh
python3 -m http.server 8097 --bind 127.0.0.1
```

Then open `http://127.0.0.1:8097/?scene=seva-instantsplat-full`.
