# Globato

:::::{div}
:class: landing-page-layout

::::{div}
:class: welcome-section-layout
# **Globato**

::::{grid} 1 2 3 5
:gutter: 2

:::{card}
:link: https://globato.readthedocs.io
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![rtd](/assets/images/logo-dark.svg)
Documentation
:::

:::{card}
:link: https://pypi.org/project/globato
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![pypi](/assets/images/pypi-logo.png)
Releases on PyPi
:::

:::{card}
:link: https://anaconda.org/conda-forge/globato
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![conda-forge](/assets/images/conda-forge-logo.png)
Releases on Conda-Forge
:::

:::{card}
:link: https://github.com/continuous-dems/globato
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![github](/assets/images/github-logo.svg)
Source in Github
:::

:::{card}
:link: https://cudem.zulipchat.com/#narrow/channel/568984-GLOBATO
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![zulip](/assets/images/zulip-logo.png)
Zulip Chat
:::

::::

---

**Globato** is the user-facing geospatial engine of the Continuous-DEMs ecosystem. It is designed for the rapid development, blending, and processing of high-accuracy Topo-Bathy Digital Elevation Models (DEMs).

Built on top of the `fetchez` (orchestration) and `transformez` (horizontal and vertical datums) libraries, `globato` abstracts away the complexity of DEM development. It allows users to generate massive, seamless DEMs using declarative YAML recipes, intuitive command-line tools, or a python API.

---

```console
$ globato build -R loc:"San Diego" crm-bathy-topo -E 1s -O san_diego --shared-cache sd_data -D sd_crm
```

![San Diego 1 Arc-Second CRM](/assets/images/san_diego_crm.png)

:::::
