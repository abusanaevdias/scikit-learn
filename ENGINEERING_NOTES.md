# scikit-learn — engineering notes

ML baselines · Source review: 6 November 2026

## Purpose

A candidate for an interpretable baseline before adding an LLM to a classification or ranking problem.

## Architecture reviewed

Scientific Python estimators, examples, benchmarks and tests live in a mature library with a BSD 3-Clause license.

Repository areas inspected: `sklearn, examples, benchmarks, pyproject.toml` (root inventory and linked README documentation).

## Decision and trade-off

Avoid data leakage: preprocessing and feature selection must be learned on training folds, not on the whole dataset.

## Verification to perform

Keep a held-out set; compare a dummy baseline; record the split seed and per-class metrics.

This is a source review and a proposed verification plan. No upstream runtime suite, deployment, provider benchmark or paid API evaluation was run for these notes.

## Attribution and scope

- Original project: [scikit-learn/scikit-learn](https://github.com/scikit-learn/scikit-learn).
- Original license: BSD-3-Clause; retained without replacement.
- Original README and source history remain part of the fork.
- This portfolio layer adds documentation; it does not claim authorship of the upstream project or an accepted upstream contribution.
- Dependency licenses, model weights, hosted services and any existing NOTICE files remain subject to their own terms.

## Start from the maintained instructions

Read the [upstream README](https://github.com/scikit-learn/scikit-learn/blob/main/README.rst) and its contribution guidance for current installation and development commands.
