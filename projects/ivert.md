# Ivert

:::::{div}
:class: landing-page-layout

::::{div}
:class: welcome-section-layout
# **Ivert**

[ [Documentation](https://github.com/continuous-dems/ivert) ]
[ [Releases on PyPi](https://pypi.org/project/ivert) ]
[ [Releases on Conda-Forge](https://anaconda.org/conda-forge/ivert) ]
[ [Source on Github](https://github.com/continuous-dems/ivert) ]
[ [Zulip Chat](https://cudem.zulipchat.com/#narrow/channel/551520-IVERT) ]

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
