# When Classification Decisions Change What a Dataset Can Reveal

**Date:** 27 September 2026  

**Domain:** Classification Architecture and Evidence Interpretation  

**Publication Type:** Article

## Context

Data do not always enter analysis in the form in which they were originally observed.

A continuous measurement may become a range.

A transaction may become a spending category.

A company may become an industry.

A person may become part of an age group.

An event may become an incident type.

A location may become a region.

A numerical score may become:

`Low`

`Medium`

or:

`High`

These transformations can make complex observations easier to organize, summarize, compare, and communicate.

But they also affect what remains visible.

The United Nations Statistics Division treats statistical classifications as an important part of producing reliable, comparable, and methodologically sound statistics.[1]

Formal classifications contain more than category names. They depend on definitions, structures, coding rules, and relationships among categories.

Eurostat's NACE system illustrates this clearly. Its published classification structure is not considered sufficiently self-explanatory for assigning economic activities. Eurostat therefore provides explanatory notes describing what each category includes, what borderline cases it additionally includes, and what it excludes.[3]

Classification therefore does more than attach a label to an observation.

It creates a structured representation of that observation.

The central distinction is:

`Same Underlying Data ≠ Same Evidentiary View`

The research question is:

**How do classification decisions shape what patterns and relationships a dataset is capable of revealing?**

## What the Evidence Shows

Official statistical systems treat classification as part of statistical production.

UNSD states that statistical classifications are a key requirement for reliable, comparable, and methodologically sound statistics.[1]

Classification systems can also be hierarchical. The UN Classification of Statistical Activities, for example, organizes statistical activities into multiple levels of categories and domains.[2]

Eurostat's NACE system adds another layer: category headings alone are insufficient to establish category membership. Explanatory notes are required to identify included activities, borderline cases, and excluded activities.[3]

Numerical grouping demonstrates the same principle differently.

NIST defines a histogram by dividing a range of observations into bins or classes and counting how many observations fall within each bin. Histograms can reveal features such as location, spread, skewness, outliers, and multiple modes.[4]

But the grouped representation depends partly on how those classes are defined. NIST documents multiple possible class-width approaches and states that no single class-width algorithm is optimal for every underlying distribution.[5]

Across these different forms of classification, a common principle appears:

**Classification affects the representation through which evidence becomes visible.**

## 1. Raw Observations and Classified Data Are Different Evidence States

Consider:

`41, 43, 48, 51, 53, 58, 61, 64, 69`

The raw observations preserve every individual value.

Now classify them as:

`Low: below 50`

`Medium: 50 to 59`

`High: 60 and above`

The resulting representation becomes:

| Category | Count |
| --- | ---: |
| Low | 3 |
| Medium | 3 |
| High | 3 |

Nothing necessarily became inaccurate.

But information changed.

The classified dataset no longer directly displays that:

`41 ≠ 48`

or:

`61 ≠ 69`

Those differences still existed in the original observations.

They have been collapsed inside broader categories.

Classification therefore converts some individual differences into common category membership.

Whether that loss matters depends on the question being asked.

## 2. Classification Determines Which Differences Remain Visible

The same collection of entities can be classified in different ways.

Companies, for example, might be grouped by:

`Industry`

`Revenue`

`Employment`

`Ownership`

`Geography`

or:

`Technology`

The companies remain the same.

The analytical view changes.

An industry classification makes sector structure visible.

A geographic classification makes spatial distribution visible.

A firm-size classification makes differences by scale visible.

Each representation preserves some distinctions and leaves others outside the immediate analytical view.

Classification is therefore partly a decision about which property of the observations becomes visible in the dataset.

## 3. Thresholds Create Category Boundaries

Consider two classifications applied to the same numerical observations.

### Classification A

`Low: < 50`

`High: ≥ 50`

### Classification B

`Low: < 60`

`High: ≥ 60`

The observations are unchanged.

The number classified as high changes because the boundary moved.

This produces:

`Same Measurements + Different Threshold = Different Category Distribution`

Thresholds are therefore part of the evidence structure whenever categories depend on them.

This matters for categories such as:

- Income bands.
- Risk levels.
- Firm size.
- Exposure levels.
- Age groups.
- Performance bands.
- Severity levels.
- Capacity ranges.

A change in category counts does not necessarily establish a change in the underlying measured values if the threshold also changed.

