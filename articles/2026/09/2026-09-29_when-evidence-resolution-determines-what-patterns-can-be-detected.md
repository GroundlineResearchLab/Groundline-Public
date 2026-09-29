# When Evidence Resolution Determines What Patterns Can Be Detected

**Date:** 29 September 2026  

**Domain:** Evidence Resolution and Pattern Detection  

**Publication Type:** Article

## Context

Evidence can be accurate, relevant, properly sourced, and still be unable to reveal the pattern a researcher is trying to detect.

A monthly average may accurately describe average conditions during a month while concealing a disruption that lasted two hours.

A national statistic may accurately describe a country while concealing strong variation between neighboring areas.

An instrument may consistently report measurements while being unable to distinguish changes smaller than its measurement resolution.

A dataset may correctly report broad economic sectors while lacking enough categorical detail to reveal changes occurring inside those sectors.

In each case, the problem is not necessarily that the evidence is wrong.

The evidence may be too coarse for the question.

Resolution concerns the scale at which distinctions remain observable.

Depending on the evidence system, that may involve:

- Time.
- Geography.
- Measurement increments.
- Observation frequency.
- Category granularity.
- Reporting level.
- Aggregation.

The research question is therefore:

**How does evidence resolution determine which patterns a dataset is capable of detecting?**

The central distinction is:

`Available Evidence ≠ Sufficient Resolution`

## What the Evidence Shows

Resolution is not one single property.

NIST defines measurement resolution as the ability of a measurement system to detect and faithfully indicate small changes in the characteristic being measured.[1]

A measurement system can therefore produce valid readings while remaining unable to distinguish changes below its effective resolution.

NIST also warns that the number of digits displayed by an instrument does not itself establish measurement resolution.[1]

Temporal evidence presents the same problem differently.

USGS guidance on high-frequency groundwater-quality monitoring states that high-frequency time series can reveal short-term water-quality trends that may not be identifiable through monthly or annual sampling programmes.[3]

Spatial evidence has another form of the same problem.

Research on the modifiable areal unit problem shows that the representation and interpretation of spatial data can change when observations are grouped into geographic units of different sizes, shapes, or configurations.[7]

NASA satellite systems make resolution tradeoffs particularly visible. NASA documentation comparing active-fire products from VIIRS, MODIS, and Landsat shows that systems with finer spatial detail may provide lower temporal coverage, while systems observing the Earth more frequently may do so at coarser spatial resolution.[5]

These examples support a common principle:

**Evidence can reveal only distinctions that survive the scale at which observations are measured, retained, aggregated, and reported.**

## 1. Resolution Determines Whether a Difference Is Observable

Suppose the underlying system contains two values:

`10.1`

and:

`10.2`

If the measurement system can distinguish only increments of one whole unit, both values may appear as:

`10`

The underlying states differ.

The available measurement does not preserve that difference.

NIST's definition of resolution captures precisely this issue: resolution concerns whether the measurement system can detect and faithfully indicate small changes.[1]

This creates a fundamental evidence distinction:

`Underlying Difference ≠ Observable Difference`

A pattern can exist while remaining below the ability of the evidence system to distinguish it.

## 2. Evidence Can Have Several Different Resolutions at Once

A dataset should not necessarily be described simply as "high resolution" or "low resolution."

Resolution can operate across several dimensions.

| Resolution Dimension | What It Affects |
| --- | --- |
| Temporal resolution | How closely events can be distinguished in time |
| Spatial resolution | How closely locations or local variation can be distinguished |
| Measurement resolution | How small a numerical change the measurement system can distinguish |
| Observation frequency | How often observations are generated |
| Category granularity | How finely categorical distinctions remain represented |
| Reporting resolution | How much collected detail survives publication |
| Aggregation level | How many detailed observations are combined into broader units |

These dimensions can differ within the same evidence system.

A dataset may have fine geographic resolution but coarse temporal resolution.

Another may record observations every second but publish only daily averages.

A third may preserve exact numerical measurements internally while releasing only broad categories.

Resolution therefore needs to be interpreted in relation to the particular distinction a claim requires.

## 3. Temporal Resolution Determines Which Events Remain Visible

Suppose electricity demand is measured every minute.

A sudden twenty-minute spike may be directly visible.

If those same observations are reduced to one daily average, the spike may barely affect the published value.

Both representations can be mathematically correct.

