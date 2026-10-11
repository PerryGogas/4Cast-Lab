# 4Cast Lab

**Train · Test · Forecast**: a free, open-source app for machine learning, econometrics and statistical analysis.

[![Latest release](https://img.shields.io/github/v/release/PerryGogas/4Cast-Lab?label=latest%20release)](https://github.com/PerryGogas/4Cast-Lab/releases/latest)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.22818865.svg)](https://doi.org/10.5281/zenodo.22818865)
[![SSRN](https://img.shields.io/badge/SSRN-7552460-blue)](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=7552460)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

4Cast Lab lets you build, test and document predictive and statistical models **without writing code**. It is for researchers, analysts, instructors and students in any field. The defaults follow the forecasting literature: time-ordered splits, benchmarks against naive forecasts and tests of predictive accuracy. If you follow them, your results should survive a referee's first questions.

- **Nothing to install.** Download and double-click.
- **Your data stay on your computer.** All computation is local, so you can use confidential, proprietary or licensed data. The only connections are the update check (GitHub) and, if you choose to use it, the optional AI interpretation (sent to the AI provider you select).
- **Reproducible.** Every run records its settings and can be saved as a session file. It produces a Methods Report for your paper and can be exported as a Python (pandas / scikit-learn) script.

Developed by **Professor Periklis Gogas**, E|M|E|F Lab, Department of Economics, Democritus University of Thrace.

---

## 1. Download and install (Windows)

1. Go to the **[latest release](https://github.com/PerryGogas/4Cast-Lab/releases/latest)** and download `4Cast.Lab.exe` from **Assets**.
2. Put it in any folder, for example `Documents\4Cast Lab`. You don't need administrator rights.
3. Double-click `4Cast.Lab.exe`.

**"Windows protected your PC"?** The app is not code-signed, so Windows SmartScreen may warn you the first time. Click **More info → Run anyway**. You only need to do this once.

**Check your download (optional).** Each release lists the file's SHA-256 checksum. To compare, open PowerShell in the download folder and run:

```powershell
Get-FileHash .\4Cast.Lab.exe -Algorithm SHA256
```

The value must match the one in the release notes. If it doesn't, delete the file and download it again from the release page only.

**Requirements:** Windows 10 or 11 with Microsoft Edge WebView2. WebView2 is already part of Windows 11 and up-to-date Windows 10. If the app opens a blank window, install the free [WebView2 Runtime](https://developer.microsoft.com/microsoft-edge/webview2/).

**Updating:** download the new `4Cast.Lab.exe` and replace the old one. Your saved sessions (`.4cl` files) keep working.

---

## 2. Quick start: videos (about 3 minutes each)

▶ **[4Cast Lab Quick Start playlist on YouTube](https://www.youtube.com/playlist?list=PLfIotCXrK6uc)**

| Part | What you learn |
|---|---|
| [**A · Machine learning**](https://www.youtube.com/watch?v=_edtfsVPS-E&list=PLfIotCXrK6uc) | Load data, choose the target and predictors, train and tune a model, read the results honestly, compare all models, see what drives the predictions, forecast new cases and export a Methods Report. |
| [**B · Econometrics**](https://www.youtube.com/watch?v=rK692DtkxMc&list=PLfIotCXrK6uc) | OLS with robust standard errors, coefficients and diagnostics, a journal-style results table (LaTeX, Word, Excel), and an ARIMA forecast. |

Inside the app, every setting and result has a **?** icon with a short explanation, and the **Glossary** tab defines every metric and test. Start in the **Core** view, which shows the essentials. Switch to **Expert** for the full set of options.

---

## 3. What 4Cast Lab does

**Forecasting (machine learning) mode**

- **Data:** CSV and Excel import, or built-in example datasets (macroeconomic monthly series, a wage cross-section, credit data). It checks for gaps, duplicates, possible target leakage and multicollinearity, and supports panel data.
- **Validation without leakage:** time-series splits with an embargo, purged cross-validation, and random splits for cross-sections.
- **Learners:** OLS, ridge, LASSO, elastic net, logistic regression, k-nearest neighbours, decision tree, random forest, gradient boosting, stacking, support vector machines and neural network. Train one, or all at once with **Train All & Compare**.
- **Tuning:** hyperparameters are tuned by cross-validation, with optional nested cross-validation and variable selection.
- **Evaluation:**
  - RMSE, MAE, MAPE, sMAPE, R², MASE and conformal prediction intervals.
  - For classification: ROC, calibration, class-imbalance handling and cost-based thresholds.
  - Every model is compared with a naive benchmark (random walk or training mean) using Diebold–Mariano, Clark–West and Pesaran–Timmermann tests.
- **Interpretation:** permutation importance, SHAP values and partial-dependence plots.
- **Reports:** a Methods Report written for the Methods section of a thesis or paper, a Full Report, and a Python export.
- **Optional AI interpretation** of the results, with the provider of your choice (ChatGPT, Gemini, Copilot, Grok or Claude) and your own API key.

**Estimation (econometrics) mode**

OLS with robust, HAC and clustered standard errors · logit and probit · IV/2SLS · ARIMA/SARIMA · ARDL with the bounds test · error-correction models · VAR and VECM · GARCH · diagnostic, specification and structural-break tests · journal-style results tables exported to LaTeX, Word and Excel.

**Checked against standard software.** Estimators and tests are checked against statsmodels, linearmodels, arch, scikit-learn, SciPy and NIST certified results on standard public datasets.

---

## 4. Limitations

- 4Cast Lab suits datasets of thousands to tens of thousands of rows, not big data. Tuning all learners on 1,000 rows takes about two minutes.
- Random forest, gradient boosting and the neural network agree with scikit-learn only approximately, because their solvers and random-number streams differ.
- Classification is currently binary.
- Predictive-accuracy tests are applied to the validation sample only.

---

## 5. How to cite

If you use 4Cast Lab in a thesis, dissertation, paper, report or course, please cite **both the software and the paper**.

**Software.** This DOI always points to the latest version. Write the version you used.

> Gogas, P. (2026). *4Cast Lab: Open-source app for machine learning and statistical analyses* (Version 4.6.2) [Computer software]. E|M|E|F Lab, Democritus University of Thrace. https://doi.org/10.5281/zenodo.22818865

**Paper**

> Gogas, P. (2026). *4Cast Lab: Open-Source App for Machine Learning & Statistical Analysis*. SSRN. https://papers.ssrn.com/sol3/papers.cfm?abstract_id=7552460

**BibTeX**

```bibtex
@software{Gogas_4CastLab_2026,
  author    = {Gogas, Periklis},
  title     = {{4Cast Lab}: Open-source app for machine learning and statistical analyses},
  year      = {2026},
  version   = {4.6.2},
  publisher = {E|M|E|F Lab, Democritus University of Thrace},
  doi       = {10.5281/zenodo.22818865},
  url       = {https://doi.org/10.5281/zenodo.22818865}
}

@misc{Gogas_4CastLab_SSRN_2026,
  author       = {Gogas, Periklis},
  title        = {{4Cast Lab}: Open-Source App for Machine Learning \& Statistical Analysis},
  year         = {2026},
  month        = oct,
  howpublished = {SSRN},
  note         = {Abstract ID 7552460},
  url          = {https://papers.ssrn.com/sol3/papers.cfm?abstract_id=7552460}
}
```

GitHub can also generate the software citation for you: click **Cite this repository** in the right-hand panel.

---

## 6. Questions, suggestions, problems

- **Comments, suggestions, corrections:** [Contact form](https://forms.gle/YjA7dgeqonm9qvcS7)
- **Report a problem:** [GitHub Issues](https://github.com/PerryGogas/4Cast-Lab/issues). Please include the version (shown in the About window), what you did, and a screenshot if you can.
- **Email:** perrygogas+4castlab@gmail.com

---

## 7. License and acknowledgements

4Cast Lab is free software under the [MIT License](LICENSE). © 2026 Periklis Gogas.

Thanks to the doctoral students of the E|M|E|F Lab, who tested successive versions on their own datasets. Their reports led to many corrections.

The Windows app is built with [WebExeBuilder](https://webexebuilder.com/) by [ezWareLab](https://ezwarelab.com/).
