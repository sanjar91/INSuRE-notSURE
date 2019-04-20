# Progress Report (insert date here)
## Overview
(insert brief overview of efforts made)

## Outcomes
(brief overview of outcomes - what did you achieve?)

also list them out like this:
* outcome 1
* outcome 2

We further refined our methodology during this milestone.  We learned that the previous calculation we used for inter-rater reliability (IRR) did not effectively accomplish the goal we were trying to meet.  We have revised our methodology in the following ways, explained in more detail below:
 * Recalculated inter-rater reliability over the entire control set for each technology domain
 * Based on the level of agreeability, calculated the percent agreement for each individual control
 * Used a combination of percent agreement and a consensus-based approach to determine final set of controls for each domain.

First, we recalculated the inter-rater reliability.  Following additional research, we learned that the IRR calculation is significantly more reliable when there are more items being measured with it.  As a result, we altered our methodology to calculate IRR over the entire set of controls instead of individual controls to get a better idea of the degree to which we agreed overall.

With our new IRR calculation, we used the Fleiss' Kappa calculation.  The Fleiss Kappa was chosen because of it's strength in measuring IRR among more than two raters. According to [1], the Fleiss Kappa is calculated using the function  

  ![equation](http://www.sciweavers.org/tex2img.php?eq=%20%5Ckappa%20%3D%20%5Cfrac%7B%5Cbar%7BP%7D%20%20-%20%20%5Cbar%7B%20P_%7Be%7D%20%7D%7D%7B%201%20-%20%20%5Cbar%7B%20P_%7Be%7D%20%7D%7D&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)

where

  ![equation](http://www.sciweavers.org/tex2img.php?eq=%20%5Cbar%7BP%7D%20%3D%20%5Cfrac%7B1%7D%7BN%7D%20%5Csum_%7Bi%3D1%7D%5EN%20P_%7Bi%7D%20%20&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)

and

![equation](http://www.sciweavers.org/tex2img.php?eq=%20%5Cbar%7BP_e%7D%20%3D%20%5Csum_%7Bj%3D1%7D%5EN%20P_%7Bj%7D%5E%7B2%7D%20%20&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0).

P<sub>i</sub>, which measures the extent to which all the raters are in agreement about a given item being relation, is defined as

  ![equation](http://www.sciweavers.org/tex2img.php?eq=p_i%20%3D%20%5Cfrac%7B1%7D%7Bn%28n-1%29%7D%20%5Cbig%28%20%5Csum_%7Bj%3D1%7D%5Ek%20n_%7Bij%7D%5E%7B2%7D%20-%20n%20%5Cbig%29%20%0A&bc=White&fc=Black&im=jpg&fs=12&ff=arev&edit=0)

and P<sub>j</sub>, which measures the proportion of which raters chose a given category compared to all categories, is defined as

  ![equation](http://bit.ly/2VXd2js)

 In these equations, N corresponds to the number of items being rated, n is the number of raters, and k is the number of categories that the raters can select for each item being rated.  A value of k=1 indicates complete agreement.

Our scenario had five raters (*n* = 5) rate 98 controls (N = 98) as either *Yes*, the control is measurable in the given technology domain, or *No*, the control is not measurable in the given technology domain (*k* = 2).

## Hinderances
(insert brief discussion of challenges encountered)

## References
[1] Nichols, T. R., Wisner, P. M., Cripe, G. and Gulabchand, L. (2010), Putting the Kappa Statistic to Use. Qual Assur J, 13: 57-61. doi:10.1002/qaj.481