## 4. Category Distance Is Not Measurement Distance

Classification can also make nearby observations appear categorically different.

Consider:

`49.9`

and:

`50.1`

With a threshold at 50, they fall into different categories despite differing by only 0.2.

Meanwhile:

`50.1`

and:

`79.0`

might remain inside the same category despite being much farther apart.

This does not make threshold classification invalid.

Thresholds may be required for regulatory, scientific, operational, or communication purposes.

But category membership and numerical distance represent different kinds of information.

A boundary can create a sharp categorical distinction in data that originally varied continuously.

## 5. Binning Changes the Visible Representation of a Distribution

Histograms provide a direct example.

NIST describes a histogram as a representation created by dividing observations into bins and counting the observations within each bin.[4]

The resulting display can help reveal:

- Center.
- Spread.
- Skewness.
- Outliers.
- Multiple modes.[4]

But bin construction matters.

NIST documents multiple class-width methods and notes that the optimal width depends on the underlying distribution, meaning that no single algorithm is best in every case.[5]

The relevant structure is:

`Same Raw Observations`

`→ Different Bin Structure`

`→ Different Grouped Representation`

The underlying observations remain the same.

What becomes visually prominent can change.

## 6. Classification Can Reveal Structure

Classification is not simply information loss.

It can make evidence interpretable.

Suppose a dataset contains one million transactions.

At the individual-record level, all detail may be preserved.

But broad patterns may be difficult to see.

Grouping transactions into categories such as:

`Food`

`Housing`

`Transport`

`Healthcare`

`Education`

can reveal the structure of expenditure far more clearly.

Detail has been reduced.

Interpretability for a particular question has increased.

This creates an important distinction:

`Information Reduction ≠ Analytical Failure`

Reducing detail can be useful when the remaining distinctions match the research question.

## 7. Classification Can Also Hide Structure

The same operation can conceal differences required for another question.

Suppose:

`Transport`

contains:

- Public transit.
- Air travel.
- Road freight.
- Private vehicles.
- Rail.
- Maritime transport.

For a question about total transport activity, the broad category may be useful.

For a question about substitution between rail and road freight, it is too coarse.

The observations are not necessarily wrong.

The representation no longer preserves the distinction needed for that claim.

A classification can therefore be appropriate for one analytical purpose and insufficient for another.

## 8. Hierarchy Allows Multiple Levels of Detail

Many formal classifications contain hierarchical levels.

UNSD's Classification of Statistical Activities demonstrates such a structure, with broad domains containing more detailed categories.[2]

Economic classifications such as NACE similarly organize activities through progressively more specific levels and provide detailed rules for determining where activities belong.[3]

This allows the same evidence to be represented at different levels:

`Broad Category`

`→ Intermediate Category`

`→ Detailed Category`

A higher level makes broad structure easier to see.

A lower level preserves more internal distinctions.

Neither is automatically the correct level for every research question.

## 9. Aggregation Changes What Questions the Dataset Can Answer

Consider:

| Industry | Output |
| --- | ---: |
| Solar equipment | 20 |
| Battery equipment | 30 |
| Wind equipment | 10 |
| Other machinery | 40 |

The first three categories might be aggregated:

| Category | Output |
| --- | ---: |
| Energy technology | 60 |
| Other machinery | 40 |

The aggregate clearly shows a broad structural comparison.

But it can no longer directly answer:

**Was battery equipment larger than solar equipment?**

The original evidence could.

The aggregated evidence cannot.

Aggregation therefore changes more than table length.

It changes which distinctions remain recoverable from the published data.

## 10. Information Loss Can Be Asymmetric

If detailed observations remain available, broad categories can often be created later.

For example:

`Detailed Categories → Broad Category`

is often possible.

The reverse is different.

From:

`Broad Aggregate`

researchers generally cannot reconstruct:

`Exact Original Detail`

unless another source preserves it.

Once detailed distinctions have been removed, later users may not be able to recover them.

This matters for evidence reuse because the level of classification preserved today can determine which questions remain answerable later.

## 11. Residual Categories Preserve Coverage but Reduce Specificity

Not every observation fits a separately named category.

Classification systems therefore commonly use residual categories such as:

`Other`

or:

`Not Elsewhere Classified`

