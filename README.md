# Stream Analysis  - Project 7

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/FeMaspe02/AlgorithmsProject_MasperoFederico/blob/main/NOTEBOOK_FILENAME.ipynb)

Final project for the Algorithms for Massive Datasets course at the University of Milan, held by Professor Dario Malchiodi.

## Overview

This project implements and evaluates three stream analysis algorithms from scratch, applied to the New York Times Articles & Comments (2020) dataset, treated as a data stream:

- **Bloom filter** — membership testing on article IDs
- **Flajolet–Martin** — estimating the number of distinct users
- **Alon–Matias–Szegedy (AMS)** — estimating the second moment over article sections

Reservoir sampling is also implemented as part of the AMS algorithm. Each algorithm is validated against exact ground truths, and the project demonstrates that these methods achieve good accuracy while using memory bounded independently of the stream size.

The full analysis and results are presented in the project report (`report.pdf`).

## Repository structure

- `stream_analysis.ipynb` — Jupyter notebook containing the full implementation and experiments
- `Final Project Report - Maspero Federico.pdf` — Project report with methodology, results and conclusions
- `README.md` — This file

## Requirements

- Python 3.x
- `kaggle` (for downloading the dataset)
- `matplotlib`

The notebook installs the `kaggle` package automatically when run.

## Dataset access

The notebook downloads the dataset dynamically from Kaggle at runtime; it is not stored in this repository. To allow the download, Kaggle API credentials must be provided:

- **On Google Colab:** add your Kaggle credentials as secrets via the Secrets panel (🔑 icon in the left sidebar), named `KAGGLE_USERNAME` and `KAGGLE_KEY`, with notebook access enabled.
- **Locally:** place your `kaggle.json` file in `~/.kaggle/kaggle.json`.

Kaggle credentials can be generated from your Kaggle account under Settings → API → Create New Token.

## How to run

Open the notebook in Google Colab using the badge above (or run it locally in Jupyter). Set up the Kaggle credentials as described, then run the cells in order. By default the notebook processes a subsample of the data for a reasonable execution time; the full dataset can be processed by setting the `SUBSAMPLE` flag to `False`. The random seed used in the experiments ensures that the results are reproducible.

## Author

Federico Maspero — Department of Computer Science, University of Milan
