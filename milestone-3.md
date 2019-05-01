# Progress Report - May 2, 2019
## Overview
* Finalizing Tool
	We finalized the creation of the tool, with the addition of brief summaries of each control. So that the user could have a  more defined definition of the control as it relates to the Tool. We also small details to make the user experience more enjoyable. We also put added back end analytics so it would automatically make the graphs to show the ranking of the tool.
	*Getting tool to test organizations
	Once the tool was finalized, we had sent it to several organizations to be filled out.
	*analyzed data returned from test organization
	*evaluated tool


## Outcomes
(brief overview of outcomes - what did you achieve?)

also list them out like this:
* outcome 1
* outcome 2

#### Methodology

We further refined our methodology during this milestone.  We learned that the previous calculation we used for inter-rater reliability (IRR) did not effectively accomplish the goal we were trying to meet.  We have revised our methodology in the following ways, explained in more detail below:
 * Recalculated inter-rater reliability over the entire control set for each technology domain
 * Based on the level of agreeability, calculated the percent agreement for each individual control
 * Used a combination of percent agreement and a consensus-based approach to determine final set of controls for each domain.

First, we recalculated the inter-rater reliability.  Following additional research, we learned that the IRR calculation is significantly more reliable when there are more items being measured with it.  As a result, we altered our methodology to calculate IRR over the entire set of controls instead of individual controls to get a better idea of the degree to which we agreed overall.

With our new IRR calculation, we used the Fleiss' Kappa calculation.  The Fleiss Kappa was chosen because of its strength in measuring IRR among more than two raters. According to [1], the Fleiss Kappa is calculated using the function  

  ![equation](http://bit.ly/2VhWuFK)

where

  ![equation](http://bit.ly/2VV7c2g) and ![equation](http://bit.ly/2VgE20l).

P<sub>i</sub>, which measures the extent to which all the raters are in agreement about a given item, is defined as

  ![equation](http://bit.ly/2VdfeWV)

and P<sub>j</sub>, which measures the proportion of which raters chose a given category compared to all categories, is defined as

  ![equation](http://bit.ly/2VXd2js)

 In these equations, N corresponds to the number of items being rated, n is the number of raters, and k is the number of categories that the raters can select for each item being rated.  A value of k=1 indicates complete agreement.

Our scenario had five raters (*n* = 5) rate 98 controls (N = 98) as either *Yes*, the control is measurable in the given technology domain, or *No*, the control is not measurable in the given technology domain (*k* = 2).  

Below are the following values we calculated for P and P<sub>e</sub> and the subsequent values of kappa for each of the three evaluated technology domains, rounded to four decimals.

| Technology Domain | P | P<sub>e</sub> | kappa |
|-------------------|---|---------------|-------|
|Identity Management|0.5510|0.5176|0.0692|
|Perimeter|0.6546|0.4991|0.3104|
|Endpoint Detection & Response|0.5918|0.5184|0.1524|

Based on these calculations, we found that there is minimal agreement among the raters at best.  As a result of this, we decided to calculate the pairwise percent agreement among the raters for each of the controls individually to assist in narrowing down which controls are measurable for a given technology domain.

To calculate pairwise percent agreement, we used a similar equation to what was used before. We counted the number of pairs that agreed between the five raters and divided this among the total number of pairs (10) to get the percentage that the pairs agreed.  An example of this is shown below (revised from Milestone 2).  First, we show an example control and the ratings on measurability for each rater.

| Control | Sarah | Lisa | Collin | Lyle | Sanjar |
|---------|-------|------|--------|------|--------|
| ID.RA-1: Asset vulnerabilities are identified and documented | No | Yes | Yes | Yes | Yes |

Next, we identified the number of pairs that agree for each control.  An example of this for the above control is shown in the following table.

| Pair | Answer 1 | Answer 2 | Agreement |
|------|----------|----------|-----------|
| Sarah & Lisa | No | Yes | 0 |
| Sarah & Collin | No | Yes | 0 |
| Sarah & Lyle | No | Yes | 0 |
| Sarah & Sanjar | No | Yes | 0 |
| Lisa & Collin | Yes | Yes | 1 |
| Lisa & Lyle | Yes | Yes | 1 |
| Lisa & Sanjar | Yes | Yes | 1 |
| Collin & Lyle | Yes | Yes | 1 |
| Collin & Sanjar | Yes | Yes | 1 |
| Lyle & Sanjar | Yes | Yes | 1 |
|**Total** | | | **6** |

The final step in this process was to add up the number of pairs that agreed and divide by the total number of pairs evaluated to give the pair-wise percent agreement.  In this case, 6 out of 10 pairs agreed, which gives us a 60% agreement on this control.

Calculating pair-wise percent agreement allows us to include or eliminate specific controls based on the agreement.  Any controls with an agreement of 75% or more was either included in the final list of controls or excluded from it based on the majority decision of the raters.

All remaining controls (those which had an agreement of less than 60%) were then evaluated using the consensus-based approach explained in previous milestones to determine if the controls were measurable in the given domain or not.

## Hinderances
(insert brief discussion of challenges encountered)

## References
[1] Nichols, T. R., Wisner, P. M., Cripe, G. and Gulabchand, L. (2010), Putting the Kappa Statistic to Use. Qual Assur J, 13: 57-61. doi:10.1002/qaj.481
