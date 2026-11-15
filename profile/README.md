# Renova

[![GitHub followers](https://img.shields.io/github/followers/renova-r?style=social&label=Followers)](https://github.com/orgs/renova-r/followers)

**Reproducible research needs living software.**

When CRAN packages fall out of maintenance, the science built on them goes dark. **Renova** is an autonomous multi-agent AI system that repairs and validates legacy R software. This public catalog showcases [![59](https://raw.githubusercontent.com/renova-r/.github/da71271801bed34a25fa8b5ce5f38333027b86ed/profile/assets/package-count.svg)](https://renova-r.r-universe.dev/packages) archived CRAN packages restored by the Renova engine and ready to install.

Project led by [Jing Jia](https://jjia131.github.io/), [Guanyang Wang](https://guanyangwang.github.io/), and [Peng Zhang](https://sites.google.com/site/pengzhang27182/).

Compute generously supported by [Open Math OS](https://www.openmathmodel.org/).

[Browse restored packages →](https://renova-r.r-universe.dev/packages)

## Install

Choose a package from the directory, then install it with:

```r
install.packages("PACKAGE", repos = c(
  Renova = "https://renova-r.r-universe.dev",
  CRAN = "https://cloud.r-project.org"
))
```
