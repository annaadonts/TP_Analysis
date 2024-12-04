# TP Analysis: Swing Size and Take Profit Recommendations

## Objective
This project analyzes swing size distributions to recommend a statistically meaningful placement for Take Profit (TP) levels. The goal is to optimize the TP range for better alignment with typical price movement patterns, thus improving the strategy's performance. By doing so, the strategy will be more realistic, avoiding overfitting to outliers and ensuring better risk/reward balance.

## Findings
- The current TP level is outside the swing size range observed in the dataset, suggesting potential overfitting or an unrealistic strategy.
- The proposed TP range of **15-20 pips** aligns with the observed swing distribution from the dataset, balancing risk and reward and better reflecting typical market behavior.

## Visualization
![Proposed TP Range](images/TP_plot.png)

## Files
- **analysis.ipynb**: Full analysis and visualizations.
- **TP_plot.png**: Visualization of the proposed TP range (embedded in the README).
- **README.md**: Overview of the TP analysis.

## Response to Screening Question

### 1. Marking the TP Adjustment on the Plot
I’ve analyzed the distribution of swing distances and marked a proposed Take Profit (TP) range of 15-20 pips on the plot (indicated by the red shaded region). This adjustment brings the TP closer to the realistic swing behavior observed in the dataset.

### 2. Logical Basis for the Adjustment
The logical reasoning for the new TP placement is based on the following:

#### Statistical Alignment with Swing Distribution:
- The current TP (mean = 33.40 pips) is far outside the observed swing size distribution (mean = 5.74 pips, median = 4.70 pips, std = 4.41 pips).
- Most swings occur within 5-10 pips, and values beyond 15-20 pips represent the broader tail of the distribution, which aligns with typical price behavior without relying on extreme outliers.
- The proposed range (15-20 pips) lies just beyond two standard deviations from the mean (approximately 14.56 pips), ensuring it reflects meaningful, yet less frequent, price movements.

#### Avoiding Overfitting:
- The current TP placement (33.40 pips) suggests potential overfitting to the small dataset, as it lies outside the meaningful range of swing distances.
- By aligning the TP with the broader tail of the swing distribution, the new placement avoids overfitting and represents a more realistic target for future price movements.

#### Strategy Effectiveness:
- A TP that is too far from typical swing distances (like the current TP) risks being ineffective, as it is unlikely to be reached under normal market conditions.
- The proposed TP (15-20 pips) ensures the strategy remains realistic, balancing risk and reward while reflecting actual market behavior.

## Addressing Concerns

### TP is completely out of swing size range
- The current TP is indeed far from the observed swing distribution. The proposed adjustment (15-20 pips) aligns the TP with realistic swing distances, validating its placement using the dataset’s distribution.

### Overfitting of optimization
- The current TP may have resulted from overfitting, where the optimization algorithm placed the TP to maximize performance on this specific dataset.
- The adjusted TP avoids overfitting by reflecting broader market behavior, as indicated by the swing distance distribution.

### Strategy may be more effective without TP
- A far-off TP reduces strategy effectiveness. The adjusted TP ensures it complements the strategy by staying close to realistic price swings, ensuring it is both achievable and meaningful.

## Validation Using Swing Distances
The swing distances (measuring high to low) exhibit a regular distribution, with most swings occurring between 5-10 pips. The proposed TP range of 15-20 pips lies within the broader tail of this distribution, ensuring it avoids outliers while reflecting realistic market behavior.

## Conclusion
The proposed TP range of 15-20 pips is a realistic and statistically supported adjustment, ensuring better alignment with typical market swings. This change is expected to improve strategy effectiveness and avoid overfitting to outliers, leading to more consistent and achievable results.
