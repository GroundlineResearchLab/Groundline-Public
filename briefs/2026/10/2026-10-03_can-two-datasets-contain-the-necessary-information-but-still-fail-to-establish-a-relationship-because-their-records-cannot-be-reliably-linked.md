# Can Two Datasets Contain the Necessary Information but Still Fail to Establish a Relationship Because Their Records Cannot Be Reliably Linked?

**Date:** 3 October 2026  
**Domain:** Data Linkage and Analytical Connectivity  
**Publication Type:** Brief

## Question

Can two datasets contain the variables needed to investigate a relationship but still be unable to establish that relationship because their records cannot be reliably connected?

## What the Evidence Shows

Yes.

The presence of relevant variables across multiple datasets does not automatically establish that observations in one dataset can be connected to the corresponding observations in another.

The central distinction is:

**Relevant Variables ≠ Linkable Records**

Data linkage requires a defensible basis for determining whether records in separate datasets refer to the same person, organization, place, event, or other unit of analysis.

The U.S. Census Bureau defines record linkage as using characteristics of an entity to determine whether multiple records refer to the same entity.[1]

Its Statistical Quality Standard C4 requires linkage systems to address matters including valid-link criteria, linking variables, standardization, verification, testing, monitoring, evaluation, and documentation.[1]

The Office for National Statistics similarly treats data linkage as joining records that relate to the same entity and distinguishes two major forms of linkage error:

- **False positive:** records relating to different entities are incorrectly linked.
- **False negative:** records relating to the same entity fail to link.[2]

Having the required variables is therefore only part of the evidence structure.

Researchers must also have a defensible connection between the observations those variables describe.

## Information Availability and Analytical Connectivity Are Different

Consider:

`Dataset A: Person ID | Income`

and:

`Dataset B: Person ID | Health Outcome`

If both datasets contain a stable and compatible identifier referring to the same individuals, the records may be connectable at person level.

Now consider:

`Dataset A: Name | Income`

and:

`Dataset B: Age | Health Outcome`

Both datasets contain information relevant to a question about income and health.

But the available fields may provide no defensible way to determine which income observation corresponds to which health observation.

The variables exist.

The record-level relationship does not.

The evidence problem is therefore not merely:

**Is the relevant information available?**

It is:

**Can the observations required by the claim be connected at the appropriate unit of analysis?**

## Shared Identifiers Can Provide a Strong Connection

Unique or otherwise suitable common identifiers can make direct linkage possible.

The OECD describes one approach in which records from separate sources are linked using common identifiers such as social security numbers, fiscal identifiers, or other identifying fields.[3]

In the household distributional framework discussed by the OECD, identifier-based record linkage is the preferred approach where it is available because it connects information consistently at the micro level without requiring statistical assumptions about which records correspond.[3]

The U.S. Census Bureau uses a related structure in its administrative-data environment.

Census documentation explains that incoming records can be probabilistically matched to a reference file using identifying information including name, address, date of birth, and Social Security Number.[4]

When a match can be made, a Protected Identification Key is appended to the incoming record. That key can then support linkage with other Census-held databases.[4]

The important property is not simply that both datasets contain useful variables.

It is that there is evidence that particular records describe the same entity.

## Lack of a Shared Unique Identifier Does Not Make Linkage Impossible

Datasets without one common unique identifier can sometimes still be linked.

Potential linking information may include:

- Name.
- Address.
- Date of birth.
- Geographic information.
- Organizational characteristics.
- Combinations of other distinguishing attributes.

Methods can include deterministic matching, probabilistic linkage, and clerical review.

But uncertain linkage introduces an additional evidence problem.

ONS notes that missing values can reduce the information available for making linkage decisions and can also make linkage-error measurement more difficult.[2]

The resulting linkage therefore needs to be evaluated as a linkage rather than assumed to be correct because a large number of records were matched.

## A High Match Rate Does Not Establish High Linkage Quality

Suppose a linkage process connects 95 percent of the records.

That may appear strong.

But the match rate tells researchers how many records were linked.

It does not establish how many of those links are correct.

ONS explicitly states that match rate is not a measure of linkage quality.[2]

It recommends evaluating linkage through measures including:

**Precision**

The proportion of links made that are true matches.

and:

**Recall**

The proportion of true matches that were successfully found.[2]

This creates an important distinction:

`Many Records Matched ≠ Matches Are Correct`

A linkage system can potentially produce a high match rate while also creating incorrect relationships.

Conversely, a cautious linkage system may make fewer matches while avoiding more false positives.

## Entity Definitions Must Align With the Claim

Even a technically successful match can connect observations recorded at different analytical levels.

