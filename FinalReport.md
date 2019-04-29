# Effective Cybersecurity Measurement using the NIST CSF
## Executive Summary
(overview of project, reuse from milestone 1, update if scope changed)

Cybersecurity departments across the United States all face a common problem: they spend loads of money and resources on implementing strong security controls with no standard way to measure the effectiveness of those controls. There are numerous frameworks that exist, including the National Institute of Standards and Technology (NIST) Cybersecurity Framework (CSF). However, these frameworks typically are limited to identifying which controls to apply and do not include how to measure the effectiveness of the implemented controls. The inability to measure the effectiveness of cybersecurity controls has a large potential impact on organizations. It can lead them to spend money on the wrong technologies, the wrong tools for their situation, or to waste resources because they do not fully understand the capabilities of the tools they purchased.

Initial investigation into the problem of the effective cybersecurity measurement revealed a variety of frameworks that have been published for the purpose of measuring cybersecurity programs.  Some of the most popular are listed below:
 * NIST 800-53 - Security and Privacy Controls for Federal Information Systems and Organizations
 * NIST Cybersecurity Framework
 * CIS Top 20 Critical Security Controls
 * ISO 27001/27002
Each of these are effective frameworks for measuring cybersecurity programs as a whole.  Many of them utilize a risk-based approach to doing so.  However, this approach makes it challenging to apply the framework for measuring a specific tool or set of tools.  Others, such as the CIS Top 20 Controls, are more technically oriented, but still apply controls at too high of a level.  When evaluating a specific type of tool, say a perimeter firewall, the Top 20 controls do not cover the breadth of measurement that would be required to effectively measure the  tool.

Over the course of this project, we created a repeatable methodology that can be used to identify a set of controls or questions that can be asked about a specific tool with the objective of more effectively measuring given tools.  This methodology was then applied in the context of three technology domains and evaluated for effectiveness with test organizations.

If this methodology is successful, it has the potential to greatly reduce the amount of toil that teams go through when evaluating new products, either because they waste time evaluating against controls that do not make sense or because they do not have a clear vision about how to measure tools.  This methodology could help provide that direction.  Additionally, it could assist companies in ensuring that their cybersecurity tools are meeting their needs, something that is not easy to measure in a standardized way today.

## Project Goals
(high level project goals, reuse from milestone 1, update if scope changed)

The goal of this project is:

 * Determine if it is possible to use the Cybersecurity Framework from NIST (NIST-CSF) as a tool to determine the controls that should be in place for a various security tools within the reference frame.
 * Determine a rating/metric scale to measure the effectiveness of security tools using the subset of controls that should be in place for that class of technology
 * Develop a survey to be used by individuals looking to rank or compare security tools in specific technology classes.
 * Determine how effectively the measurement survey can be applied to test organizations and how easy the survey makes it to measure tool effectiveness compared to evaluating against all controls

## Project Methodology
(specific methodology followed in the project, reuse from milestone 1/2, update if scope changed)

#### Project Overview
Cybersecurity departments across the United States all face a common problem: they spend loads of money and resources on implementing strong security controls with no standard way to measure the effectiveness of those controls. There are numerous frameworks that exist, including the Cybersecurity Framework from NIST. However, these frameworks typically are limited to measuring security programs as a whole and do not focus on how to measure the effectiveness of security tools that have been implemented.  The inability to measure the effectiveness of cybersecurity tools, specifically, has a large potential impact on organizations.  It can lead them to spend money on the wrong technologies, the wrong tools for their situation, or to waste resources because they do not fully understand the capabilities of the tools they purchased.

Developing a strong and comprehensive approach to measuring implemented security technologies and their corresponding security controls has the potential to greatly impact security organizations and ensure their resources are used as effectively as possible.  The goal of this project is to develop a repeatable process that, when followed, produces a prototype of a measurement framework for specific technology domains that leads to a strong and comprehensive method of measuring the effectiveness of the evaluated technologies and their associated controls.  This prototype will be in the form of a survey, which an individual can fill out in regards to the technology that is being evaluated and will output a measurement indicating how effective the control is.

