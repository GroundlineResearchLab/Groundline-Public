# Can Two Datasets Built From the Same Observations Support Different Apparent Patterns Because They Use Different Classification Rules?

**Date:** 27 September 2026  

**Domain:** Classification and Pattern Visibility  

**Publication Type:** Brief

## Question

Can two datasets built from the same underlying observations show different apparent patterns because those observations are classified differently?

## What the Evidence Shows

Yes.

The underlying observations can remain unchanged while the categories used to organize them change.

The central distinction is:

**Same Observations ≠ Same Classification ≠ Same Visible Pattern**

The SDMX Glossary defines a statistical classification as a set of categories that can be assigned to variables and used in the production and dissemination of statistics.[1]

It also recognizes that classifications may be hierarchical, with categories at more detailed levels contained within broader categories at higher levels.[1]

Classification therefore affects how observations are partitioned before aggregated results are presented.

The same observations might, for example, be organized as:

`Low | Medium | High`

or:

`Low | Lower-Middle | Upper-Middle | High`

or:

`Below Threshold | Above Threshold`

The measurements themselves have not necessarily changed.

What changed is the rule determining which observations appear together.

That can change category counts, proportions, distributions, and the pattern visible in the resulting table or chart.

## Classification Changes the View of the Evidence

Classification can differ through:

- Thresholds.
- Category boundaries.
- Number of categories.
- Grouping rules.
- Hierarchical level.
- Treatment of residual categories.
- Degree of aggregation.

These differences do not necessarily alter the original observations.

They alter how those observations become visible after classification.

A difference hidden inside one broad category may become visible when that category is divided.

Conversely, a pattern visible among detailed categories may disappear when those categories are aggregated into a broader group.

The result is not necessarily conflicting evidence.

It may be the same evidence viewed through different classification structures.

## Degree of Urbanisation Provides a Practical Example

Eurostat's Degree of Urbanisation classification illustrates this distinction.

At its principal level, the methodology classifies local administrative units into three mutually exclusive classes:

- Cities.
- Towns and suburbs.
- Rural areas.[2]

The classification is based on population-grid information and uses population density, population size, and geographical contiguity to identify settlement structures.[3]

Eurostat also provides a more detailed Level 2 classification.

At that level, the broader urban-rural structure is divided into seven classes, including distinctions such as dense towns, semi-dense towns, suburban or peri-urban areas, villages, dispersed rural areas, and mostly uninhabited areas.[4]

The underlying population evidence does not have to change for this more detailed pattern to appear.

At the broader level, several settlement types are intentionally grouped together.

At the more detailed level, those distinctions become visible.

Neither level necessarily contradicts the other.

They represent different levels of classification detail applied to the underlying population structure.

## The Same Observations Can Produce Different Distributions

Consider an illustrative dataset containing ten measured values:

`12, 18, 23, 29, 34, 41, 47, 53, 66, 78`

One classification might define:

`Low: < 30`

`Medium: 30 to 59`

`High: ≥ 60`

The resulting distribution is:

`Low: 4`

`Medium: 4`

`High: 2`

Now apply different boundaries:

`Low: < 20`

`Medium: 20 to 49`

`High: ≥ 50`

Using exactly the same observations, the distribution becomes:

`Low: 2`

`Medium: 5`

`High: 3`

Nothing in the underlying measurements changed.

The classification boundaries changed.

As a result, the visible category distribution changed.

This example does not establish that either classification is better.

It demonstrates a narrower point:

**Category distributions depend partly on the rules used to partition the observations.**

## Aggregation Can Hide Existing Differences

Classification also changes visibility through aggregation.

Suppose detailed observations are organized as:

`A1 | A2 | B1 | B2`

A higher-level classification may combine them into:

`A | B`

The number of underlying observations remains unchanged.

But differences between A1 and A2, or between B1 and B2, are no longer visible in the aggregated presentation.

This is a normal property of hierarchical classification.

SDMX defines a hierarchy as a classification structure arranged from broader to more detailed levels, with categories at lower levels related to categories above them.[1]

Aggregation therefore trades detail for a broader view.

That may be entirely appropriate for a particular purpose.

But the broader view cannot display distinctions that were collapsed during aggregation.

## Different Visible Patterns Do Not Necessarily Mean Different Underlying Evidence

Suppose two reports use the same source observations.

One displays results using three broad categories.

The other uses seven more detailed categories.

Their charts may look different.

One may show apparent concentration.

The other may reveal internal variation.

One may appear relatively uniform.

The other may expose distinct subgroups.

Those differences do not necessarily establish disagreement in the underlying observations.

They may arise because the reports preserve different levels of detail.

This creates another useful distinction:

`Change in Observation`

is different from:

`Change in Classification`

The first concerns the underlying evidence.

The second concerns how that evidence has been organized.

## Thresholds Can Produce Apparent Movement

Threshold-based classifications make this especially visible.

Suppose an observation has a measured value of:

`72`

Under one classification:

`High = ≥ 80`

the observation belongs to:

`Medium`

Under another:

`High = ≥ 70`

the same observation becomes:

`High`

The measurement remains:

`72`

Only its category assignment changes.

