# Penrose Window

A window onto an endless Penrose tiling that you can pan and zoom around forever.

Live: https://dglittle.github.io/penrose-window/

## How it works

It uses N. G. de Bruijn's *multigrid* method (1981). Take `d` sets of evenly
spaced parallel lines, each set turned by 1/`d` of a circle from the last.
Every point where two lines cross becomes one rhombus, and the rhombi fit
together edge to edge into a tiling that never repeats. With `d = 5` (a
*pentagrid*) you get the Penrose rhombus tiling; `d = 8` gives the 8-fold
Ammann–Beenker tiling.

- **− / +** (top left): change `d`, the number of grids.
- **Left slider**: morphs between the grid of lines and the tiling, so you can
  watch each crossing turn into its rhombus.
- **Right slider**: shifts the grids against each other (de Bruijn's offsets),
  which changes which tiling you get.
- Drag / scroll to pan, pinch / ctrl-scroll to zoom. Colors are random on each load.

Everything is drawn on the GPU (WebGL).

## URL options

- `d=8`: number of grids (default 5)
- `g=0.2`: spacing between lines, i.e. zoom (default 0.1)
- `s1=…`, `s2=…`: starting slider positions (0–1000)
- `nohud`: hide the sliders

Example: https://dglittle.github.io/penrose-window/?d=8

## Run it

One file, `index.html` (it loads gl-matrix from a CDN). Open it in a browser.

## Further reading

- N. G. de Bruijn, "Algebraic theory of Penrose's non-periodic tilings of the plane", 1981: https://doi.org/10.1016/1385-7258(81)90016-0
- Greg Egan's explainer and applet: https://www.gregegan.net/APPLETS/12/deBruijnNotes.html
- [Penrose tiling on Wikipedia](https://en.wikipedia.org/wiki/Penrose_tiling)

## License

MIT