Consider:

`Dataset A: Establishment`

`Dataset B: Enterprise`

An enterprise may contain several establishments.

A matching business name therefore does not automatically make an establishment-level observation equivalent to an enterprise-level observation.

The same problem occurs with:

`Household`

versus:

`Individual`

or:

`Facility`

versus:

`Company`

or:

`Municipality`

versus:

`Postal Code`

The datasets can each be valid.

The units represented by their records may still differ.

A relationship can sometimes be studied across those levels, but the analytical interpretation needs to remain consistent with the structure actually linked.

## Time Alignment Matters After Entity Linkage

Correctly identifying the same entity does not automatically mean that all of its attributes describe the same temporal condition.

ONS identifies timing differences as a potential source of error in longitudinal administrative evidence.[5]

Suppose:

`Dataset A: Employment status in January`

and:

`Dataset B: Income in December`

The records may correctly describe the same person.

But treating the January employment condition and December income as simultaneous observations would introduce an additional assumption.

Record linkage therefore involves at least two separate questions:

**Do these records describe the same entity?**

and:

**Do the linked attributes represent sufficiently compatible periods or conditions for the intended claim?**

The first establishes identity linkage.

It does not automatically establish temporal comparability.

## Geographic Alignment Can Create the Same Problem

Suppose one dataset reports information by:

`Municipality`

while another uses:

`Postal Code`

The labels may refer to overlapping geographic spaces without representing identical boundaries.

A technically available geographic field therefore does not automatically establish a one-to-one spatial relationship.

The same issue can arise when boundaries change over time.

A region identifier from one period may not describe the same geographic unit in another period.

Linkage therefore needs to preserve not only the identifier but also the entity that the identifier represents.

## Aggregated Data Support Different Relationships From Record-Level Data

Relevant variables may exist at different aggregation levels.

For example:

`Dataset A: Individual Income`

`Dataset B: Regional Health Outcome`

Both contain information relevant to income and health.

But a regional health statistic cannot be assigned directly to one person's health experience merely because that person lives within the region.

The OECD distinguishes direct record linkage at the micro level from approaches in which results from separate sources are connected only after aggregation.[3]

Both approaches can support legitimate analysis.

They support different analytical claims.

Aggregate-level evidence may support questions such as:

**Do regions with higher average income also have different regional health outcomes?**

It does not independently establish:

**Does this individual's income correspond to this individual's health outcome?**

The level at which data can be linked therefore constrains the level at which the resulting relationship can be interpreted.

## Incorrect Linkage Can Create a Relationship That Never Existed

Suppose Person A has an income record.

Person B has a health record.

An incorrect linkage creates:

`Person A Income + Person B Health Outcome`

Both individual values may be accurate.

The combined analytical record is not.

ONS identifies this as a false positive linkage.[2]

The reverse also matters.

If two records actually describe the same person but fail to link, a genuine relationship may remain absent from the analytical dataset.

That is a false negative.[2]

Linkage errors can therefore affect evidence in two directions:

`Relationships Incorrectly Created`

and:

`Relationships Incorrectly Missed`

This is why the linkage itself forms part of the evidence supporting a relationship.

## Linkage Does Not Eliminate Other Comparability Problems

Successful record linkage establishes a connection between records.

It does not automatically establish that every variable attached to those records is comparable.

Two correctly linked datasets can still differ in:

- Definitions.
- Measurement methods.
- Observation periods.
- Geographic boundaries.
- Coverage.
- Missingness.
- Category systems.
- Data quality.

For example, two datasets may correctly link the same company while defining:

`Revenue`

differently.

The entity relationship is correct.

The variable relationship may still require qualification.

Record linkage therefore solves one evidence problem.

It does not solve every evidence problem created when sources are combined.

## What Relevant Variables Do Not Establish

The presence of relevant variables across datasets does not by itself establish that:

- Records refer to the same entities.
- A usable common identifier exists.
- Identifiers are stable across periods.
- Entity definitions are compatible.
- Geographic units align.
- Observation periods align.
- Record levels are equivalent.
- Individual observations can be connected reliably.
- Aggregate evidence can be interpreted at individual level.
- A matched pair is a true match.
- An unmatched pair necessarily represents different entities.
- Linkage error is negligible.
- A high match rate establishes high linkage quality.
- The linked variables are methodologically comparable.
- The resulting relationship can be interpreted at the level required by the claim.

The existence of information is therefore different from the existence of a defensible evidentiary connection between pieces of information.

## Why It Matters

Two datasets may appear to contain everything required for an analysis.

One contains:

`Variable X`

The other contains:

