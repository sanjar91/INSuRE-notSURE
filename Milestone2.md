# Progress Report (March 28, 2019)
## Overview
For the improving of Cybersecurity Measurement Science, we have focused on developing a scoring technique that shows the maturity score of a domain. We have researched and evaluated three domains (User Management, Perimeter Defenses, Endpoint Technology) against the National Institute of Standards and Technology Cybersecurity Framework (NIST CSF) controls and have created smaller and more specific control for each domain. We choose these three domains because of the significant difference from each other. This process shows that the process can be reused for other domains and is flexible in its implementation. We were able to narrow down the controls to ten to twenty controls per domain. We used Inter-rater Reliability (IRR) to see which controls should be used for each domain and consensus-based approach for any items that didn't meet the IRR threshold. This allows for more precise questions for the scoring tool which in turn will give a more precise maturity rating. We have planned measurements for the first draft of measurement questionnaire for each selected control.

## Outcomes

To date, we have achieved the following major outcomes in relation to our project.  These outcomes are explained in more detail below, including the methodologies we used and the outcomes of those methodologies.
* Identified the technologies which are being used in the evaluation described below
* Completed initial evaluation of the NIST Cybersecurity Framework (CSF) against the identified technologies
* Used the inter-rater reliability function and a consensus-based approach to identify the specific vulnerabilities which are considered measurable for each identified technology
* Identified measurements for first draft of measurement scoring form

#### Project Overview
Cybersecurity departments across the United States all face a common problem: they spend loads of money and resources on implementing strong security controls with no standard way to measure the effectiveness of those controls. There are numerous frameworks that exist, including the Cybersecurity Framework from NIST. However, these frameworks typically are limited to identifying which controls to apply and do not include how to measure the effectiveness of the implemented controls.  The inability to measure the effectiveness of cybersecurity controls has a large potential impact on organizations.  It can lead them to spend money on the wrong technologies, the wrong tools for their situation, or to waste resources because they do not fully understand the capabilities of the tools they purchased.

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

##### Maturity Model
The scoring tool uses a maturity ranking/scoring of each item to determine the average score based upon NIST CSF categories. </br>
Level 0 - Ad-hoc or Not Implemented</br>
Level 1 - Repeatable/Managed (Risk Informed) - Partially Implemented</br>
Level 2- Defined - Largely Implemented</br>
Level 3 - Quantitatively Managed - Fully Implemented</br>
Level 4 - Optimizing - Achieved</br>

The team categorized the CSF in to three control types; Administrative, Operational, Technical. **Administrative** are controls related to an organization’s policy, procedures, and/or written instructions. **Technical** are controls that can be executed using a technology, and technical controls are measureable. **Operational** controls are the processes carried out with a technology by following administrative controls. Here is an example to simplify this; Let’s say an organization has rules regarding how long to store data and when to destroy it. This can be categorized in Administrative, Technical, and Operational controls.

* **Administrative:** *The written policy on how long to keep and when to destroy the data.*
* **Technical:**  *Technology actually keeping and/or destroying data.*
* **Operational:** *The process of destroying data according to policy and using technology.*

After going through all the components within CSF as a team we had decided that most of technical and some operational controls are actually measureable. On the other hand, administrative controls are not measureable since they are written policies and procedures. Our team reviewed all the controls in the CSF for all three domains (User Management, Perimeter Defense, Endpoint Technology) individually, and marked the controls “*YES*” if they are measureable or “*NO*” if they are not. Afterwards, we compared our results and used the Inter-rater Reliability technique to measure the degree of agreement between us.


#### Inter-rater Reliability

We use to use the Inter-Rater Reliability (IRR) measurement as a way to narrow down the number of controls for each domain.  Inter-rater Reliability is “a numerical estimate/measure of the degree of agreement among raters” [5].  It compares the answer each person provides to a given rating against every other person that rated that control.  Then it calculates a percentage of overall agreement based on how many pairs agreed.  For instance, in our case, five people were measuring each control.  For each control, they chose an answer of "Yes, the control is applicable and measurable in this domain" or "No, the control is either not applicable or not measurable in this domain".  An exmaple of such a scenario is shown below.

| Control | Sarah | Lisa | Collin | Lyle | Sanjar |
|---------|-------|------|--------|------|--------|
| ID.AM-1: Physical devices and systems within the organization are inventoriedID.RA-1: Asset vulnerabilities are identified and documented | No | Yes | Yes | Yes | Yes |

To calculate the IRR, the result provided by each person is compared to the result provided by every other person to see how each pair agrees.  To continue the example above, the pair-wise comparison is shown in the table below.

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

The final step of calculating the inter-rater reliability is to add up the number of pairs that agree and divide by the total number of pairs evaluated to give the percent agreement.  In this case, 4 out of 10 pairs agreed, which gives us a 40% agreement on this control.  This process was performed for each control in the CSF framework in each of the three technology domains.

The generally accepted level of agreement is 75% for a minimal agreement with 90% or higher being a high agreement. That is, if the level of agreement is over 75% then the group has agreed upon a specific answer.  The issue we encountered was that if just one of our members disagrees with the rest of the group, that gives us 6 out 10 pairs in agreement and our IRR score becomes 60%.  This would mean that in order for us reach agreement on whether any of the controls are applicable and measurable, it would have to be a unanimous yes vote. This is an issue with using the percent-based statistic. Absolute agreement is unforgiving and with how our rating system was created, a yes/no rating, it is not viable to use adjacent ratings of agreement simply by themselves. Even if adjacent ratings were used, that could lead to meaningless reliability estimates if we simply threw out all controls that had less than a 75% agreement rate.

