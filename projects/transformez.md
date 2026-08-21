# Transformez

:::::{div}
:class: landing-page-layout

::::{div}
:class: welcome-section-layout
# **Transformez**

::::

::::{grid} 1 2 3 5

:::{card}
:link: https://transformez.readthedocs.io

![rtd](/assets/images/logo-dark.svg)
Documentation
:::

:::{card}
:link: https://pypi.org/project/transformez

![pypi](/assets/images/pypi-logo.png)
Releases on PyPi
:::

:::{card}
:link: https://anaconda.org/conda-forge/transformez

![conda-forge](/assets/images/conda-forge-logo.png)
Releases on Conda-Forge
:::

:::{card}
:link: https://github.com/continuous-dems/transformez

![github](/assets/images/github-logo.svg)
Source in Github
:::

:::{card}
:link: https://cudem.zulipchat.com/#narrow/channel/562904-Transformez

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
