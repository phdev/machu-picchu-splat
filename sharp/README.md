# PlayCanvas Single-Image Research Viewer

This generated preview package serves the existing PlayCanvas/SuperSplat viewer with the Machu Picchu single-image research candidates: SHARP, SEVA + InstantSplat, and one-image fallback baselines.

Research label: SHARP, SEVA, and InstantSplat outputs are research feasibility only; not cleared for Supernatural production/commercial use.

Public Pages URL after deploy:

```text
https://phdev.github.io/machu-picchu-splat/sharp/?scene=sharp-full
https://phdev.github.io/machu-picchu-splat/sharp/?scene=seva-instantsplat-tuned-full
https://phdev.github.io/machu-picchu-splat/sharp/?scene=seva-instantsplat-jun30-full
```

Scenes:
- `sharp-full`: full SHARP SOG, about 11.25 MB.
- `sharp-lod50`: 50% SHARP LOD SOG, about 6.49 MB.
- `sharp-lod25`: 25% SHARP LOD SOG, about 3.38 MB.
- `seva-instantsplat-tuned-full`: SEVA + InstantSplat with giant scale outliers removed, `seva_instantsplat_20260629T165620Z_tuned_full.sog`, about 9.81 MB.
- `seva-instantsplat-tuned-lod50`: 50% tuned LOD, `seva_instantsplat_20260629T165620Z_tuned_lod50.sog`, about 5.07 MB.
- `seva-instantsplat-tuned-lod25`: 25% tuned LOD, `seva_instantsplat_20260629T165620Z_tuned_lod25.sog`, about 2.53 MB.
- `seva-instantsplat-jun30-full`: Jun30 SEVA conservative nearby views trained with InstantSplat, `seva_instantsplat_20260630T130026Z_full.sog`, about 9.50 MB.
- `seva-instantsplat-jun30-lod50`: Jun30 50% LOD, `seva_instantsplat_20260630T130026Z_lod50.sog`, about 4.90 MB.
- `seva-instantsplat-jun30-lod25`: Jun30 25% LOD, `seva_instantsplat_20260630T130026Z_lod25.sog`, about 2.47 MB.
- `seva-instantsplat-full`: raw SEVA synthetic views trained with InstantSplat, `seva_instantsplat_20260629T165620Z_full.sog`, about 11.37 MB.
- `seva-instantsplat-lod50`: raw 50% SEVA + InstantSplat LOD SOG, `seva_instantsplat_20260629T165620Z_lod50.sog`, about 5.75 MB.
- `seva-instantsplat-lod25`: raw 25% SEVA + InstantSplat LOD SOG, `seva_instantsplat_20260629T165620Z_lod25.sog`, about 2.87 MB.
- `curved-shell`: smoother 1024-grid spherical curved-shell one-image baseline, about 4.8 MB.
- `curved-shell-lite`: original 256-grid curved-shell diagnostic, about 0.42 MB.
- `billboard`: one-image billboard baseline.

InstantSplat tuning notes:
- Dedicated settings: `instantsplat_research.json`, initial camera `[0,0,0]`, target `[0,0,4]`, FOV `75`.
- Tuned assets use SplatTransform scale-outlier filtering: `-V scale_0,lte,0.02 -V scale_1,lte,0.02 -V scale_2,lte,0.02`.
- This removes the worst long streaks from giant splats. It does not fix SEVA hallucinated sky/terrain geometry.
- The Jun30 run used the conservative SEVA subset: hero, left/right 0.25m, and left/right 0.50m. The mobile-VR harness flagged the Jun30 full PLY as `yes_card_or_missing_parallax`, so treat it as a viewer/debug candidate, not a solved mobile scenic asset.
- InstantSplat scenes default to paused animation because the viewer's generated fly-through enters failed sky/edge splats. Add `&anim` to the URL to re-enable that generated animation.

Serve from this directory with:

```sh
python3 -m http.server 8097 --bind 127.0.0.1
```

Then open `http://127.0.0.1:8097/?scene=seva-instantsplat-jun30-full`.
