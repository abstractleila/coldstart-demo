# Abstract Atomic · Cold Start Failure Model demo site

Static site, no build step. Three pages:

- `index.html`  landing: two domains, open one
- `battery.html`  unseen XJTU cells, wound-cell ASCII render, what-if physics
- `silicon.html`  real NASA PCoE #13 MOSFET runs plus synthetic units for four mechanisms, die-on-package ASCII render

All forecasts were produced offline by the trained checkpoints in `physics-informed-failure-prediction/artifacts/` and are embedded in the pages (see `run_horizons.py`, `run_semi.py`, `run_real.py`).

## Deploy to Vercel

```bash
cd demo-site
npx vercel --prod        # framework preset: Other, build command: none, output directory: .
```

Or push this folder to a GitHub repo under abstractleila and import it in the Vercel dashboard with no build command and `.` as the output directory. `vercel.json` turns on clean URLs so `/battery` and `/silicon` work.