`Variable Y`

It may therefore appear that the relationship between X and Y can be calculated simply by combining the files.

But record-level relationship evidence requires more than the presence of the variables.

Researchers need a defensible reason to conclude that:

`X Observation A`

belongs with:

`Y Observation A`

rather than:

`Y Observation B`

The narrower principle is:

**Relevant information in separate datasets does not independently establish a relationship between their records. The connection itself requires evidence.**

A relationship created through linkage inherits the quality and limitations of that linkage.

If the records cannot be connected reliably at the analytical level required by the claim, possessing both variables does not repair that missing connection.

## Limits

This brief addresses one narrow evidence issue: whether the presence of relevant variables in separate datasets is sufficient to establish a relationship between them.

It does not establish that datasets without common unique identifiers cannot be linked.

Deterministic, probabilistic, clerical, statistical, and other methods can support defensible linkage where suitable information and evaluation are available.

It also does not establish that record-level linkage is required for every research question.

Some analyses can legitimately connect evidence at:

- Geographic level.
- Institutional level.
- Population-group level.
- Time-period level.
- Other aggregate levels.

The public sources reviewed for this brief do not establish:

- That unique identifiers are always error free.
- That probabilistic linkage is inherently unreliable.
- That every unmatched record represents a linkage failure.
- That every matched record represents a correct match.
- That high linkage rates establish high linkage quality.
- That differently timed observations can never be analyzed together.
- That datasets using different aggregation levels cannot support any common analysis.
- That linkage quality alone determines the validity of the final analytical conclusion.

The appropriate linkage structure depends on the relationship being investigated and the level at which the claim is made.

The relevant boundary is therefore not whether two datasets contain useful information.

It is whether the observations required by the claim can be connected with sufficient reliability.

The central distinction remains:

**Relevant Variables ≠ Linkable Records**

## Sources

**[1] U.S. Census Bureau.** "Statistical Quality Standard C4: Linking Data Records." Official statistical quality standard covering automated and clerical record linkage for statistical purposes. Requires planning, valid-link criteria, linking variables, variable standardization, system verification and testing, monitoring and evaluation, and documentation of linkage operations.

**URL:** https://www.census.gov/about/policies/quality/standards/standardc4.html

**Accessed:** 3 October 2026.

**[2] Office for National Statistics.** "Data linkage and matching policy." Official ONS policy for data linkage used in research and statistical production. Defines false positive and false negative linkage errors, states that match rate does not measure linkage quality, and requires linkage quality to be assessed using measures including precision and recall.

**URL:** https://www.ons.gov.uk/aboutus/transparencyandgovernance/datastrategy/datapolicies/datalinkageandmatchingpolicy

**Accessed:** 3 October 2026.

**[3] Organisation for Economic Co-operation and Development.** "Linking or matching data across data sources." In *OECD Handbook on the Compilation of Household Distributional Results on Income, Consumption and Saving in Line with National Accounts Totals*. Methodological guidance distinguishing micro-level record linkage, statistical matching, and aggregate-level approaches. In this framework, direct linkage through common identifiers is the preferred option where suitable identifiers are available.

**URL:** https://www.oecd.org/en/publications/oecd-handbook-on-the-compilation-of-household-distributional-results-on-income-consumption-and-saving-in-line-with-national-accounts-totals_5a3b9119-en/full-report/component-10.html

**Accessed:** 3 October 2026.

**[4] U.S. Census Bureau.** "Data Ingest and Linkage." Official Census administrative-data documentation. Describes probabilistic linkage to a reference file using identifying information and the assignment of Protected Identification Keys to support linkage with other Census-held databases.

**URL:** https://www.census.gov/about/adrm/linkage/technical-documentation/processing-de-identification.html

**Accessed:** 3 October 2026.

**[5] Office for National Statistics.** "An error framework for longitudinal administrative sources; its use for understanding the statistical properties of data for international migration." *ONS Working Paper Series No. 19.* Identifies timing differences, coverage differences, false positive linkage, false negative linkage, definitional differences, and other sources of error in longitudinal and multiple-source administrative evidence.

**URL:** https://www.ons.gov.uk/methodology/methodologicalpublications/generalmethodology/onsworkingpaperseries/onsworkingpaperseriesno19anerrorframeworkforlongitudinaladministrativesourcesitsuseforunderstandingthestatisticalpropertiesofdataforinternationalmigration

**Accessed:** 3 October 2026.

---

**Groundline Research Lab**  
**Data • Evidence • Provenance • Research Systems**  
Under the DGCP™ framework

**Commit:** `Add brief on record linkage and analytical relationships`