They answer different questions.

The minute-level series can address:

`Did a short-duration peak occur?`

The daily average can address:

`What was average demand during the day?`

Using the daily average to conclude that no short peak occurred would require information the daily series no longer preserves.

This is why temporal resolution and the duration of the phenomenon need to be considered together.

## 4. Observation Frequency Is Not Always the Same as Temporal Resolution

Frequent timestamps can create an appearance of high temporal detail.

But a new timestamp does not always represent a fully independent new measurement.

USGS guidance for field fluorescence sensors defines temporal resolution as the amount of time between truly independent measured values.[4]

It notes that sensors can average information over intervals that exceed the nominal reporting interval.[4]

This creates another important distinction:

`Frequent Timestamp ≠ Independent High-Resolution Observation`

A system reporting every second may still contain values influenced by overlapping measurement intervals or internal averaging.

The timestamp alone therefore does not fully describe the temporal resolution of the evidence.

## 5. Short Events Can Occur Between Observations

Suppose an event lasts five minutes.

Measurements are taken once every hour.

The event can begin and end between two observations.

The dataset may contain no record of it.

That produces:

`No Recorded Event`

without necessarily establishing:

`No Event Occurred`

The interpretation depends on whether the observation schedule was capable of capturing a phenomenon of that duration.

USGS makes the same broader point in groundwater monitoring: high-frequency observations can reveal short-term trends that monthly or annual programmes may not detect.[3]

A negative finding therefore needs to remain bounded by the temporal resolution available.

## 6. Temporal Aggregation Can Preserve Quantity While Removing Timing

Consider:

| Hour | Events |
| --- | ---: |
| 08:00 | 5 |
| 09:00 | 50 |
| 10:00 | 5 |
| 11:00 | 5 |

Total activity is:

`65 events`

If only the four-hour total is retained, the evidence correctly preserves total volume.

It no longer shows that most events occurred around 09:00.

Aggregation preserved:

`Quantity`

while removing:

`Timing`

For research concerning total activity, nothing essential may have been lost.

For research concerning short-duration stress or concentration, timing may be the central evidence.

The usefulness of the aggregate therefore depends on the claim.

## 7. Spatial Resolution Determines Which Local Differences Survive

Spatial evidence behaves similarly.

Suppose neighborhood-level pollution measurements reveal one severe local hotspot.

If all neighborhoods are averaged into one city-level statistic, the hotspot may become much less visible.

The city average can be completely correct.

It does not establish that every location experienced the average condition.

The modifiable areal unit problem, or MAUP, describes related effects arising when observations are grouped into spatial units of different sizes, shapes, or arrangements.[7]

Changing the geographic unit can alter mapped patterns and analytical interpretation even though the underlying observations remain the same.

This creates a spatial version of the same evidence boundary:

`No Local Pattern Visible at Coarse Scale ≠ No Local Pattern Exists`

## 8. Geographic Aggregation Changes the Evidence Being Analyzed

Suppose 1,000 detailed spatial observations are aggregated into 20 regions.

The published dataset now contains:

`20 regional summaries`

rather than:

`1,000 local observations`

The original observations may still exist elsewhere.

But if researchers have access only to the regional dataset, local variation can no longer be recovered directly from that evidence.

Aggregation therefore does not merely shorten a table.

It changes the observational unit available for analysis.

That distinction matters whenever a claim concerns a scale smaller than the published geographic unit.

## 9. Spatial Scale Can Change Apparent Statistical Relationships

Geographic resolution can affect more than visible hotspots.

It can also affect measured relationships between variables.

MAUP research demonstrates that changing geographic scale or boundaries can change statistical results produced from spatially aggregated observations.[7]

Local variation can be reduced when observations are averaged into larger geographic units.

Correlations or apparent associations at the regional level may therefore differ from relationships visible at a finer scale.

The regional values are not necessarily false.

The relationship being measured belongs to a different evidence scale.

A statistical association observed at one spatial scale should therefore not automatically be assumed to describe another.

## 10. Remote Sensing Makes Resolution Tradeoffs Explicit

Satellite observation systems routinely document both spatial and temporal resolution because the two affect what can be observed.

NASA's comparison of VIIRS, MODIS, and Landsat active-fire products provides a clear example.[5]

VIIRS and MODIS provide broad, frequent coverage.

