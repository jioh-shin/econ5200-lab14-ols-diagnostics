# OLS Diagnostics: Robust and Clustered Standard Errors

## Objective
I examined how different standard error methods affect confidence interval coverage in OLS regression and used diagnostic measures to identify influential observations.

## Methodology
- Simulated OLS regressions with heteroskedastic errors and errors shared within 40 firms.
- Compared the coverage rates of nominal 95% confidence intervals using classical, HC3, and firm-clustered standard errors.
- Used leverage, studentised residuals, and Cook's distance to identify three planted influential observations.
- Examined how influential observations affected the estimated regression slope.
- Wrote my own AI prompt to generate a standard error comparison table.
- Completed 1 round of prompting and checked all 18 values against statsmodels, including a test with renamed columns.

## Key Findings
- **Heteroskedasticity:** Classical standard errors produced 92.4% coverage, while HC3 improved coverage to 94.4%, closer to the nominal 95%.
- **Within-firm correlation:** HC3 produced only 50.3% coverage when errors were shared within firms. Clustering by firm increased coverage to 93.7%.
- **Influential observations:** I identified all three planted observations using regression diagnostics. Removing one influential observation changed the estimated slope from 1.4927 to 1.4468.
- **AI validation:** All 18 values generated through my AI-assisted workflow matched statsmodels, including the renamed-column test.

## Conclusion
I found that choosing the appropriate standard error method matters for reliable statistical inference. HC3 improved coverage under heteroskedasticity, but firm-clustered standard errors were necessary when errors were correlated within firms. I also learned how influential observations can affect coefficient estimates and how to validate AI-generated results against established statistical tools.
