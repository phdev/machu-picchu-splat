# PlayCanvas SHARP Research Viewer

This generated preview package serves the existing PlayCanvas/SuperSplat viewer with the SHARP Machu Picchu SOG variants.

Research label: SHARP model outputs are research feasibility only; not cleared for Supernatural production/commercial use.

Public Pages URL after deploy:

```text
https://phdev.github.io/machu-picchu-splat/sharp/?scene=sharp-full
```

Scenes:
- `sharp-full`: full SHARP SOG, about 11.25 MB.
- `sharp-lod50`: 50% SHARP LOD SOG, about 6.49 MB.
- `sharp-lod25`: 25% SHARP LOD SOG, about 3.38 MB.
- `billboard`: one-image billboard baseline.

Serve from this directory with:

```sh
python3 -m http.server 8097 --bind 127.0.0.1
```

Then open `http://127.0.0.1:8097/?scene=sharp-full`.
