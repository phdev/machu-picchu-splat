# Packaged Research Splats

research feasibility only; not cleared for Supernatural production/commercial use.

This package was generated locally by `spikes/mobile_vr_splat_feasibility/scripts/package_splats_for_viewer.sh`.

- Viewer directory: `/Users/peterhowell/mp-deploy`
- Standalone package: `False`
- Manifest: `splats/manifest.json`

## Packaged Assets

- `spag4d-research` -> `splats/machu_picchu_spag4d_research_only.sog`
- `sharp360-research` -> `splats/machu_picchu_sharp360_research_only.sog`
- `pano-360cities-research` -> `splats/machu_picchu_360cities_pano_bubble_research_only.sog`
- `vggt-research` -> `splats/machu_picchu_vggt_research_only.sog`
- `anysplat-research` -> `splats/machu_picchu_anysplat_research_only.sog`
- `sharp-refined-research` -> `splats/machu_picchu_sharp_refined_research_only.sog`
- `sharp-research-packaged` -> `splats/machu_picchu_sharp_research_only.sog`
- `sparse-ranked-research` -> `splats/machu_picchu_sparse_ranked_research_only.sog`

## Deploy Gate

Assets are not pushed by the packaging command. To deploy, run:

```bash
GH_PAGES_DEPLOY=1 bash spikes/mobile_vr_splat_feasibility/scripts/deploy_viewer_assets.sh
```