This project utilizes the NIST Cybersecurity Framework (CSF) as the foundation for evaluation [1].  The CSF is an industry-accepted framework which defines "standards, guidelines, and best practices to manage cybersecurity-related risk" [1].  The framework operates by defining broad functions which define the different stages of a Cybersecurity lifecycle, including Identify, Protect, Detect, Respond, and Recover.  Within each function, categories and subcategories are further defined to identify the outcomes that are expected in that category.  

As designed, the CSF is intended to be used by an organization as a way to evaluate themselves against the CSF to see how well they have achieved the desired outcomes.  This works great from a high-level perspective of the organization as a whole.  However, it is less effective and more time consuming when trying to evaluate something more specific, such as a specific technology.  When evaluating a specific technology, many of the controls do not apply to the evaluated technology, which could cause a significant amount of time wasted if evaluating several technologies.  Thus, this project focuses on demonstrating that there is an effective method of identifying specific controls that apply to specific classes of technology that can be used to measure that technology, documenting that method, and providing a survey that can be used to easily evaluate a tool that exists in that technology domain against only the applicable CSF controls.  This should save time and streamline the process for evaluations that are more specific.

#### Defining Technology domains

For the sake of this project, we define a technology domain as a broad class of technologies that are used in an enterprise network environment.  Examples of technology domains include perimeter technologies, data center technologies, identity and access management technologies, etc.  Within each technology domain, there are more specific classes of technologies.  An example of different classes of technologies within the data center technologies domain could include operating system monitoring software, temperature monitoring software, a hypervisor that allows for virtualization of the servers running in the data center, etc.  Essentially, these technology classes are types of software that operate in that domain.  Within each technology class are specific tools which perform the function of that technology.  For example, two tools that fall into the hypervisor class of technologies are VMWare ESXi and Citrix ZenServer.

When evaluating for the sake of this project, we chose to focus on the middle layer: the specific class of technology.  This decision was made because we felt it gave the most impact in creating an effective, usable method for measuring the effectiveness of security technologies and the controls they implement.  If we attempted to evaluate at the level of the technology domain, we would end up in the same situation that we outlined earlier with the CSF framework.  That is, it's too high level to get actionable results.  However, if we attempted to evaluate at the tool level, the outcome would be too specific and not repeatable. Thus, we chose to evaluate the class of technology as a whole because it provides enough similarities within the class to be effective, while also being repeatable across tools of the same class.

For this project, we evaluated three unique technology domains and selected a single technology class within each domain to use in our prototype development.  In developing our prototype, we focused on the capabilities of technologies in that class in general instead of on the capabilities of specific tools.

For this project, we chose to evaluate technology classes in the following technology domains.  Each of these domains are considered a building block in a successful security program while also being distinctly different from each other.  They were chosen because of their uniqueness and lack of overlap with each other.  Below we dive into more detail about each domain and the specific class of technology that is evaluated within each domain.
* User Management
* Perimeter Defenses
* Endpoint Technology

The user management technology domain is a broad umbrella of technologies that manage the entire lifecycle of a user, from the time the user is onboarded and their account is created to time the user is offboarded and the account is destroyed and access is removed.  For the sake of this project, we decided to focus specifically on Identity Management software within the user management domain.  Identity Management (IDM) software, also known as Identity and Access Management (IAM) software, is a technology that is put in place to manage people's digital identities.  This can include "verification of entity authenticity, authorization of access control, secure transfer of identity attributes, lifecycle management of identity, administration of work flow while exchanging identity and federation of identity between different domains and dynamic trust delegations" [2].  Examples of IDM tools include Microsoft Active Directory and Oracle Identity Management.  IDM tools are essential to running a strong security program as it ensures that all actions performed in an environment can be traced back to a user.  For this reason, it was included in the scope of our project.