Landsat provides much finer spatial detail but observes the same location less frequently.

NASA describes VIIRS active-fire observations at approximately 375 metres and MODIS at approximately 1 kilometre, while Landsat's Operational Land Imager can provide active-fire detections at 30 metres.[5]

The finer Landsat spatial detail comes with lower temporal coverage than the daily global coverage available from VIIRS and MODIS.[5]

Different systems are therefore useful for different questions.

A rapidly evolving fire may benefit from frequent observation.

Detailed mapping of fire location and extent may benefit from finer spatial resolution.

There is no single resolution that maximizes every evidentiary property simultaneously.

## 11. Finer Spatial Resolution Is Not Automatically Better Evidence

The NASA example illustrates an important boundary.

`Finer Spatial Resolution`

does not automatically mean:

`More Useful Evidence for Every Claim`

A sensor providing frequent wide-area coverage may be more useful for monitoring rapid change across a large area.

A sensor with finer pixels may be more useful for distinguishing small local features.

The appropriate evidence therefore depends partly on the scale and dynamics of the phenomenon.

Maximum spatial detail is not a universal research objective.

## 12. Measurement Resolution Determines Which Numerical Changes Can Be Distinguished

Measurement resolution creates the numerical version of the same problem.

Suppose an instrument effectively distinguishes increments of:

`1 unit`

Two underlying states:

`100.1`

and:

`100.4`

may not be distinguishable as separate measurements.

If the research claim concerns a change of:

`0.2`

the measurement system may not be able to support that distinction.

This is not necessarily measurement error.

The instrument may function correctly.

The limitation lies in how finely it can discriminate among nearby states.

## 13. More Displayed Digits Do Not Establish Better Resolution

Digital instruments and databases can display many decimal places.

That visual precision can be misleading.

NIST explicitly warns:

**The number of displayed digits does not determine the resolution of the instrument.**[1]

A device might display:

`12.34567`

without meaningfully distinguishing changes at the fifth decimal place.

The relevant distinction is therefore:

`More Digits ≠ More Measurement Resolution`

Formatting can create apparent precision that the measurement system itself does not support.

## 14. Resolution Is Not the Same as Measurement Quality

Fine resolution does not automatically produce reliable measurement.

NIST research on finite-resolution measurements shows that finite resolution contributes to measurement uncertainty and interacts with measurement noise in ways that are not always simple.[2]

USGS high-frequency monitoring guidance similarly requires careful sensor operation, cleaning, calibration, evaluation, review, and quality assurance.[3]

A system may generate highly detailed measurements while still facing:

- Calibration error.
- Noise.
- Drift.
- Missing observations.
- Interference.
- Sensor fouling.
- Processing problems.

Resolution therefore answers one question:

**How finely can the system distinguish observations?**

It does not answer every question about whether those observations are accurate, stable, or trustworthy.

## 15. Category Granularity Is Also a Form of Resolution

Evidence can lose resolution even when no numeric measurement is rounded.

Statistical classifications often have several levels.

Eurostat's NACE Rev. 2.1, for example, is hierarchical, moving from broad sections through divisions and groups to detailed classes.[8]

Eurostat explains that hierarchical classifications make it possible to collect and present information at different levels of aggregation.[8]

Suppose detailed evidence distinguishes:

`Semiconductor manufacturing`

`Battery manufacturing`

`Electronic components`

but the published dataset reports only:

`Manufacturing`

The broader category is not incorrect.

It has lower categorical resolution.

The detailed activity still exists in the underlying system.

It is no longer separately visible in the reported evidence.

## 16. Stable Broad Categories Can Hide Large Internal Changes

Suppose a broad sector contains two subcategories.

| Subcategory | Change |
| --- | ---: |
| A | +40 |
| B | -40 |

At the broad level:

`Net Change = 0`

The aggregate suggests stability.

The detailed evidence shows substantial internal restructuring.

The classification may not have changed at all.

The issue is simply that the reported category is too broad to expose the opposing movements inside it.

This is different from classification-rule change.

It is a resolution problem.

The evidence retains the broad category but not enough internal differentiation for the narrower pattern to remain visible.

## 17. Higher Category Resolution Also Has Costs

More detailed categories preserve more distinctions.

They can also result in very small groups.

Small categories may create:

- Unstable estimates.
- Greater uncertainty.
- Confidentiality problems.
- Harder comparison.
- More complex reporting.

