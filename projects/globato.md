# Globato

:::::{div}
:class: landing-page-layout

::::{div}
:class: welcome-section-layout
# **Globato**

[ [Documentation](https://globato.readthedocs.io) ]
[ [Releases on PyPi](https://pypi.org/project/globato) ]
[ [Releases on Conda-Forge](https://anaconda.org/conda-forge/globato) ]
[ [Source on Github](https://github.com/continuous-dems/globato) ]
[ [Zulip Chat](https://cudem.zulipchat.com/#narrow/channel/560691-Globato) ]

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