The perimeter defenses technology domain is a group of technologies that sit on the edge of an enterprise network and examine and protect all incoming and outgoing traffic.  These tools can listen in on traffic, route traffic, and examine and block potentially malicious traffic to name a few. For this project we chose to examine next-generation firewalls (NGFW's) specifically.  At its core, a next-generation firewall is a more advanced firewall that goes beyond filtering just on ports and IP addresses.  Instead, it "applies [deep packet inspection] (DPI) firewall technology by integrating Intrusion Prevention Systems (IPS), and application intelligence and control to visualize the content of the data being accessed and processed" [3].  DPI technology allows examining the contents of a packet instead of just what port it is sent to or from in order to determine if the packet is malicious or not.  Examples of such technology include Palo Alto's NGFW or Cisco's NGFW.  Having a strong firewall that allows DPI is often the first line of defense for most companies.  Thus, it was chosen as part of the scope for this project.

The endpoint technology domain is a group of technologies that focus on securing the endpoint.  Once the perimeter is protected, securing the assets that are used by users becomes the next most important thing.  There are many ways to secure an endpoint, including traditional anti-virus, endpoint IDS/IPS, etc.  This project will focus on the endpoint detection and response (EDR) technologies that are often used for more advanced endpoint detection.  EDR technologies typically focus on logging and storing information about how a system has behaved and the events that occurred on the system in order to perform analysis on the system and identify anomalous behavior.  Additionally, strong EDR tools go as far as to respond to the anomalous behavior [4]. Examples of EDR technologies include Crowdstrike Falcon and Carbon Black Response.

With the three classes of technology defined, the team moved on to evaluating the CSF outcomes against those three domains to identify the subset of controls that would apply to each.  The process developed to do this as well as the outcome of this exercise is documented in the next section.

#### Control Selection Methodology and Outcomes

Next, we established a control selection methodology, which is a repeatable process that can be used to identify the subset of controls that are measurable in a given technology domain.  This process, at a high level, contains the following steps:

1. Each member of a team of raters rates each control in the NIST CSF on whether it is measurable in the given technology class.
2. Inter-rater reliability (IRR) is calculated for all controls for the given technology class to determine the overall level of agreement between the raters.
3. If IRR outcomes indicate low levels of agreement, calculate the pairwise percent agreement for each control to identify controls that can be included or excluded based on agreement among raters.
4. For all remaining controls, use a consensus-based approach to determine if the control is measurable or not.

Next, we explain each of these steps in further detail.

First, each member of our team rated each control against its potential to be measured in the given class of technology.  We defined measurement as whether or not a tool could be rated on the following maturity model scale:

Level 0 - Ad-hoc or Not Implemented</br>
Level 1 - Repeatable/Managed (Risk Informed) - Partially Implemented</br>
Level 2- Defined - Largely Implemented</br>
Level 3 - Quantitatively Managed - Fully Implemented</br>
Level 4 - Optimizing - Achieved</br>

For example, if a CSF control indicated whether a specific feature in a tool was implemented, it could be measured on this scale because you can measure the how mature that implementation was.  However, if a CSF control dealt with whether policies were in place, that would not be measurable for the tool on this scale.

For each control, the rater chose an answer of "Yes, the control is applicable and measurable in this domain" or "No, the control is either not applicable or not measurable in this domain".  With each control assessed in each technology class, the next step was to get an idea of how well the group agreed on which controls were measurable and should be included in the survey for each domain.

#### Inter-rater Reliability

We chose to use the Inter-Rater Reliability (IRR) measurement as a way to determine the overall level of agreement between our team of raters within in technology class.  Inter-rater Reliability is “a numerical estimate/measure of the degree of agreement among raters” [5].  We calculated IRR using the Fleiss' Kappa calculation.  The Fleiss Kappa was chosen because of its strength in measuring IRR among more than two raters.

According to [1], the Fleiss Kappa is calculated using the function

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

#### Pairwise Percent Agreement calculation

Next we calculated the pairwise percent agreement to see which controls had high levels of agreement between the raters.  To calculate pairwise percent agreement, we counted the number of pairs that agreed between the five raters and divided this among the total number of pairs (10) to get the percentage that the pairs agreed.  An example of this is shown below.  

First, we show an example control and the ratings on measurability for each rater.

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

Calculating pairwise percent agreement allows us to include or eliminate specific controls based on the agreement.  Any controls with an agreement of 75% or more was either included in the final list of controls or excluded from it based on the majority decision of the raters.

#### Consensus-Based Approach

The pairwise percent agreement account for some of the CSF controls.  However, many controls fell below the 75% mark.  This confirmed for our team that the controls are ambiguous and prone to being interpreted differently by different people.  As a result, we chose to use a consensus-based approach as our final step in our methodology.

In the consensus process, we discussed each of the remaining controls as a group.  In our discussions, we learned how the controls were being interpreted by each member of the team and were able to further refine definitions .  For example, we determined as a group that "assets", which are commonly referred to in the control set, can refer to a computer asset or an information or human asset as well.  Discussing and narrowing these definitions allowed us to narrow down the control set to a manageable level for evaluating the effectiveness of a tool.  The output of these steps provided us with a subset of controls for each technology class that could be used for rating tools in a more manageable way.  The subset of controls that were identified for each technology class is shown below.

##### Identity Management
<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/IDMControls.png">

##### Next Generation Firewalls
<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/PerimeterControls.png">

##### Endpoint Detection and Response
<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/EDRControls.png">

## Results / Findings
(brief overview of outcomes - what did you achieve?, list milestone 1/2/3 outcomes, make an effort to logically collect and organize the findings)

(bulleted lists can also be helpful to structure your results discussion)
* outcome 1
* outcome 2

## Install Instructions (if applicable)
### Requirements
(list of any software / hardware requirements necessary to run the code/app/etc)

### Installation Instructions
(list of steps to install the product/app/code/etc)

### Getting started
(list of any steps to run the code after installation and/or manage the apps over their lifecycle)



# Rubric Information

## Final Report: Packaging and Release
>An important part of developing or assessing a product is making the product or results accessible to those that might want to use it or them. This part of the final milestone tasks you with preparing your product, code, processes, and/or other relevant results for release by using relevant deployment strategies and by creating appropriate companion documentation. It is expected that every team will create a final report for release and review by partnering companies and organizations. All projects with code or other requirements must prepare a list of installation instructions and run instructions necessary to install and run any required apps.

### Code artifact Expectations
>Expectations:
> * Polish your product by squashing as many bugs as possible and cleaning up the user interface.
> * Package your code and/or deployment environment for release using relevant deployment solutions such as [github](https://github.com/), [docker](https://www.docker.com/), [npm](https://docs.npmjs.com/getting-started/creating-node-modules), [bower](https://bower.io/docs/creating-packages/), [apt-get](https://help.launchpad.net/Packaging/PPA), [Python pip](https://packaging.python.org/distributing/), etc. The simplist deployment solution is creating a github repository that is cloneable and has a few short install instructions. Other solutions like docker can be helpful in situations where the deployment environment context is complex or depends on certain versions of supporting software. Others like npm, bower, apt-get, or pip are useful for libraries that others might want to install or add to their own projects.
> * Create ```installation``` and ```getting started``` instructions using markdown in their repository or documentation to detail what an end-user must do to setup their app or product.

### Results and findings Expectations
> * Summarize your results discovered over the life of the project.
> * Summarize findings as they relate to the original proposal in milestone 1. What worked, what didn't work? Where would future work be most useful?
> * The report should arrange documentation generated over the project timeline in a logical way that supports the summary. Think of the final report as a compilation of all of your work over the semester.

> A suggested format for the final report is as follows:

```markdown
# Project name
## Executive Summary
(overview of project, reuse from milestone 1, update if scope changed)

## Project Goals
(high level project goals, reuse from milestone 1, update if scope changed)

## Project Methodology
(specific methodology followed in the project, reuse from milestone 1/2, update if scope changed)

## Results / Findings
(brief overview of outcomes - what did you achieve?, list milestone 1/2/3 outcomes, make an effort to logically collect and organize the findings)

(bulleted lists can also be helpful to structure your results discussion)
* outcome 1
* outcome 2

## Install Instructions (if applicable)
### Requirements
(list of any software / hardware requirements necessary to run the code/app/etc)

### Installation Instructions
(list of steps to install the product/app/code/etc)

### Getting started
(list of any steps to run the code after installation and/or manage the apps over their lifecycle)


```

>### Submission materials
>For this submission, you should submit your final report as a `.md` file called `finalreport.md` or `README.md` (to make it your default page) in your project GitHub repository. You should also convert the md file to pdf and upload it as `finalreport.pdf` for use on other non-web-based file stores.
