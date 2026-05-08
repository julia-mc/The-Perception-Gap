## Exploratory Data Analysis Summary

* Joined the dispatch dataset with the crime dataset using the crime report number to compare reported incidents with confirmed outcomes
* Removed duplicate crime records by keeping only the highest severity offense per report
* Created variables to measure the perception gap, including whether a call resulted in a crime report and whether the severity matched
* Built a severity ranking system (0–3 scale) for dispatch types and crime classifications
* Identified service and non-criminal calls that do not correspond to actual crimes
* Aggregated the data by district and month to analyze trends over time
* Created visualizations to explore how the perception gap varies across districts and categories

### Key Variables

* **no_crime_report**: Indicates whether a dispatch call resulted in a confirmed crime report
* **severity_shift**:

  * Severity Match: perception was correct
  * Severity Downgraded : reported as more severe than actual (Overestimate)
  * Severity Upgraded: reported as less severe than actual (Underestimate)
  * No Report: no official crime report generated
* **gap_type**:

  * No Report
  * Service / Non-Criminal
  * Severity Downgraded
  * Severity Upgraded
  * Match
* **perception_gap_binary**: Classifies calls as Gap or Accurate
* **service_category**: Identifies whether a call is service related or crime related

### Key Findings

* Most dispatch calls do not result in a confirmed crime report.
* The perception gap is mainly driven by the large number of **No Report** and **Service / Non Criminal** calls.
* Misclassification (overestimation and underestimation) plays a smaller role in the overall gap.
* When a crime is confirmed, the reported severity is usually upgraded.
* The perception gap is consistently high across districts.

### Interpretation

The perception gap reflects differences between how the public interprets situations and how incidents are officially classified.

The high number of non crime and service related calls suggests that many reported situations do not meet the legal definition of a crime, even if they appear suspicious or concerning to the caller.

### Limitations

* The severity classification is based on keyword rules, which may not capture all situations perfectly
* Some cases remain unclassified due to missing or unclear information
* This analysis is exploratory and does not establish causation