If many observations lie close to the changed threshold, the resulting category distribution can shift substantially without any change in the underlying measurements.

An apparent increase in the number of "high" observations can therefore arise from:

`Real Change in Measurements`

or:

`Change in Classification Threshold`

or some combination of both.

The category counts alone cannot distinguish those possibilities.

## More Detail Is Not Automatically Better Evidence

A more granular classification preserves more distinctions.

That does not mean it is always better.

Broad categories may be appropriate for:

- International comparison.
- Summary reporting.
- Communication.
- Long historical series.
- Policy categories defined by regulation.

More detailed categories may be appropriate for:

- Local analysis.
- Subgroup analysis.
- Spatial planning.
- Identifying internal variation.

The appropriate classification depends on the question being examined.

A system with more categories may reveal distinctions that a broad classification conceals.

It may also create detail that is unnecessary for another purpose.

Classification therefore involves a trade-off between aggregation and granularity rather than a universal rule that more categories produce stronger evidence.

## What the Same Underlying Observations Do Not Establish

Use of the same underlying observations does not by itself establish that two classified datasets will show:

- The same category distribution.
- The same proportion in each category.
- The same apparent concentration.
- The same subgroup distinctions.
- The same ranking of category sizes.
- The same visible spatial pattern.
- The same amount of visible variation.
- The same analytical granularity.

Nor does a different visible pattern establish that the underlying observations changed.

The difference may arise from:

- Different thresholds.
- Different category boundaries.
- Different grouping rules.
- Different numbers of categories.
- Different levels of aggregation.
- Different hierarchical levels.

A classified output therefore contains information from both:

`Underlying Observations`

and:

`Classification Structure`

The two should not be treated as the same thing.

## Why It Matters

Tables, dashboards, maps, and charts frequently present classified evidence rather than raw observations.

The categories can begin to look like properties of the underlying world.

But the visible pattern depends partly on how boundaries were defined and which observations were grouped together.

A broad classification can hide differences.

A detailed classification can expose them.

A threshold change can move observations between categories without changing their measured values.

An aggregation can remove distinctions that remain present in the underlying data.

The narrower principle is:

**The same underlying observations can support different visible distributions when different legitimate classification rules are applied.**

A difference between classified outputs should therefore not automatically be interpreted as a difference in the underlying observations.

Sometimes the evidence changed.

Sometimes the classification changed.

And sometimes both changed.

## Limits

This brief addresses one narrow evidence problem: whether different classification rules can produce different apparent patterns from the same underlying observations.

It does not establish that every classification materially changes an analytical result.

Different classifications may produce substantially similar patterns when most observations fall far from changed boundaries or when aggregation does not conceal important variation.

It also does not establish that unclassified data are inherently superior.

Classification is necessary in many statistical systems.

It can make complex observations interpretable, support consistent reporting, enable comparison, and reveal patterns that are difficult to see in raw measurements.

The public sources reviewed for this brief do not establish:

- That classification is inherently misleading.
- That every category boundary is arbitrary.
- That more categories always produce better evidence.
- That finer granularity is always preferable.
- That aggregation necessarily produces an incorrect conclusion.
- That different classified patterns must be caused by classification alone.
- That one classification is suitable for every analytical purpose.

The broader conclusion is narrower:

**When a visible pattern is produced from classified or aggregated data, the classification structure forms part of the evidence needed to understand what that pattern represents.**

The raw observations and their classified presentation are related.

They are not identical evidence objects.

## Sources

**[1] SDMX Statistical Working Group.** *SDMX Glossary, Version 2.1.* December 2020. Official statistical metadata terminology. Defines a statistical classification as a set of categories assignable to variables and used in the production and dissemination of statistics, and describes classifications that may contain hierarchical levels.

**URL:** https://sdmx.org/wp-content/uploads/SDMX_Glossary_Version_2_1_December_2020.htm

**Accessed:** 27 September 2026.

**[2] Eurostat.** "Degree of urbanisation: Information on data." Official statistical documentation. Describes the Degree of Urbanisation as a classification of territory along the urban-rural continuum using population size and population density thresholds to establish three mutually exclusive classes: cities, towns and suburbs, and rural areas.

**URL:** https://ec.europa.eu/eurostat/web/degree-of-urbanisation/information-data

**Accessed:** 27 September 2026.

**[3] Eurostat.** "Degree of urbanisation: Methodology." Official methodology. Describes the two-stage classification using 1 km² population grid cells, population density, population size, geographical contiguity, and the population shares used to classify local administrative units as cities, towns and suburbs, or rural areas.

**URL:** https://ec.europa.eu/eurostat/web/degree-of-urbanisation/methodology

**Accessed:** 27 September 2026.

**[4] Eurostat.** "Degree of urbanisation." GISCO statistical geodata documentation. Describes Degree of Urbanisation Level 2 as a more detailed seven-class classification that subdivides the broader Level 1 categories and exposes additional distinctions within intermediate and rural areas.

**URL:** https://ec.europa.eu/eurostat/web/gisco/geodata/population-distribution/degree-urbanisation

**Accessed:** 27 September 2026.

---

**Groundline Research Lab**  

**Data • Evidence • Provenance • Research Systems**  

Under the DGCP™ framework