The Australian Bureau of Statistics explains that `Not elsewhere classified` categories are used for valid responses for which no specific category exists in the classification.[6]

It distinguishes these from `Not further defined`, where there is enough information for partial classification but not enough for assignment to the most detailed category.[6]

Residual categories are useful because they preserve observations that cannot be placed elsewhere.

But they also reduce specificity.

If multiple different activities are placed into:

`Other`

their existence remains visible.

Their internal differences may not.

## 12. "Other" Is Not Automatically One Homogeneous Phenomenon

Residual categories require careful interpretation.

The Australian Bureau of Statistics explains that residual categories may be needed because not every observation can form a separately identified homogeneous group or because some groups are too small to justify separate identification.[7]

This means:

`Other`

does not necessarily represent one coherent underlying activity.

It may represent several different phenomena grouped together because the classification does not distinguish them separately.

An analyst should therefore avoid giving a residual category a stronger substantive meaning than its definition supports.

## 13. A Changing Residual Category Can Be Informative

Suppose:

`Other = 2%`

in one period and:

`Other = 18%`

in another.

That increase does not reveal its cause by itself.

Possible explanations include:

- New activities emerging.
- Existing categories becoming less suitable.
- Changes in coding.
- Different source data.
- Reduced reporting detail.
- Real changes in the population.
- Changes in the classification structure.

The increase can be research-relevant.

But it should not automatically be interpreted as rapid growth of one substantive activity called "Other."

The residual category is itself a classification outcome.

## 14. One Category Assignment Does Not Describe Everything About an Entity

Real-world units are often multidimensional.

A company can simultaneously be:

`A manufacturer`

`An exporter`

`A large employer`

`Foreign-owned`

`A technology user`

`Located in Region A`

If a published dataset retains only industry, the other properties may no longer be visible.

They have not ceased to exist.

They are simply outside that representation.

This explains why the same population can generate different datasets depending on which classification dimensions are preserved.

## 15. Cross-Classification Can Reveal Hidden Differences

A dataset may classify evidence along more than one dimension.

Instead of:

`Employment by Industry`

researchers might examine:

`Employment by Industry × Region`

or:

`Employment by Industry × Firm Size`

Cross-classification can expose patterns hidden inside broader totals.

But additional detail introduces trade-offs.

As categories become more numerous, some combinations may contain very few observations.

That can affect statistical stability, interpretation, and confidentiality.

Greater granularity therefore increases detail but does not automatically increase evidentiary strength.

## 16. Fine and Coarse Classifications Serve Different Purposes

Broad classifications can offer:

- Simpler interpretation.
- Larger groups.
- Easier reporting.
- Greater statistical stability.

But they can hide:

- Subgroups.
- Internal variation.
- Emerging activities.
- Local differences.

More detailed classifications can offer:

- Greater specificity.
- Better subgroup visibility.
- More precise structural description.

But they can also create:

- Sparse categories.
- More complicated coding.
- Harder communication.
- Greater confidentiality concerns.

Classification granularity should therefore be interpreted in relation to analytical purpose.

## 17. Reclassification Can Change a Pattern Without Changing Observations

Suppose 1,000 observations produce:

### Classification A

| Category | Count |
| --- | ---: |
| A | 400 |
| B | 400 |
| C | 200 |

The same observations are then reorganized:

### Classification B

| Category | Count |
| --- | ---: |
| X | 250 |
| Y | 500 |
| Z | 250 |

The underlying 1,000 observations may be identical.

The visible distribution is different.

This is the central distinction:

`Same Observations ≠ Same Classification ≠ Same Visible Pattern`

A change in a classified distribution therefore should not automatically be interpreted as a change in the underlying observations.

## 18. Classification Can Create or Conceal Apparent Concentration

Suppose ten detailed industries contain similar numbers of firms.

A broader classification combines eight of them into:

`Other Services`

while preserving two as named categories.

The resulting table may appear highly concentrated in `Other Services`.

The concentration partly reflects the aggregation structure.

The reverse can also occur.

A broad category can appear balanced while one detailed subcategory accounts for most of the activity inside it.

Whether concentration appears visible can therefore depend on classification level.

This does not mean the underlying concentration is fictitious.

It means the level at which concentration is measured must be clear.

## 19. Rankings Depend on Category Boundaries

Suppose Region A has the largest:

`Technology Sector`

when multiple technology industries are combined.

