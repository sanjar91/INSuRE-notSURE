# Progress Report (March 28, 2019)
## Overview
> (insert brief overview of efforts made)

## Outcomes

To date, we have achieved the following major outcomes in relation to our project.  These outcomes are explained in more detail below, including the methodologies we used and the outcomes of those methodologies.
* Identified the technologies which are being used in the evaluation described below
* Completed initial evaluation of the NIST Cybersecurity Framework (CSF) against the identified technologies
* Used the inter-rater reliability function and a consensus-based approach to identify the specific vulnerabilities which are considered measurable for each identified technology
* Identified measurements for first draft of measurement survey

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

#### Survey Methodology and Outcomes

## Hinderances
> (insert brief discussion of challenges encountered)

## Ongoing Risks
> (address your project risks identified from Milestone 1 and update them based on your current progress, this should be a table)

## References
[1]: NIST Cybersecurity Framework (https://www.nist.gov/cyberframework)

[2]: Cao, Y., & Yang, L. (2010, December). A survey of identity management technology. In 2010 IEEE International Conference on Information Theory and Information Security (pp. 287-293). IEEE.

[3]: Malecki, F. (2012). Next-generation firewalls: Security with performance. Network Security, 2012(12), 19-20.

[4]: Gartner Endpoint Detection and Response Solutions (https://www.gartner.com/reviews/market/endpoint-detection-and-response-solutions)



# Project realization
> The bulk of the project work is centered on realizing the methodology you defined in Milestone 1. Here, you should identify the tasks you have achieved, document the product or other intellectual/applied outcomes that have resulted from your efforts, and bind your tasks to the outcomes and documentation you have produced so far.

>Be productive, work towards completing your process, and document what you do.

>Documentation towards project realization will come in the form an intermediate project report. Your project report should be placed on GitHub in the same repository you used for Milestone 1. Create a new markdown file that contains the following.

```markdown
# Progress Report (insert date here)
## Overview
> (insert brief overview of efforts made)

## Outcomes
> (brief overview of outcomes - what did you achieve?)

> also list them out like this:
> * outcome 1
> * outcome 2

## Hinderances
> (insert brief discussion of challenges encountered)

## Ongoing Risks
> (address your project risks identified from Milestone 1 and update them based on your current progress, this should be a table)

```

> ### Submission materials
>For this submission, you should submit your progress report as a `.md` file in your project GitHub repository

## Diagrams
>In addition to the project documentation, you should produce a set of process or conceptual diagrams suited to your project. >This could be a set of activity diagrams for penetration-testing oriented projects, it could be software architecture diagrams for development-oriented projects, or it could be a process/conceptual model for other projects.

>For more information about different types of diagrams, see:

>Activity diagrams:
>* [http://www.agilemodeling.com/artifacts/activityDiagram.htm](http://www.agilemodeling.com/artifacts/activityDiagram.htm)
>* [http://www.uml-diagrams.org/activity-diagrams.html](http://www.uml-diagrams.org/activity-diagrams.html)

>Process Diagrams:
>* [http://asq.org/learn-about-quality/process-analysis-tools/overview/flowchart.html](http://asq.org/learn-about-quality/process-analysis-tools/overview/flowchart.html)
>* [https://www.rds-london.nihr.ac.uk/RDSLondon/media/RDSContent/files/Research-process-flow-chart_A4_web.pdf](https://www.rds-london.nihr.ac.uk/RDSLondon/media/RDSContent/files/Research-process-flow-chart_A4_web.pdf)

>Conceptual Model:
>* [https://airbrake.io/blog/sdlc/conceptual-model](https://airbrake.io/blog/sdlc/conceptual-model)
>* [http://boxesandarrows.com/conceptual-models-in-a-nutshell/](http://boxesandarrows.com/conceptual-models-in-a-nutshell/)

>### Submission materials
>You should create your diagrams using an architectural tool such as Lucidchart, MS Visio, or similar tools. You should include the diagram in your main project README.md file and in your Progress report in your GitHub repo, as an image and/or link to Lucidchart.
