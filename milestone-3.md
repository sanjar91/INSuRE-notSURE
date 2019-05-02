# Progress Report - May 2, 2019
## Overview
The efforts made during the time between milestone 2 and milestone 3 can be summarized into four main areas. The first area being that we finished creating our tool. We added  brief summaries of each control. So that the user could have a  more defined definition of the control as it relates to the Tool. We also small details to make the user experience more enjoyable. We also put added back end analytics so it would automatically make the graphs to show the ranking of the tool. The second area is that we sent out our tool to test organizations. We had two organizations that we could send our tool and we had them fill out the survey tool. The next area was that we analyzed the data. With the Data we got back from the test organizations we did the analytics on them and got the results from the survey tool. And the last area was evualating out tool and seeing if it was effective or not. 

## Outcomes
We created the Tool based off the NIST framework. IN that we used the controls that NIST provides in our tool. We went through and decided which Controls should be applied to each area that our tool was designed for. (end point, user Management, Perimeter) Once the controls were chosen we added them to the Tool. To use the tool, the tool needed to be accessed through a link. The link would bring the user to a home page, which desribed what it was and how to use it, and asked for some user information. The user would provide information like the users email so that we could get back to them with the results. THe user would then choose which tool he wanted to measure (endpoint, user management, or perimeter). The tool would bring the user to the controls that were decided to be relevant to the specific tool and the user would rate against two measures. Once all three sections were completed by the user the data would be sent to us to be anaylized and then the results were sent back to the user.

* Continued refining measurements for the scoring form.
* Refined methodology including IRR recalculation, introduced pairwise percent agreement, and further explored using consensus agreement.
* Created Google Form version of the tool to be user friendly.
* Sent the survey to two organizations for testing.

## Methodology

#### Control Selection Methodology

We further refined our control selection methodology during this milestone.  We learned that the previous calculation we used for inter-rater reliability (IRR) did not effectively accomplish the goal we were trying to meet.  We have revised our methodology in the following ways, explained in more detail below:
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

#### Measurement Survey Creation

The survey tool was created using a Google Form.  This method was chosen because the process should be universally adaptable and we did not want to use a proprietary survey tool they might not have access to.  Google forms collects all the data in a spreadsheet/table format.  It is within this table that the graphical representations of the data are calculated.  


<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/surveytoolmain.png">

The survey asks the user to compare 2 items that are desired to be measured within a specified domain: user management, perimeter defenses and endpoint technology.  

<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/survey tool-domainselection.png">

The two items can be individual tools that are used for the same purpose or they can be what the tool is at now and the desired state/new state.  We felt that this flexibility on what measurement 1 and 2 were allowed the survey tool to be used in multiple forms.  The scale that the users assed are based upon the Carnegie Mellon Capability Maturity Model: 

Level 0 - Ad-hoc or Not Implemented</br>
Level 1 - Repeatable/Managed (Risk Informed) - Partially Implemented</br>
Level 2- Defined - Largely Implemented</br>
Level 3 - Quantitatively Managed - Fully Implemented</br>
Level 4 - Optimizing - Achieved</br>

<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/Survey%20tool-domain.png">

Once the user answers the questions, the tool sums the answers inside each of the NIST Control Families:  Identify, Protect, Detect, Respond, and Recover.  Then based upon these calculations, the following graphical representations are created:

<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/bargraph2.png">

<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/spiderweb2.png">

#### Survey Feedback 
To measure whether or not the tool was useful and would meet the needs of the cybersecurity professionals, we included a survey at the end to capture this data.  We had 5 people use the tool from 2 different test organizations.  These people included security analysts, highly technical security engineers, and governance/risk/compliance professionals.  

<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/FeedbackSurvey.png">

The results were very promising: </br>
Ease of use:  4.4 </br>
Understandable:  4.0 </br>

We also allowed for comments to be made on ease of use, did the survey include the necessary controls to adequately evaluate the tools, and what improvements to the tool would they like to see.

Ease of use comments were fairly consistent that the tool was self-explanatory. The adequate evaluation comments were not very enlightening except one user would like the ability to select more controls.  The improvement suggestions were to automate the reporting graphs and to allow the users to compare more than 2 tools.

## Hinderances
The challenge of this methodology is that the controls that were chosen to be used to evaluate the security tools based upon domain can be subjective to the group that was deciding them.  Another person may chose to evaluate based upon slightly different criteria.  To combat this issue, we use to use the IRR and consensus approach.  With the IRR approach, our hope is that a different group of approximately five people would come to similar levels of consensus that we did and that this would be repeatable.

Introducing the IRR approach did introduce it's own challenges.  As discussed above, the threshold for agreement in the IRR approach is generally considered to be 75%, which is higher than our group of five people is mathematically capable of achieving unless we have 100% agreement.  To reduce the impact of this, we added the consensus approach.  Additionally, we adopted a revised threshold of 60% for the sake of this project as described above.

In addition, time constrain was a big challenge on our final mile stone. We would prefer to send our measurement survey to more than two organizations in order to get more accurate feedback. Having additional time and feedback would've helped us re-engineer the survey that best suits a user's needs and requirements. 


## References
[1] Nichols, T. R., Wisner, P. M., Cripe, G. and Gulabchand, L. (2010), Putting the Kappa Statistic to Use. Qual Assur J, 13: 57-61. doi:10.1002/qaj.481