Region B may have the largest:

`Semiconductor Manufacturing`

when the category is disaggregated.

Both claims can be true.

They concern different classification boundaries.

A ranking therefore inherits the definition and level of the category being ranked.

A ranking without a category definition is incomplete evidence.

## 20. Apparent Similarity Can Also Depend on Classification

Two regions may have identical shares of:

`Manufacturing`

while having very different internal structures.

One may specialize in:

`Food + Textiles`

while another specializes in:

`Electronics + Machinery`

At the broad level:

`Same Manufacturing Share`

At a detailed level:

`Different Industrial Structure`

Whether the regions appear similar depends partly on the resolution of the evidence.

## 21. Aggregates Can Hide Internal Distributions

Suppose:

`Category A average = 50`

and:

`Category B average = 50`

The averages are identical.

But Category A may contain values concentrated tightly around 50.

Category B may contain values ranging from 5 to 95.

Aggregation preserved:

`Same Average`

It did not preserve:

`Same Distribution`

A summary statistic can therefore be valid without preserving every feature of the underlying observations.

The claim must remain limited to what the summary actually establishes.

## 22. Familiar Categories Are Still Analytical Representations

Terms such as:

`Urban`

`Industry`

`Small Firm`

`High Risk`

`Middle Income`

can become so familiar that they appear to be natural properties of the world.

But statistical categories are defined representations.

Their boundaries may be strongly justified.

They may be internationally standardized.

They may be indispensable for research.

They still depend on classification rules.

The evidence distinction is:

`Observed Property`

versus:

`Classification Assigned to That Property`

Confusing the two can make a category appear more natural or inevitable than its underlying definition supports.

## 23. Classification Is Not Inherently a Source of Error

The fact that classification shapes evidence does not mean classification is inherently misleading.

UNSD describes statistical classifications as essential to producing reliable, comparable, and methodologically sound statistics.[1]

Classification enables:

- Standardization.
- Aggregation.
- Comparison.
- Retrieval.
- Statistical production.
- International reporting.
- Communication.

The problem is not that classification occurs.

The problem arises when the classification is invisible to interpretation.

If category boundaries materially affect a conclusion, information about those boundaries is part of the evidence needed to understand that conclusion.

## 24. Classification Metadata Matter for Reuse

A dataset may survive for years while its classification context disappears.

The values remain.

The categories remain.

But a later researcher may not know:

- Which classification system was used.
- Which version applied.
- What each category meant.
- Which aggregation level was retained.
- Which observations were placed into residual categories.

The file may still be readable.

Its categorical meaning may not be reliably interpretable.

Eurostat's NACE guidance illustrates why category headings alone are insufficient: explanatory information is required to understand what belongs inside or outside each category.[3]

Classification information is therefore also part of evidence provenance.

## 25. Reclassification Creates a Different Derived Dataset

Consider the same raw observations processed under two different classifications:

`Raw Data → Classification A → Dataset A`

and:

`Raw Data → Classification B → Dataset B`

Dataset A and Dataset B share the same underlying observations.

They do not necessarily contain the same categorical evidence.

Their distributions, subgroup sizes, rankings, and visible relationships may differ.

This distinction matters especially when downstream analysis uses the classified values rather than the original observations.

The classification step is part of how the evidence object was produced.

## Why It Matters

Data analysis often begins after classification has already occurred.

Researchers download a table.

The categories appear fixed.

The column names look natural.

The classification process may therefore disappear from analytical attention.

But classification has already determined:

- Which differences remain visible.
- Which observations are treated as equivalent.
- Which boundaries matter.
- Which activities receive separate categories.
- Which observations enter residual groups.
- Which detail survives aggregation.
- Which questions remain answerable from the published data.

The dataset does not simply contain observations.

It presents observations through a defined representation.

Two datasets can begin from the same underlying evidence and preserve different parts of it.

One may reveal sector structure.

Another may reveal geographic structure.

Another may reveal firm-size differences.

Another may aggregate those distinctions away.

None must be false.

They are different evidentiary views.

The relevant principle is:

**Classification changes the representation through which evidence becomes visible.**

Sometimes that transformation makes an important structure easier to see.

Sometimes it removes a distinction required for another question.

And sometimes several classifications of the same observations are all legitimate because they serve different purposes.

## Limits and Uncertainty

