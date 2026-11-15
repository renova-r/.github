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

Examples include adapting code to newer R versions, fixing compilation and dependency problems, registering missing methods, and correcting documentation and package metadata.

```mermaid
---
config:
  theme: base
  themeVariables:
    fontSize: 14px
    lineColor: "#94a3b8"
    edgeLabelBackground: "#ffffff"
  flowchart:
    nodeSpacing: 18
    rankSpacing: 22
    padding: 8
    wrappingWidth: 240
---
flowchart TD
    A["Archived CRAN<br/>packages"] --> B["Coordinator<br/>Diagnose & assign"]
    B --> C["Repair agents<br/>Code · deps · docs"]
    C -->|"Up to 3 rounds"| C
    C --> D["Independent validation"]
    D -->|"Validated"| F["Release & catalog"]
    D -->|"Unresolved"| E["Specialist agents<br/>Repair & revalidate"]
    E -->|"Up to 2 additional rounds"| E
    E -->|"Validated"| F
    E -->|"Still unresolved"| G["Follow-up queue"]

    classDef agent fill:#e9f2ff,stroke:#7aa2d6,color:#17467b,stroke-width:1px
    classDef activity fill:#e8f5ed,stroke:#7eaf94,color:#245b3e,stroke-width:1px
    classDef context fill:#f2f4f7,stroke:#b0bbc7,color:#4b586b,stroke-width:1px
    class B,C,E agent
    class D,F activity
    class A,G context
```

## Install

Choose a package from the directory, then install it with:

```r
install.packages("PACKAGE", repos = c(
  Renova = "https://renova-r.r-universe.dev",
  CRAN = "https://cloud.r-project.org"
))
```
