# Ivert

:::::{div}
:class: landing-page-layout

::::{div}
:class: welcome-section-layout
# **Ivert**

::::

::::{grid} 1 2 3 5
:gutter: 2

:::{card}
:link: https://github.com/continuous-dems/ivert
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![rtd](/assets/images/logo-dark.svg)
Documentation
:::

:::{card}
:link: https://pypi.org/project/ivert
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![pypi](/assets/images/pypi-logo.png)
Releases on PyPi
:::

:::{card}
:link: https://anaconda.org/conda-forge/ivert
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![conda-forge](/assets/images/conda-forge-logo.png)
Releases on Conda-Forge
:::

:::{card}
:link: https://github.com/continuous-dems/ivert
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![github](/assets/images/github-logo.svg)
Source in Github
:::

:::{card}
:link: https://cudem.zulipchat.com/#narrow/channel/551520-IVERT
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![zulip](/assets/images/zulip-logo.png)
Zulip Chat
:::

::::

---

ICESat-2 Validation of Elevations Reporting Tool

**IVERT** validates Digital Elevation Models (DEMs) by comparing their elevations against ICESat-2 satellite photon data. It supports topographic, bathymetric, and mixed coastal DEMs, runs fully offline on any machine, and handles vertical datum conversions automatically.

---

```console
# 1. Set up IVERT's data directories and credentials (run once on a new machine)
# This creates the local ~/.ivert data directories and checks your ~/.netrc for NASA Earthdata Login credentials, offering to save them if they are not already present.
# Earthdata credentials are required to download ICESat-2 data (register for a free account).
$ ivert setup

# 2. Download ICESat-2 photon data for your area (bounding box in W/E/S/N order):
$ ivert database download -- -82.6/-82.5/27.25/27.35

# 3. Validate your DEM:
$ ivert validate sarasota_dem.tif -n "Sarasota, FL"

# 4. Check the output directory for sarasota_dem_results.h5, a validation plot (.png), and error exports (.tif, .gpkg).
```

![Ivert Results Sample](/assets/images/sarasota_ivert_plot.png)

:::::