This article does not argue that raw, unclassified data are inherently superior to classified data.

Raw observations can be difficult to interpret, unsuitable for direct publication, sensitive, noisy, or too detailed for the research question.

Nor does greater granularity automatically produce better evidence.

Highly detailed classification can create sparse categories, unstable estimates, disclosure risks, and excessive complexity.

The UNSD materials cited here concern principles and systems for statistical classification.[1][2]

NACE concerns classification of economic activities and demonstrates why category definitions and inclusion and exclusion rules matter.[3]

The NIST histogram material concerns one specific form of numerical grouping.[4][5]

ABS supplementary-code guidance concerns residual categories in Australian statistical classifications.[6][7]

These sources should not be treated as establishing one universal classification procedure for every evidence domain.

The public sources reviewed do not establish that:

- Classification is inherently misleading.
- Every category boundary is arbitrary.
- More categories always produce stronger evidence.
- Fine classification is always preferable to aggregation.
- Every classified pattern is highly sensitive to classification choices.
- Aggregation necessarily produces an incorrect conclusion.
- Residual categories indicate poor-quality data.
- One classification system can serve every analytical purpose.

The broader conclusion is narrower:

`Same Underlying Data ≠ Same Evidentiary View`

Classification does not merely organize observations after they have been collected.

It helps determine which distinctions the resulting dataset preserves, which patterns become easy to see, and which questions the classified evidence can still answer.

## Sources

**[1] United Nations Statistics Division.** "Best Practices for Developing Statistical Classifications." Official UNSD classification guidance. States that statistical classifications are a key requirement for the production of reliable, comparable, and methodologically sound statistics and provides principles for development, maintenance, and implementation.

**URL:** https://unstats.un.org/unsd/classifications/bestpractices

**Accessed:** 27 September 2026.

**[2] United Nations Statistics Division.** "Classification of Statistical Activities." Official international classification documentation. Describes the Classification of Statistical Activities as an analytical classification with a hierarchical structure of statistical domains and categories.

**URL:** https://unstats.un.org/unsd/classifications/CSA2

**Accessed:** 27 September 2026.

**[3] Eurostat.** "NACE: Guidance." Official guidance for NACE Rev. 2.1. States that the formal NACE structure is not sufficiently self-explanatory for classification and provides explanatory notes identifying activities that each category includes, additionally includes, and excludes.

**URL:** https://ec.europa.eu/eurostat/web/nace/guidance

**Accessed:** 27 September 2026.

**[4] National Institute of Standards and Technology.** "Exploratory Data Analysis: Histogram." *NIST/SEMATECH e-Handbook of Statistical Methods.* Defines histograms by dividing observations into bins or classes and describes the distributional features that histogram representations can help reveal.

**URL:** https://www.itl.nist.gov/div898/handbook/eda/section3/eda33e.htm

**Accessed:** 27 September 2026.

**[5] National Institute of Standards and Technology.** "Histogram Class Width." Dataplot technical documentation. Describes alternative algorithms for histogram class width and states that no single class-width algorithm is optimal for every underlying distribution.

**URL:** https://www.itl.nist.gov/div898/software/dataplot/refman1/auxillar/histwidt.htm

**Accessed:** 27 September 2026.

**[6] Australian Bureau of Statistics.** "Understanding supplementary codes in Census variables." Released 6 June 2022. Official statistical guidance distinguishing supplementary categories including `Not elsewhere classified` and `Not further defined` and explaining how they are used for valid responses that cannot be represented by more specific categories.

**URL:** https://www.abs.gov.au/statistics/detailed-methodology-information/information-papers/understanding-supplementary-codes-census-variables

**Accessed:** 27 September 2026.

**[7] Australian Bureau of Statistics.** "Labour Force Survey concepts and data item guide." Official methodology guidance. Explains the role of residual categories such as `Not elsewhere classified`, `Other`, and `Miscellaneous`, including cases where observations cannot form a sufficiently homogeneous or statistically significant separately identified group.

**URL:** https://www.abs.gov.au/statistics/understanding-statistics/guide-labour-statistics/labour-force-survey-products-guide/labour-force-survey-concepts-and-data-item-guide

**Accessed:** 27 September 2026.

---

**Groundline Research Lab**  

**Data • Evidence • Provenance • Research Systems**  

Under the DGCP™ framework