This is one reason hierarchical classifications provide several levels of detail.

The relevant objective is not:

`Maximum Detail`

It is:

`Enough Detail for the Claim While Preserving Evidence Reliability`

Greater category resolution is useful only when the additional distinctions can be supported reliably.

## 18. Collection Resolution and Reporting Resolution Can Differ

Evidence may be collected at one resolution and published at another.

For example:

`Minute Measurements → Daily Public Average`

or:

`Address-Level Records → District Statistics`

or:

`Detailed Industry Classes → Broad Sector Totals`

The detailed original evidence may still exist internally.

The public dataset may not preserve it.

Researchers using public evidence therefore need to interpret:

`Resolution of the Evidence Available to Them`

rather than assuming:

`Resolution of the Original Collection System`

This distinction is especially important when reporting what public evidence can or cannot establish.

Absence of detail in a public aggregate does not independently establish that the detail was never collected.

## 19. Aggregation Can Cause Irreversible Information Loss

Aggregation is usually many-to-one.

For example:

`Hourly Observations → Monthly Average`

Many different hourly sequences can produce the same monthly average.

The reverse transformation is therefore not uniquely determined.

From the aggregate alone, researchers cannot reconstruct the exact detailed observations that produced it.

The same applies spatially.

Regional averages cannot uniquely recover the original neighborhood values from which they were calculated.

Resolution loss can therefore affect future research long after the original reporting decision was made.

## 20. The Same Mean Can Hide Very Different Evidence

Consider two systems:

### System A

`49, 50, 50, 51`

### System B

`10, 30, 70, 90`

Both have a mean of:

`50`

If only the mean is retained, the systems appear identical on that statistic.

Their underlying variation is very different.

The aggregate supports:

`Same Mean`

It does not establish:

`Same Distribution`

A valid summary is not necessarily a complete representation of the observations from which it was calculated.

## 21. Aggregation Can Hide Short-Duration Failure

Suppose an infrastructure system operates at:

`100% capacity for 23 hours`

and:

`0% capacity for 1 hour`

Its daily average remains high.

For research into average daily utilization, that may be appropriate evidence.

For research into whether interruption occurred, the daily average is insufficient.

The relevant event occurred at a finer temporal scale than the reported evidence preserved.

A high daily average therefore cannot establish:

`No Interruption Occurred`

unless additional evidence supports that claim.

## 22. Aggregation Can Hide Localized Failure

The same principle applies geographically.

Suppose nine districts operate normally while one experiences complete service loss.

A national availability metric may remain extremely high.

That national metric can correctly describe aggregate availability.

It does not establish:

`No District Experienced Failure`

The claim concerns a smaller geographic unit than the aggregate can resolve.

National performance and local continuity are different evidence questions.

## 23. Pattern Absence Must Be Bounded by Resolution

When a dataset shows no visible pattern, the strongest defensible statement may sometimes be:

**No clear pattern is visible at the resolution available in this evidence.**

That is different from:

**No pattern exists.**

The first statement preserves the evidence boundary.

The second may extend beyond it.

A useful distinction is:

`No Pattern Detected at Resolution R`

does not independently establish:

`No Pattern Exists Below Resolution R`

The scale at which evidence was observed and reported therefore forms part of the meaning of a negative finding.

## 24. The Pattern Has a Scale Too

Resolution requirements depend on what researchers are trying to detect.

A relevant phenomenon might last:

`seconds`

`minutes`

`hours`

or:

`years`

It might exist within:

`one street`

`one neighborhood`

`one region`

or:

`an entire country`

It might involve:

`one subgroup`

or:

`the whole population`

It might be a numerical change of:

`0.01`

or:

`10 units`

Evidence must preserve enough detail to distinguish the scale relevant to the claim.

A dataset does not need the maximum possible resolution.

It needs sufficient resolution for the phenomenon being investigated.

## 25. The Same Dataset Can Be Sufficient for One Claim and Insufficient for Another

Consider hourly water-quality observations.

They may be appropriate for asking:

**Did water quality change substantially during the day?**

They may be insufficient for asking:

**Did a contamination pulse lasting thirty seconds occur?**

Conversely, second-by-second monitoring may provide far more detail than needed for a long-term annual trend.

Resolution sufficiency is therefore claim-specific.

The relevant question is not simply:

