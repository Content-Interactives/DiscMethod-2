# DiscMethod-2 (Disk method)

Step-by-step Vite + React app: Riemann sums and disc approximations for a configurable plane curve (default linear slice in `App.jsx`), with a **12-step** wizard (`StepManager`), **Flexi** copy in `Template`, and a mix of **2D** chart components and **3D** `@react-three/fiber` / `three` scenes. Curriculum and placement metadata are in [`Standards.md`](Standards.md).

**Production:** [https://content-interactives.github.io/DiscMethod-2/](https://content-interactives.github.io/DiscMethod-2/)

---

## Stack

| Layer | Packages |
|--------|-----------|
| UI | React 19 |
| 3D | `three`, `@react-three/fiber`, `@react-three/drei` |
| Diagrams | `react-xarrows`, `react-arrow` |
| Build | Vite 7, `@vitejs/plugin-react` |
| Styling | Tailwind 3, PostCSS, Autoprefixer |
| Types | `.tsx` (`StepManager`, step slices) + `.jsx` |

---

## Build

`vite.config.js`: `base: '/DiscMethod-2/'` for GitHub Pages.

| Script | Command |
|--------|---------|
| Dev | `npm run dev` |
| Build | `npm run build` → `dist/` |
| Preview | `npm run preview` |
| Deploy | `npm run deploy` (`gh-pages -d dist`) |

---

## Layout

| Path | Role |
|------|------|
| `src/main.jsx` / `App.jsx` | Mount, `current_step` state, `flexi_steps`, `functionConfigs.linear` |
| `src/template/` | `Template.jsx`, Flexi assets, header/footer chrome |
| `src/components/` | `StepManager`, `functionConfigs`, per-step views (`Step1_2DFunction.jsx` … `ThreeDSteps.tsx`) |
| `src/components/subComponents/` | `FunctionPlot`, `CoordinateGrid`, `RiemannSum`, … |
| `public/flexi-gallery.html` | Optional static gallery helper |

`App.jsx` wires `StepManager` with `functionConfigs.linear` and a fixed `total_steps = 12`.

---

## Product / curriculum

See [`Standards.md`](Standards.md) for subject area, topic, and pending standard codes.
