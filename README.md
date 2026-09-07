# Metodi Latinov

Working in Bayesian statistics, statistical modeling and scientific computing.

[![GitHub followers](https://img.shields.io/github/followers/mlatinov?label=Follow&style=social)](https://github.com/mlatinov)
[![Email](https://img.shields.io/badge/email-metodilatinov%40abv.bg-blue)](mailto:metodilatinov@abv.bg)

---

## About Me

I come from a molecular biology background at Sofia University and have moved progressively deeper into statistical modeling and scientific computing. Most of my work sits at the point where a biological or physical question has to be turned into a model that can actually be fit, checked, and trusted — which usually means writing the model, writing the tooling around it, and writing the simulation study that tells me whether either one works.

### What I Do

I build Bayesian models for scientific and applied problems: hierarchical and multilevel structures for grouped experimental data, mechanistic and nonlinear models where the parameters carry physical meaning, causal models for questions that observational or trial data can't answer by regression alone, and spatial and time-series structure where the data demands it. Most of this is written in Stan and driven from R through reproducible `targets` pipelines.

Alongside the models, I develop the software that supports them — R packages for simulation, model validation, causal inference and visualization, and a preprocessor and language tooling that give Stan a package manager and namespaced imports it doesn't have natively.

---

## Research

<table>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/mlatinov/diet-exercise-rct-t2d"><b>diet-exercise-rct-t2d</b></a><br>
Bayesian analysis of a diet and exercise trial in type 2 diabetes, with the causal structure written as an explicit DAG and a simulated data-generating process for anthropometric outcomes.<br><br>
<sub><code>Bayesian</code> <code>Causal Inference</code> <code>DAGs</code> <code>Stan</code> <code>R</code> <code>targets</code></sub>
</td>
<td width="50%" valign="top">
<a href="https://github.com/mlatinov/emf-maize-bayes"><b>emf-maize-bayes</b></a><br>
Hierarchical Bayesian modeling of maize growth and physiology under 868 MHz electromagnetic field exposure, spanning Gompertz growth curves, cell-means models, JIP-test photosynthesis parameters and biochemistry endpoints.<br><br>
<sub><code>Hierarchical Bayes</code> <code>Gompertz Growth</code> <code>Stan</code> <code>R</code></sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/mlatinov/University-Biomembranes-"><b>University-Biomembranes-</b></a><br>
Bayesian analysis of electroinduced erythrocyte lysis, running from Stan models through a reproducible pipeline to a LaTeX write-up.<br><br>
<sub><code>Bayesian</code> <code>Biophysics</code> <code>Stan</code> <code>R</code> <code>targets</code></sub>
</td>
<td width="50%" valign="top">
<a href="https://github.com/mlatinov/bayesian-viral-infectivity"><b>bayesian-viral-infectivity</b></a><br>
Bayesian estimation of the probability that a cell becomes infected, across a dilution series.<br><br>
<sub><code>Bayesian</code> <code>Dilution Series</code> <code>Virology</code> <code>R</code></sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/mlatinov/Bayes-Langmuir-Vs-Classical-Langmuir"><b>Bayes-Langmuir-Vs-Classical-Langmuir</b></a><br>
Bayesian nonlinear regression for thermodynamic parameters from Langmuir monolayer compression isotherms, set against the classical fitting approach.<br><br>
<sub><code>Nonlinear Regression</code> <code>Thermodynamics</code> <code>Bayesian</code> <code>Stan</code></sub>
</td>
<td width="50%" valign="top">
</td>
</tr>
</table>

---

## Business Cases

<table>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/mlatinov/airbnb-listings-"><b>airbnb-listings-</b></a><br>
Hierarchical Bayesian price modeling for Airbnb listings, with simulation-based checks and a <code>targets</code> pipeline that can execute remotely on AWS.<br><br>
<sub><code>Hierarchical Bayes</code> <code>Stan</code> <code>R</code> <code>targets</code> <code>AWS</code></sub>
</td>
<td width="50%" valign="top">
</td>
</tr>
</table>

---

## Laplace

<table>
<tr>
<td width="170" align="center" valign="middle">
<img src="assets/laplace.png" alt="Laplace" width="150">
</td>
<td valign="middle">
<b>Laplace</b> is a source-to-source preprocessor for <a href="https://mc-stan.org/">Stan</a>. It compiles <code>.laplace</code> files down to plain, readable <code>.stan</code> files, adding a package manager and namespaced <code>pkg::func()</code> imports to a language that has neither natively.<br><br>
It never becomes a runtime dependency: once <code>build/model.stan</code> exists, it can be handed to <code>stanc</code> or CmdStan with Laplace uninstalled.
</td>
</tr>
</table>

### Laplace Language

<table>
<tr>
<td valign="top">
<a href="https://github.com/mlatinov/laplace"><b>laplace</b></a><br>
The compiler and package manager. Resolves and installs dependencies, builds <code>.laplace</code> sources into committable <code>.stan</code> files, and optionally validates them against <code>stanc</code>.<br><br>
<sub><code>Rust</code> <code>Stan</code> <code>Compilers</code> <code>Package Management</code></sub>
</td>
</tr>
</table>

### Laplace Ecosystem

<table>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/mlatinov/laplace_tools"><b>laplace-tools</b></a><br>
Editor tooling — a language server plus a VS Code extension giving block-role and function-origin coloring, autocomplete across imported libraries, and live diagnostics for unresolved imports and stale version pins.<br><br>
<sub><code>Language Server</code> <code>Rust</code> <code>TypeScript</code> <code>VS Code</code></sub>
</td>
<td width="50%" valign="top">
<a href="https://github.com/mlatinov/laplace-transform"><b>transformation</b></a><br>
A Laplace package of data transformation functions for Stan: centering, scaling and standardization, Box-Cox and Yeo-Johnson, rank and quantile transforms.<br><br>
<sub><code>Laplace Package</code> <code>Stan</code> <code>Transformations</code></sub>
</td>
</tr>
</table>

---

## Software &amp; R Libraries

<table>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/mlatinov/bsst"><b>bsst</b></a><br>
Bayesian Simulation-based Severe Testing — an R package for validating Stan models through parameter recovery experiments, built to locate the sample sizes, effect sizes and designs where inference quietly breaks down.<br><br>
<sub><code>R</code> <code>Stan</code> <code>Parameter Recovery</code> <code>Model Validation</code></sub>
</td>
<td width="50%" valign="top">
<a href="https://github.com/mlatinov/rsims"><b>rsims</b></a><br>
An R package for simulating statistical datasets: hierarchical and crossed designs, random and correlated effects, splines, CFA/SEM helpers and state-space processes.<br><br>
<sub><code>R</code> <code>Simulation</code> <code>Hierarchical Data</code> <code>State-Space</code></sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/mlatinov/tidycausality"><b>tidycausality</b></a><br>
Meta machine-learning algorithms for causal inference in R — S-, T-, X- and R-learners built on the tidymodels framework.<br><br>
<sub><code>R</code> <code>Causal Inference</code> <code>Meta-Learners</code> <code>tidymodels</code></sub>
</td>
<td width="50%" valign="top">
<a href="https://github.com/mlatinov/stanviz"><b>stanviz</b></a><br>
Reusable ggplot2-based plotting functions for fitted Stan models.<br><br>
<sub><code>R</code> <code>Stan</code> <code>ggplot2</code> <code>Visualization</code></sub>
</td>
</tr>
<tr>
<td width="50%" valign="top">
<a href="https://github.com/mlatinov/qcflowr"><b>qcflowr</b></a><br>
An RNA-seq workflow from raw FASTQ to gene counts, automating quality control, trimming, alignment and quantification with FastQC, fastp, HISAT2 and featureCounts.<br><br>
<sub><code>Shell</code> <code>RNA-seq</code> <code>Bioinformatics</code> <code>Pipelines</code></sub>
</td>
<td width="50%" valign="top">
</td>
</tr>
</table>

---

## Skills &amp; Tools

### Statistical Modeling

Bayesian inference &middot; hierarchical and multilevel models &middot; causal inference &middot; nonlinear and mechanistic models &middot; state-space and time series &middot; spatial modeling &middot; simulation-based validation and parameter recovery &middot; probabilistic programming &middot; supervised learning and model explainability

### Languages

R ; Stan ; Julia ; Python : Shell / Bash ; SQL ; LaTeX

### Bioinformatics

FastQC &middot; fastp &middot; HISAT2 &middot; featureCounts

---

**Contact** — [metodilatinov@abv.bg](mailto:metodilatinov@abv.bg)
