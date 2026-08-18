---
site:
  hide_toc: true
  hide_outline: true
  hide_title_block: true
---
# Fetchez

:::::{div}
:class: landing-page-layout

::::{div}
:class: welcome-section-layout
# **Fetchez**

[ [Documentation](https://fetchez.readthedocs.io) ]
[ [Releases on PyPi](https://pypi.org/project/fetchez) ]
[ [Releases on Conda-Forge](https://anaconda.org/conda-forge/fetchez) ]
[ [Source on Github](https://github.com/continuous-dems/fetchez) ]
[ [Zulip Chat](https://cudem.zulipchat.com/#narrow/channel/560691-Fetchez) ]

::::

---

**Fetchez** is a robust, highly modular and extensible Python framework designed to orchestrate complex geospatial data engineering workflows.

Originally developed as the core fetching engine for the [CUDEM](https://github.com/ciresdem/cudem) project, Fetchez has evolved into a standalone geospatial ETL platform. It seamlessly retrieves Bathymetry, Topography, Imagery, and Oceanographic data from dozens of global repositories (NOAA, USGS, Copernicus, ESA) and processes it on the fly.

---

### Fetch and process data:

```python
import fetchez

# Fetch Electronic Nautical Chart data from NOAA
files = fetchez.get("charts", region=[-120, -118, 33, 34], hooks=['unzip', 'filename_filter:match=.000', 'audit'])
```


### Define resusable YAML data Bundles:

```yaml
name: grav_and_bath
description: >
  Some fast bathymetry data sources.
modules:
  - module: margrav
    args:
      weight: .01
  - module: nos_hydro
    args:
      datatype: "xyz"
      weight: .35
    hooks:
      - name: unzip
      - name: set_datatype
        args:
          data_type: "nos_xyz"
  - module: charts
    args:
      weight: .15
    hooks:
      - name: unzip
      - name: filename_filter
        args:
          match: ".000"
          stage: "file"
      - name: set_datatype
        args:
          data_type: "charts_000"
```

```python
# Fetch the custom bundle
files = fetchez.get("grav_and_bath", region=[-120, -118, 33, 34])
```
:::::