**Is this high-resolution evidence?**

It is:

**Can the available evidence distinguish the pattern required by this claim?**

## 26. Higher Observation Frequency Does Not Automatically Mean Proportionally More Information

Sampling a slowly changing system every second can produce millions of records.

Many adjacent measurements may contain very similar information.

The number of observations increases dramatically.

The number of substantively different states may not.

This produces another distinction:

`Higher Frequency ≠ Proportional Increase in Evidentiary Information`

Observation frequency should therefore be interpreted relative to how quickly the underlying phenomenon can actually change and how independently the measurement system samples it.

## 27. Resolution and Coverage Are Different Properties

A dataset may have very fine resolution over a small area.

Another may have coarse resolution over an entire country.

For example:

`Dataset A: fine spatial resolution for one city`

`Dataset B: coarse spatial resolution nationwide`

Neither is universally stronger.

For a local infrastructure question, Dataset A may be more useful.

For a national land-pattern question, Dataset B may provide the necessary coverage.

This creates:

`High Resolution ≠ Broad Coverage`

Resolution describes detail.

Coverage describes how much of the relevant system is observed.

Both matter.

## 28. Resolution and Accuracy Are Different Properties

A measurement system can distinguish tiny changes and still be biased.

A high-resolution image can misclassify what each pixel contains.

A sensor can provide frequent, precise timestamps while being poorly calibrated.

Resolution asks:

**How fine a distinction can the system represent?**

Accuracy asks:

**How well does the measurement correspond to the quantity or condition being measured?**

They are related but not equivalent.

A highly resolved incorrect measurement remains incorrect.

## 29. Resolution and Completeness Are Different Properties

A dataset may contain every expected observation and still be too coarse.

Suppose daily observations are present without gaps for ten years.

The dataset may be highly complete.

If the phenomenon of interest lasts only a few minutes, daily resolution may remain inadequate.

The reverse is also possible.

A minute-level sensor may provide excellent temporal resolution while suffering major missing-data periods.

This distinction matters:

`Completeness → Were expected observations present?`

`Resolution → What distinctions can those observations preserve?`

A dataset can perform well on one dimension and poorly on the other.

## 30. Resolution and Classification Are Related but Different

Classification determines where observations belong.

Resolution determines how much distinction remains visible in the evidence being used.

Suppose a classification remains perfectly stable:

`Industry A`

`Industry B`

`Industry C`

but a public dataset publishes only:

`Total Industry`

The classification itself did not change.

The reporting resolution changed.

The detailed category distinctions were aggregated away.

Classification and resolution therefore interact, but they represent different evidence problems.

## 31. Resolution and Timeliness Are Also Different

Evidence can be highly current and still too coarse.

A dataset might update:

`Every five minutes`

while reporting only:

`National totals`

Another may provide neighborhood-level data that are several months old.

Timeliness asks whether the evidence is current enough.

Resolution asks whether it is detailed enough.

A current source does not automatically provide sufficient resolution for a local or fine-scale claim.

## 32. Resolution Can Be Reduced After Collection

Evidence can deliberately be transformed into lower-resolution forms.

Examples include:

`Second-Level Data → Minute Averages`

`Exact Coordinates → District`

`Exact Age → Age Band`

`Detailed Product → Sector`

There can be legitimate reasons for doing this:

- Confidentiality.
- Privacy protection.
- Statistical stability.
- Standardization.
- Storage.
- Communication.
- Reporting simplicity.

The transformation is not inherently problematic.

But it changes which patterns remain observable in the resulting evidence.

## 33. Detailed Source Data Preserve More Analytical Options

When sufficiently detailed original evidence is securely retained, researchers can often create coarser representations later.

For example:

`Hourly → Daily → Monthly`

or:

`Neighborhood → District → Region`

The reverse usually cannot be reconstructed exactly from aggregates alone.

This gives detailed source evidence an important preservation value.

It retains analytical options for future questions.

That does not imply that fine-grained data should always be publicly released.

Privacy, rights, security, licensing, or other governance constraints may require restricted access.

Preservation and public disclosure are separate issues.

## 34. Aggregation Method Matters as Well as Aggregation Level

Two datasets can summarize the same detailed observations over the same time period while preserving different properties.

For example:

`Daily Mean`

`Daily Maximum`

`Daily Minimum`

`Daily Total`

Each describes the original observations differently.