If we change the minimal level of agreement to 60%, we are able to form conclusions on if the controls are considered relevant and final. If the controls reached 60% (that is, if 4 of the 5 members voted similarly), the control was accepted as either relevant or not relevant. The same result occurred if the vote was unanimous. If the level of agreement did not reach 60%, we used the consensus approach. Using this approach, we evaluated the scores that did not reach the minimal level of agreement and discussed our thought process and concerns about the unused controls to see if everyone had the same ideas of what the definitions of the unused controls were. Some controls were vague in their description which made reaching a level of agreement difficult. To combat this, some controls had their definitions tweaked to a group agreed upon definition which allowed us to rate comfortably.

The outcome of the IRR and consensus approaches provided us with a subset of the overall controls for each of the three classes of technology that we are evaluating.  The control subsets for each are shown below.

##### Identity Management
<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/IDMControls.png">

##### Next Generation Firewalls
<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/PerimeterControls.png">

##### Endpoint Detection and Response
<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/EDRControls.png">

### Scoring Methodology and Outcomes  

Scoring rules measures the accuracy of subjectvie assessment/probabilistic predictions. A score in cybersecurity can be thought of as either a measure of the "calibration" of a set of subjective assessment/probabilistic predictions, or as a "cost function" or "loss function".  For the purposes of this project, we chose to subjective assessment/probablilistic predictions of the maturity model.  Each score, while subjective, is based upon a concrete definition of a scale.  

Each domain is surveyed/scored based upon controls that are applicable to that domain as shown in the IRR section above.  The controls are grouped into categories based upon the NIST CSF.  Then the controls are averaged based upon category and scored on the tool. 

#### Scoring Tool
The tool averages each of categories and compares it to a baseline or another security tool and represents the data in graph form. We still need to define what it is compared against as choosing the best in class will be difficult and not all tools will have a full maturity score, especially for new and emerging technologies.  As the products mature, the maturity baseline should increase.  </br>
<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/bargraph.PNG">
</br>
<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/spidergraph.PNG">
</br>
<img src="https://github.com/sanjar91/INSuRE-notSURE/blob/master/linegraph.PNG">
</br>


## Hinderances
The challenge of this methodology is that the controls that were chosen to be used to evaluate the security tools based upon domain can be subjective to the group that was deciding them.  Another person may chose to evaluate based upon slightly different criteria.  To combat this issue, we use to use the IRR and consensus approach.  With the IRR approach, our hope is that a different group of approximately five people would come to similar levels of consensus that we did and that this would be repeatable.

Introducing the IRR approach did introduce it's own challenges.  As discussed above, the threshold for agreement in the IRR approach is generally considered to be 75%, which is higher than our group of five people is mathematically capable of achieving unless we have 100% agreement.  To reduce the impact of this, we added the consensus approach.  Additionally, we adopted a revised threshold of 60% for the sake of this project as described above.

## Ongoing Risks
|Risk name (value)  | Impact     | Likelihood | Description | Status      | Update      |
|-------------------|------------|------------|-------------|-------------|-------------|
| Resource restrictions (21) | 7 | 3 | Having limited resources can affect the testing phase of new measurements techniques/tools, which could affect the final outcome of this project. | Open | Given that we are halfway through the semester, the likelihood of this happening has decreased. |
|Time restrictions (21) | 7 | 3 | One risk that could arise is running out of time to complete a task setting us back and endangering the completion of the project. | Open | The team has successfully met each deadline and is on track to met future deadlines. |
|Identified measurements are not effective (32) | 8 | 4 | One risk that affects us is that the metrics that we identify for measuring the effectiveness of a cybersecurity program could be ineffective. | Open | No significant change. |
|Identified measurements are too effective (18) | 9 | 2 | One risk that could arise is that the current measurements for effectiveness are very effective leaving our work to be in vain. | Open | No significant change. |
| The methodology is not universal (25) | 5 | 5 | It is possible that the identified methodology cannot be applied evenly to all systems in the evaluated domain.  This has the potential to skew certain aspects of the methodology.| Open | In the process of evaluating control, we learned that many of them were vague and allowed for subjective assessment. |
| Scoring form questions are ambiguous (24) | 6 | 4 | This will not allow for proper answering of the questions due to misunderstanding of the question. This will cause the results to be inaccurate and that will cause the maturity model comparison to be poor. | Open | Newly added. |
| Scoring form questions are biased (30) | 6 | 5 | Having bias in the questions can lead to improper answering of questions which will skew the results. Which will end up ruining the maturity model comparison. | Open | Newly added. |
| Wrong controls were choosen (21) | 7 | 3 | Using IRR and consensus-based approach for choosing there is a chance we left out needed control or left in an unneeded control. | Open | Newly added. |


## References
[1]: NIST Cybersecurity Framework (https://www.nist.gov/cyberframework)

[2]: Cao, Y., & Yang, L. (2010, December). A survey of identity management technology. In 2010 IEEE International Conference on Information Theory and Information Security (pp. 287-293). IEEE.

[3]: Malecki, F. (2012). Next-generation firewalls: Security with performance. Network Security, 2012(12), 19-20.

[4]: Gartner Endpoint Detection and Response Solutions (https://www.gartner.com/reviews/market/endpoint-detection-and-response-solutions)

[5]: Portland Community College. Inter-rater Reliability: Challenges affecting LAC assessment projects. (https://www.pcc.edu/resources/academic/learning-assessment/documents/LACMtg2InterRater_Reliability.pdf)
