# Renova

[![Packages](https://img.shields.io/badge/Packages-59-blue?style=social&logo=r)](https://renova-r.r-universe.dev/packages) [![GitHub followers](https://img.shields.io/github/followers/renova-r?style=social&label=Followers)](https://github.com/orgs/renova-r/followers)

**Reproducible research needs living software.**

When CRAN packages fall out of maintenance, the science built on them goes dark. **Renova** is an autonomous multi-agent AI system that repairs and validates legacy R software. This public catalog showcases archived CRAN packages restored by the Renova engine and ready to install.

Project led by [Jing Jia](https://jjia131.github.io/), [Guanyang Wang](https://guanyangwang.github.io/), and [Peng Zhang](https://sites.google.com/site/pengzhang27182/).

Contact: [Jing Jia](mailto:jing.jia@rutgers.edu) · [Guanyang Wang](mailto:guanyang.wang@rutgers.edu).

Compute generously supported by [Open Math OS](https://www.openmathmodel.org/).

[Browse restored packages →](https://renova-r.r-universe.dev/packages)

## How Renova works

Renova coordinates specialized AI agents to restore archived CRAN packages. Agents diagnose problems, develop repairs, and validate results through an iterative workflow.

```mermaid
flowchart TD
    A["Archived CRAN packages"] --> B["Coordinator<br/>Diagnose & assign"]
    B --> C["Repair agents<br/>Code · dependencies · documentation"]
    C -->|"Up to 3 rounds"| C
    C --> D["Independent validation"]
    D -->|"Validated"| F["Release to the Renova catalog"]
    D -->|"Unresolved"| E["Specialist agents<br/>Repair & revalidate"]
    E -->|"Up to 2 additional rounds"| E
    E -->|"Validated"| F
    E -->|"Still unresolved"| G["Tracked for follow-up"]
```

## Install

Choose a package from the directory, then install it with:

```r
install.packages("PACKAGE", repos = c(
  Renova = "https://renova-r.r-universe.dev",
  CRAN = "https://cloud.r-project.org"
))
```
