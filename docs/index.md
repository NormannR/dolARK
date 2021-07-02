# DolARK

## Introduction

DolARK is an experimental project to solve heterogenous agents models with infinitely lived agents. It relies on [Dolo](https://EconForge.github.io/dolo/) to model individual agents behaviors and extends its modeling language to describe distributions of agents and aggregate dynamics.

We aim to support the following basic features on the household's side:

   - homogeneous as well as heterogeneous preferences
   - idiosyncratic shocks, which need not to be i.i.d and whose process can be conditioned by the value of aggregate shocks, as in Krusell and Smith (1998)

As for the aggregate side, the following features shall be supported :

   - presence of aggregate shocks
   - presence of aggregate state variables

In terms of resolution method, we aim at implementing Reiter (2009) with some state-space reduction methods, whether it be the vanilla one or the DCT-related one Bayer and Luetticke (2020) make a case for.

!!!note

	2021, June 24 update: conditional processes still need to be implemented in dolo. Moreover, the considered processes for idiosyncratic shocks need to be discretizable into Markov processes. For now, Reiter (2009) is the only implemented method.

## Frequently Asked Questions

No question was ever asked. Certainly because it's all very clear.

## Developers' Corner

### Contribute to the documentation

Documentation is contained in the docs subdirectory.
In order to develop it locally:

```
pip install mkdocs
pip install pymdown-extensions
```

Then `mkdocs serve` from within DolARK repository.
On a regular basis, latest version is deployed to github pages [pages](http://www.econforge.org/dolARK/) (for now) using `mkdocs gh-deploy`.

Notebooks are written as Python files and can be opened with Jupyter using the
[jupytext](https://github.com/mwouts/jupytext) extension.
