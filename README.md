# Chess Openings Statistical Analysis

Statistical analysis of 19,629 Lichess games across 316 chess opening families, 
using Bühlmann credibility weighting, Wald confidence intervals, and chi-square 
testing to identify openings with a statistically significant performance edge — 
visualized in an interactive Tableau Public dashboard.

## Methodology
1. Cleaned and classified 1,477 unique openings into 316 opening families using XLOOKUP
2.Applied Bühlmann credibility weighting (k=10) to smooth win-rate estimates across 
  varying sample sizes, reducing noise from small-sample openings
3.Calculated 99% Wald confidence intervals for each opening family's win rate
4.Ran a chi-square test to confirm differences across opening families were 
  statistically significant overall (χ² p ≈ 4.04×10⁻³²)

## Key Findings
Across all 316 opening families, 8 showed a statistically significant advantage 
for White and 3 for Black, at ≥50 games and 99% Wald confidence.

White-significant (8 families):
| Opening | Games | White Win Rate |
|---|---|---|
| Philidor Defense | 671 | 57.2% |
| Australian Defense | 611 | 55.3% |
| Barnes Defense | 606 | 59.6% |
| Elephant Gambit | 439 | 59.5% |
| Queen's Gambit | 168 | 63.7% |
| Bishop's Opening: Berlin Defense | 111 | 62.2% |
| King's Gambit Accepted: Becker Defense | 74 | 66.2% |
| Ruy Lopez: Bird's Defense Deferred | 67 | 67.2% |

Black-significant (3 families):
| Opening | Games | Black Win Rate |
|---|---|---|
| Amar Opening | 992 | 56.7% |
| Sicilian Defense | 783 | 54.7% |
| Center Game: Berger Variation | 77 | 66.2% |

## Dashboard
Live interactive dashboard on Tableau Public: http://public.tableau.com/app/profile/rajnish.giri8158/viz/shared/36XXK8576

## Tools
Excel, Tableau Public

## Files
- `ChessOpeningsAnalysis.xlsx` — full workbook with raw data, credibility 
  weighting calculations, Wald CI formulas, and chi-square testing