A short peak may disappear from the mean while remaining visible in the maximum.

A total preserves cumulative volume while removing timing.

A minimum preserves the lowest observed state while saying little about typical conditions.

The relevant question is therefore not only:

**At what level was evidence aggregated?**

It is also:

**Which property of the detailed evidence did the aggregation preserve?**

## 35. Averages Can Conceal Operational States

Suppose a system operates half of a period at:

`0`

and half at:

`100`

The mean is:

`50`

The calculation is correct.

But the system never actually operated at 50.

For some research questions, the average may be useful.

For others, the distribution of operating states is essential.

This demonstrates why numerical validity and evidentiary sufficiency are different questions.

The summary can be correct while remaining insufficient for the phenomenon under investigation.

## 36. Maximum Resolution Is Not the Universal Goal

There are many situations in which lower-resolution evidence is appropriate.

A regional estimate may be more statistically stable than an estimate for a very small population.

A monthly average may be more relevant to a long-term trend than second-level variation.

Broad categories may be preferable where detailed categories contain too few observations for reliable reporting.

A lower-resolution sensor with strong calibration may be more useful than a nominally higher-resolution instrument producing unstable measurements.

The objective is therefore not:

`Maximum Resolution`

It is:

`Resolution Appropriate to the Claim`

## Why It Matters

The absence of a pattern can appear persuasive.

The chart is flat.

The monthly average remains stable.

The national statistic does not move.

The instrument reports no distinguishable change.

The broad category appears unchanged.

But before interpreting that absence, researchers need to know whether the evidence was capable of detecting the relevant pattern.

A local effect may disappear nationally.

A short disruption may disappear monthly.

A small numerical change may fall below measurement resolution.

An internal sector shift may disappear inside a broad category.

A local statistical relationship may change after geographic aggregation.

The appropriate conclusion is therefore often not:

**The pattern is absent.**

It is:

**The pattern was not detected at the resolution available in the evidence.**

A stronger conclusion requires evidence that the observation system had sufficient resolution to detect the pattern if it were present.

This is why evidence availability and evidence resolution need to remain separate.

A dataset can be abundant.

It can be complete.

It can be current.

It can be credible.

It can still be too coarse for the question.

`Available Evidence ≠ Sufficient Resolution`

## Limits and Uncertainty

This article does not argue that every dataset should be collected or published at the highest technically possible resolution.

Resolution involves tradeoffs.

NASA's active-fire systems demonstrate that finer spatial detail can come with lower temporal coverage.[5]

USGS high-frequency monitoring demonstrates that finer temporal information also requires additional maintenance, calibration, evaluation, review, and quality assurance.[3]

NIST demonstrates that measurement resolution must be understood separately from display precision and other components of measurement quality.[1][2]

MAUP research demonstrates that geographic aggregation can affect apparent spatial patterns while also recognizing that small geographic units can create their own statistical limitations.[7]

Hierarchical statistical classifications similarly exist because evidence may need to be represented at several levels of detail.[8][9]

The sources reviewed for this article do not establish that:

- Higher resolution always produces stronger evidence.
- Coarse evidence is inherently poor-quality evidence.
- Every fine-scale pattern is substantively important.
- Every aggregate hides a meaningful pattern.
- Observation frequency is identical to effective temporal resolution.
- More displayed digits imply greater measurement capability.
- Fine spatial resolution guarantees accuracy.
- Fine category granularity guarantees statistical reliability.
- One resolution is appropriate for every research question.
- Maximum data detail should always be publicly disclosed.

The broader evidence principle is narrower:

**Resolution determines which distinctions an evidence system is capable of preserving.**

Higher resolution can expose patterns that coarse evidence cannot show.

But the additional detail is useful only when the observations remain sufficiently reliable, interpretable, comparable, and appropriately covered.

The relevant objective is therefore not maximum granularity.

It is sufficient resolution for the phenomenon and claim being investigated, with remaining limits preserved.

`Available Evidence ≠ Sufficient Resolution`

and:

`No Pattern in Coarse Evidence ≠ No Pattern in the Underlying System`

## Sources

**[1] National Institute of Standards and Technology.** "Resolution." *NIST/SEMATECH Engineering Statistics Handbook.* Measurement-process guidance defining resolution as the ability of a measurement system to detect and faithfully indicate small changes and warning that the number of displayed digits does not establish instrument resolution.

