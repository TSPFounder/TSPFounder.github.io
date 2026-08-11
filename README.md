# Dream World Maker — website

Static landing page for [Dream World Maker](https://github.com/TSPFounder/DWMStudio), served by GitHub Pages.

## Structure

```
index.html          single page, all CSS inline — no build step, no dependencies
assets/img/         web-sized JPEGs (resized from C:\DreamWorldMaker\Images)
.nojekyll           skip Jekyll processing
```

## Editing

Open `index.html` and edit. There is no framework and nothing to compile — commit and push to
`main` and GitHub Pages redeploys within a minute.

## Images

Source PNGs live in `C:\DreamWorldMaker\Images` (UE 5.3 captures, 2–4 MB each) and are **not**
committed. They were resized to 1600px-wide JPEGs at quality 82 for the web, taking the page
from ~25 MB of images to ~1.9 MB.

To regenerate after adding a new capture, resize with .NET `System.Drawing` (ImageMagick is not
installed on the build machine) and drop the result in `assets/img/`.

The `Images/` folder in this directory is gitignored — it contains Dreamstime comps that are not
licensed for publication.

## Content sources

Copy is drawn from the project's own docs, so keep them in sync when the story changes:

| Section | Source |
|---|---|
| Tagline, story hook, CTA | the Kit landing page |
| Five communities | `DEMO_ECONOMY.md`, `DWM_MVP_Storyline.md` |
| Stone ledger | `DEMO_ECONOMY.md` §1, `ECONOMY_SCHEMA_SPEC.md` |
| Engineering pipeline | `README.md` (toolchain table), `SCOPE.md` |

### One constraint worth keeping

`SCOPE.md` records that the turbine rotor on screen is **not** driven live by the Simulink model
in the MVP — the asset animates itself, and a rotor turning at a steady rate looks identical
either way. The engineering section says the simulation *data* is real model output and
explicitly declines the stronger claim. Don't let that wording drift.

Likewise `DWM_MVP_Storyline.md` asks that the theme be demonstrated and never announced. The
"stronger together" idea appears here only as the ledger arithmetic and as Hank's own line —
not as site copy asserting it.
