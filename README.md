# Why Young Men Turn to the Far Right

**The effects of gendered economic attitudes on far-right voting in Europe**

A cross-national individual-level analysis testing whether perceived economic costs of gender equality help explain far-right voting among young European men. Uses the new gender attitudes module fielded for the first time in ESS Round 11.

Term paper for module 15081, *The Political Economy of Gender Inequality* (Dr. Paula Zuluaga Borrero), Geschwister Scholl Institute of Political Science, LMU Munich. Submitted 9 March 2026.

---

## Summary

**Question.** To what extent is young European men's voting for far-right parties driven by perceived economic costs of gender equality?

**Motivation.** A gender gap in far-right support has opened among Europe's youngest voters that has no equivalent in older cohorts — a generational rather than life-cycle phenomenon. The drivers of this divergence remain underexplored, particularly its economic dimension. ESS Round 11 (2023/24) fielded a dedicated gender attitudes module for the first time, including items on perceptions of gender relations in the labour market, which had not previously been used in the far-right voting literature.

**Theory.** The paper builds on Iversen and Rosenbluth's (2010) political economy of gender inequality, in which policies expanding women's labour market opportunities improve women's household bargaining power while being financed partly through taxation of male breadwinners. Extending this logic to a phenomenon the original authors did not address, the paper argues that young men who perceive themselves as bearing the economic costs of that shift — especially under labour-market precarity — may become receptive to parties framing gender equality as a threat to men's prospects.

### Hypotheses

- **H1** — Among young men in European democracies, opposition to gender equality economic policies is positively associated with far-right voting, net of established individual-level predictors.
- **H2** — Economic gender attitudes retain a significant association with far-right voting after controlling for anti-immigration attitudes.
- **H3** — Economic gender attitudes have explanatory power independent of hostile sexism when both enter the same model.

### Data and measures

**Source.** European Social Survey Round 11 (2023/24), integrated file **`ESS11e04_1`**. The sample is restricted to male respondents aged 18–34 in European democracies where far-right parties contested elections. Hungary is excluded on the grounds of democratic backsliding (Freedom House "Partly Free"). Great Britain and Lithuania are dropped because no young male respondent reported a far-right vote. Final analytic sample: **N = 1,486 across 23 countries**, of whom 238 reported voting for a far-right party.

**Dependent variable.** Binary indicator of far-right vote, coded using the PopuList dataset and verified against additional sources for party renamings, ideological shifts, and newly emerged parties. Where multiple vote types were recorded (e.g. Germany), only party-list votes are used. The full country-by-party coding scheme is in the paper's appendix.

**Key independent variables.**

| Index | Items | Construction |
|---|---|---|
| Gendered economic attitudes | `eqpaybg`, `eqmgmbg` (perceived economic impact of equal pay and equal representation in management), `fineqpy`, `eqparlv` (support for fines on gender pay gaps and for equal parental leave) | Items on different scales (0–6 and 1–5); `eqpaybg` and `eqmgmbg` reverse-coded, then all items z-standardised individually before averaging so higher values consistently indicate greater opposition |
| Hostile sexism | `wsekpwr`, `weasoff`, `wexashr` | 5-point items, z-standardised and averaged |
| Anti-immigration attitudes | Composite | Item-level standardisation, then averaged |
| Political trust | Trust in political institutions | Averaged; no standardisation, as all items share a scale |

**Estimation.** Logistic regression with country fixed effects, absorbing all observed and unobserved between-country heterogeneity, with standard errors clustered at the country level. Four nested specifications: baseline controls only; baseline plus hostile sexism; baseline plus economic gender attitudes; and both indices jointly.

### Findings

| | Baseline | + HS | + EGA | Full |
|---|---|---|---|---|
| Hostile sexism | | 0.103 (0.115) | | 0.083 (0.126) |
| Economic gender attitudes | | | 0.111 (0.089) | 0.098 (0.096) |
| Anti-immigration | 1.204\*\*\* (0.150) | 1.178\*\*\* (0.152) | 1.173\*\*\* (0.154) | 1.156\*\*\* (0.155) |
| Education | −0.122\* (0.063) | −0.116\* (0.062) | −0.123\* (0.064) | −0.119\* (0.063) |
| Urban | −0.483\*\*\* (0.171) | −0.479\*\*\* (0.170) | −0.478\*\*\* (0.175) | −0.476\*\*\* (0.174) |
| Pseudo R² | 0.254 | 0.254 | 0.255 | 0.255 |

*N = 1,486 in all models. Country FE and clustered SEs throughout. Political trust, income, employment, age and religiosity included but not significant. \*\*\* p < 0.01, \*\* p < 0.05, \* p < 0.10.*

**None of the three hypotheses is supported in its strong form.** Anti-immigration attitudes are by far the strongest and most consistent predictor across every specification. Neither hostile sexism nor economic gender attitudes reaches conventional significance once standard controls and country fixed effects are included, though both coefficients remain positive and therefore directionally consistent with theory. Diagnostics show no multicollinearity problem (all VIFs below 1.5), so the null result is not an artefact of the attitudinal indices competing for variance.

**Interpretation.** The result suggests that gendered economic perceptions, as operationalised here, do not independently explain far-right voting among young European men when pooled cross-nationally. This does not invalidate the mechanism outright: the relationship may be context-dependent, and social desirability may suppress honest reporting of gender attitudes in countries where support for gender equality is normatively expected. The paper argues the more promising next step is testing country-level structural conditions related to the decline of male economic privilege, and examining propensity to vote far-right and policy-position alignment rather than reported vote alone.

### Limitations

Cross-sectional data cannot support causal claims. The gendered economic attitudes index has Cronbach's α below 0.70, indicating only modest internal consistency and imperfect measurement of the underlying construct — the other indices exceed 0.70. Most fundamentally, the theorised mechanism is structural while the analysis relies on individual-level attitudinal proxies; the paper does not claim to identify structural effects.

---

## Repository contents

| File | Description |
|---|---|
| `Why_Young_Men_Turn_to_the_Far_Right.pdf` | Full paper, including country-by-party far-right coding scheme in the appendix |
| `Young_males_voting_for_the_far_right.ipynb` | Data subsetting, variable construction, index standardisation, reliability and multicollinearity diagnostics, and estimation of all four models |

## Data availability

The analysis uses ESS Round 11 integrated file, edition `ESS11e04_1`. The raw ESS file is **not** redistributed here. It can be downloaded free of charge from the [ESS Data Portal](https://ess.sikt.no/) after registering an account. Place the downloaded file in the repository root and run the script to reproduce the analytic dataset.

Far-right party classification draws on [The PopuList](https://popu-list.org/), supplemented by manual verification.

## Author

Iuliia Peskisheva — MA Social Sciences, LMU Munich
