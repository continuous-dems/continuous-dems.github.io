# Transformez

:::::{div}
:class: landing-page-layout

::::{div}
:class: welcome-section-layout
# **Transformez**

::::

::::{grid} 1 2 3 5
:gutter: 2

:::{card}
:link: https://transformez.readthedocs.io
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![rtd](/assets/images/logo-dark.svg)
Documentation
:::

:::{card}
:link: https://pypi.org/project/transformez
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![pypi](/assets/images/pypi-logo.png)
Releases on PyPi
:::

:::{card}
:link: https://anaconda.org/conda-forge/transformez
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![conda-forge](/assets/images/conda-forge-logo.png)
Releases on Conda-Forge
:::

:::{card}
:link: https://github.com/continuous-dems/transformez
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![github](/assets/images/github-logo.svg)
Source in Github
:::

:::{card}
:link: https://cudem.zulipchat.com/#narrow/channel/562904-Transformez
:class: p-2 text-center hover:bg-slate-50 border rounded transition-all cursor-pointer select-none no-underline block
:class-body: p-0 m-0 flex flex-col items-center justify-center gap-1 no-underline

![zulip](/assets/images/zulip-logo.png)
Zulip Chat
:::

::::

---

**Transformez** is a standalone Python engine for converting geospatial data between vertical datums.

Built with `fetchez` to use the latest available transformations, transformez performs vertical transformations utilizing various sources such as VDatum, FES, Proj, and more.

```console
$ transformez grid -R loc:"new orleans" -E 3s -I mllw -O 5703 --preview
```

![Shift Grid Example](/assets/images/mllw2nvd.png)

---

:::::