**URL:** https://www.itl.nist.gov/div898/handbook/mpc/section4/mpc451.htm

**Accessed:** 29 September 2026.

**[2] Phillips SD, Toman B, Estler WT.** "Uncertainty Due to Finite Resolution Measurements." *Journal of Research of the National Institute of Standards and Technology*. 2008;113(3):143-156. Examines the contribution of finite measurement resolution to uncertainty and its interaction with measurement noise.

**DOI:** 10.6028/jres.113.011

**URL:** https://www.nist.gov/publications/uncertainty-due-finite-resolution-measurements

**Accessed:** 29 September 2026.

**[3] Mathany TM, Saraceno JF, Kulongoski JT.** *Guidelines and Standard Procedures for High-Frequency Groundwater-Quality Monitoring Stations: Design, Operation, and Record Computation.* U.S. Geological Survey Techniques and Methods 1-D7. 2019. Technical guidance explaining that high-frequency time series can reveal short-term groundwater-quality trends that may not be identifiable from monthly or annual sampling and describing associated quality-assurance requirements.

**DOI:** 10.3133/tm1D7

**URL:** https://www.usgs.gov/publications/guidelines-and-standard-procedures-high-frequency-groundwater-quality-monitoring

**Accessed:** 29 September 2026.

**[4] Booth A, Fleck J, Pellerin BA, et al.** *Field Techniques for Fluorescence Measurements Targeting Dissolved Organic Matter, Hydrocarbons, and Wastewater in Environmental Waters: Principles and Guidelines for Instrument Selection, Operation and Maintenance, Quality Assurance, and Data Reporting.* U.S. Geological Survey Techniques and Methods 1-D11. 2023. Defines signal resolution and temporal resolution for field fluorometers and explains that sensor averaging intervals can exceed nominal reporting intervals.

**DOI:** 10.3133/tm1D11

**URL:** https://pubs.usgs.gov/publication/tm1D11

**Accessed:** 29 September 2026.

**[5] NASA Fire Information for Resource Management System, Earthdata.** "Characteristics of VIIRS, MODIS and OLI Sensors and Their Effects on the Spatial Extent of Daily Active Fire Data." 29 September 2022. Technical explanation comparing spatial and temporal characteristics of VIIRS, MODIS, and Landsat OLI active-fire observations and describing the tradeoff between finer spatial detail and observation frequency.

**URL:** https://wiki.earthdata.nasa.gov/spaces/FIRMS/blog/2022/09/29/266967967/Characteristics+of+VIIRS+MODIS+and+OLI+Sensors+and+Their+Effects+on+the+Spatial+Extent+of+Daily+Active+Fire+Data

**Accessed:** 29 September 2026.

**[6] NASA Earthdata.** "FIRMS FAQ: Landsat Fire Data." Official Earthdata documentation. Describes Landsat 30 metre active-fire observations and contrasts their finer spatial resolution with the more frequent global coverage provided by MODIS and VIIRS.

**URL:** https://forum.earthdata.nasa.gov/viewtopic.php?t=5197

**Accessed:** 29 September 2026.

**[7] Buzzelli M.** "Modifiable Areal Unit Problem." In *International Encyclopedia of Human Geography*. 2020. Research reference explaining how changes in the size, shape, or configuration of spatial aggregation units can alter mapped evidence and its interpretation.

**URL:** https://pmc.ncbi.nlm.nih.gov/articles/PMC7151983/

**Accessed:** 29 September 2026.

**[8] Eurostat.** *NACE Rev. 2.1: Statistical Classification of Economic Activities in the European Union, 2026 Edition.* Published 17 September 2026. Official statistical classification guidance describing hierarchical classifications as increasingly detailed partitions that allow information to be collected and presented at multiple levels of aggregation.

**URL:** https://ec.europa.eu/eurostat/documents/3859598/24236479/KS-01-26-047-EN-N.pdf

**Accessed:** 29 September 2026.

**[9] United Nations Statistics Division.** "Classification of Statistical Activities." Official international classification documentation describing a hierarchical structure of statistical domains and categories and its use in organizing statistical information.

**URL:** https://unstats.un.org/unsd/classifications/CSA2

**Accessed:** 29 September 2026.

---

**Groundline Research Lab**  

**Data • Evidence • Provenance • Research Systems**  

Under the DGCP™ framework

