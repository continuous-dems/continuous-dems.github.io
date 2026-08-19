# Fetchez

:::::{div}
:class: landing-page-layout

::::{div}
:class: welcome-section-layout
# **Fetchez**

::::

::::{grid} 1 2 3 5
:gutter: 2

:::{card}
:link: https://fetchez.readthedocs.io
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![rtd](/assets/images/logo-dark.svg)
Documentation
:::

:::{card}
:link: https://pypi.org/project/fetchez
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![pypi](/assets/images/pypi-logo.png)
Releases on PyPi
:::

:::{card}
:link: https://anaconda.org/conda-forge/fetchez
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![conda-forge](/assets/images/conda-forge-logo.png)
Releases on Conda-Forge
:::

:::{card}
:link: https://github.com/continuous-dems/fetchez
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![github](/assets/images/github-logo.svg)
Source in Github
:::

:::{card}
:link: https://cudem.zulipchat.com/#narrow/channel/560691-Fetchez
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![zulip](/assets/images/zulip-logo.png)
Zulip Chat
:::

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


### Define reusable YAML data Bundles:

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
