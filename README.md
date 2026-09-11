# HealthConnect Clinic – Week 6 Analysis

## AnalystLab Africa | Data Analytics Internship (Batch D)

This repository contains my Week 6 submission for the AnalystLab Africa Experience Lab, continuing the HealthConnect Clinic project: *Improving Patient Appointment Attendance and Healthcare Support Using Data and AI*.

## Project Background

Week 6 moves the HealthConnect project from initial implementation (Week 5) into **Integration → Advanced Development → Validation**. Rather than repeating the Week 5 EDA, this week deepens the strongest Week 5 findings and formally integrates them with another project track.

## Week 6 Focus (Data Analytics Track)

- Validated whether the two strongest Week 5 predictors (booking lead time and previous no-show history) compound when combined
- Built a new combined-risk visualisation in Power BI (added as a new page to the existing Week 5 file, not a rebuild)
- Refined Week 5 recommendations into a single combined risk score
- Completed and documented a verified cross-track integration with the Project Management track
- Updated assumptions, limitations, risks, and dependencies

## Files in This Repository

| File | Description |
|---|---|
| `HealthConnect_Week6_Analysis.docx` | Full Week 6 write-up: Week 5→6 transition, combined risk analysis, refined recommendations, cross-track integration evidence, updated limitations, and project summary |
| `HealthConnect_Week5_Analysis.pbix` | Power BI file, updated with a new "Week 6 - Combined Risk" page in addition to the original Week 5 KPI visuals |
| PM integration conversation screenshot | Evidence of the Data Analytics → Project Management exchange |

## Key Finding: Compounding Risk

Booking lead time and previous no-show history do not act independently — they compound:

| Lead Time | No-Show History | No-Show Rate |
|---|---|---|
| 31+ days | High (2+ prior no-shows) | **73%** |
| 31+ days | Low (0-1 prior no-shows) | 59% |
| 8-30 days | High (2+ prior no-shows) | 55% |
| 8-30 days | Low (0-1 prior no-shows) | 38% |
| 0-7 days | High (2+ prior no-shows) | 44% |
| 0-7 days | Low (0-1 prior no-shows) | **26%** |

Best case (26%) to worst case (73%) represents nearly a 3x difference in no-show risk.

## Cross-Track Integration

**Data Analytics → Project Management**: Week 5 findings (KPI results, priority variables, data limitations, Week 7 testing considerations) were shared with the Project Management track. This integration is formally documented in the PM track's Week 6 records:
- Integration Register: DINT-006 (Status: Active - Informed)
- Cross-Track Coordination: CTR-001 (Status: Completed)
- Decision Log: DEC-006
- Integration Issue Log: ISS-003 (Status: Resolved - Analytics Integration Completed)
- Updated Risk Register: R011, R012

## Refined Recommendations

1. Introduce a combined risk score (lead time × no-show history) rather than two separate flags
2. Reserve lightest-touch reminders for the lowest-risk group (short lead time, clean history)
3. Apply moderate reminder intensity to single-risk-factor segments
4. Deprioritise appointment type in intervention design — it showed minimal predictive value, independently and combined

## Next Steps (Week 7)

Calculate the remaining appointment-time-slot KPI, and test whether the combined risk pattern holds consistently across patient demographic segments (age group, gender).

## Author

Ofentse Lebethe — Data Analytics Intern, AnalystLab Africa (Batch D)
