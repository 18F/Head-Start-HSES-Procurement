# Initial HSES Cost RFI

| Date | Description | 
|----------|-------|
| 10/14/2021 | RFI is opened for vendor responses |
| 10/26/2021 | 12pm EDT - [responses due from vendors in this Google form](https://docs.google.com/forms/d/e/1FAIpQLSdS5FCiLwibwZyjapR5LS0XPGk-Y8aK_Uq1EqISwG9smDbDyQ/viewform) |

[The RFI questions are available for your review](./rfi-questions.md) before submitting your responses.

## Executive Summary
The Head Start Enterprise System (HSES) is the primary data management system of the Office of Head Start (OHS). The project's purpose is to continuously improve management and oversight of grantee organizations and program operations at the local, state, regional and national levels through growth and enhancements in the HSES system; and to provide leadership within the Administration with near real-time, multi-level reports as needed. HSES is also used to continuously improve OHS' ability to conduct fiscal management and program operations through a system that reflects an expert understanding of the macro and micro work of the OHS. HSES, in conjunction with the GrantSolutions grant award system, provides OHS with the ability to manage funds, performance, and to inform Congress on the operation and management of over $9 billion in federal funds for 4,000 annual grant awards. 

18F, in collaboration with Office of Head Start (OHS), have envisioned what is needed from a vendor team to maintain operations and modernize HSES through agile and user centered methodologies. The team makeup, standards, and practices will allow OHS and vendor team(s) to have the flexibility needed to:
* Design and develop for evolving user needs
* Answer emerging requests from legislation
* Respond to disasters or other emergencies
* Maintain the system’s interoperability, sustainability, and ability to transition to new vendor teams in the future. 

We do not expect this effort to be a wholesale replacement of our existing system, but anticipate ongoing maintenance and feature work to evolve and modernize HSES.

## Focus Area 1: System Availability and Resilience

OHS relies on HSES for all aspects of its work; including rapid disbursement of funds and ongoing oversight of all Head Start grantees. HSES launched in 2008 and has grown into a [large system with a complex codebase](./appendix_a.md) reflective of its size and age. In order to illustrate the relative size of HSES and scale of work required to maintain and modernize it, the table below shows metrics of HSES in use at OHS today.

| Metric | HSES application code[^1] |
|------ | ----- |
| Lines of code | 1,021,413 |
| Classes | 6,117 |
| Functions | 73,842 |
| Cyclomatic Complexity[^2] | 172,430 |
| Tech Debt[^3] | 5,242 days |

### Needs for system availability and resilience:

With this amount of complexity, the existing code base needs to be maintained and upgraded when there are small fixes, emergent bugs, and library upgrades to perform. We do not anticipate that this will include large feature work, but it will require generalist skills and big-picture vision.

This work will help identify and design opportunities for smaller wins (band-aid solutions). We expect that, as situations present themselves, the work will include refactoring code to better align the application with the future-facing opportunities.

[Current HSES technical and architectural details](./appendix_a.md)

## Focus Area 2: Security and Compliance

HSES needs to meet all current HHS security requirements, including a continuous Authority to Operate (ATO). OHS expects ATO security controls to align with the system categorization and control selection as part of the ACF Governance Framework, which will be tailored toward an agile practice. The contractor is expected to use best practices for security in delivering code.

### Background details:

The production environment is hosted on the cloud.gov platform providing services for security, user applications, and data exchange. A Secure Sockets Layer (SSL) Gateway is used for System Administration access. HSES is rated FedRAMP Low.

### Needs for security and compliance:

The contractor must have both strategic and tactical security and compliance ability and knowledge. The FedRAMP Low rating and the use of cloud.gov lowers the compliance burden. However, ongoing attention is needed to maintain compliance, infrastructure, and security best practices. This will include developing an internal vendor security and compliance awareness program, performing routine audits on the system to determine weaknesses, and regular system hardening.

## Focus Area 3: Interoperability

Moving forward, OHS would like all of its systems to engage in seamless data exchange. The design and implementation of a consistent, understandable API will aid the efforts of the greater OHS agency.

### Background details:

HSES interfaces with four government systems:
* Early Childhood Learning & Knowledge Center (ECLKC)
* IT Aligned Monitoring System (ITAMS)
* TTA Hub
* Grant Solutions (NOT under the ownership of OHS)

HSES pulls data from three government systems to support federal oversight of grantees:
* Federal Audit Clearinghouse
* SAM.gov
* Payment Management System

### Needs for interoperability:

The connections between some of these systems are fragile and require ongoing attention and maintenance to ensure consistent data connections throughout. This requires cooperation with other systems, meeting regularly with other system owners, and working to build more cohesive interoperability.  

## Focus Area 4: Planned Feature Work in a Future-facing System

### Background details:

Historically, OHS has not made user research and experience of the system a priority for development. While a lot of work can be accomplished in HSES, users find their workflows through the system inefficient and unintuitive. Users have developed workarounds that pull work out of the system. Much of the data entry is manual. Additionally, users report that data insights are difficult to visualize or find.

There is also a large backlog of feature-level work that touches many different components. Many of these represent a high level of effort.

| Priority Level | Number of tickets[^4] | 
|----------|-------|
| Critical | 5 |
| Major | 67 |
| High | 6 |
| Medium | 44 |
| Low | 3 |
| Minor | 5 |

### Needs of planned feature work in a future-facing system:

This work needs more than code alone; it also needs designers and product experts to learn more about the problems and the users to ensure that the end result is intuitive, easy to use, and efficiently solves real-world problems. This will require core agile, user-centered principles and practices to identify, design, build, and test new work that will remove problems and improve the user experience of HSES. We envision this will require multi-team coordination and knowledge in HSES and the workings of OHS that will be developed throughout the transition process.

## Focus Area 5: Emergent Work in a Future-facing System 

OHS is, by nature, an agency which adapts in real time to Congressional priorities and mandates. Just-in-time enhancements are vital to achieving agency goals. Currently, there are issues balancing those emergent and existing priorities that have led to halted or delayed feature work.

### Background Details:

In the past year, OHS has been awarded supplementary money from the American Rescue Plan to disburse to grantees. The HSES system had to very quickly:
* Stand up new grants for every child serving grantee
* Design, develop and implement a new grant application process
* Restructure permissions so that the new process could be done efficiently. 

While OHS has learned from previous emergent issues, this sort of mandate is, by nature, unpredictable and often has to happen very quickly. 

### Needs of emergent work in a future-facing system:

As Congressional priorities and mandates roll out, OHS will require rapid development in certain priority areas. This work will not undergo the full agile process of engaging users in advance, but will still use core agile principles of determining minimum viable value and working in small steps to complete work in a way that still centers user experience.

This team will also find opportunities for necessary but non-urgent work that it can work on during slack times that will enhance the system but can be put aside for emergent work.

## Focus Area 6: Data Insights

### Background Details:

OHS has reporting needs that are Congressionally mandated; but they would like to be able to better structure their data and reporting so that they can extract patterns to better serve grantees. Better data collection techniques,  processes, and visualizations could allow OHS to unearth inequities, identify at-risk grantees, and help set grantees up for greater success by mapping long-run distribution patterns.

### Needs for data insights:

OHS would like to develop and maintain a deep understanding of the data sets that currently exist within the system. This will require research and supporting technical efforts to determine what data opportunities exist and the type of reporting and data visualizations that will allow OHS to better implement their goals.

## Focus Area 7: Coordination 

HSES is a large system. While the OHS Product Owner (PO) will be embedded in some agile rituals and be involved in the development process, it is necessary to coordinate the day-to-day work in and across different focus areas. This will allow for the work to meet OHS’s long-term goals and be prioritized by the PO. 

### Needs for coordination:

OHS needs development, product, and user experience work to be coordinated across the multiple teams so that:
* High level goals are established and carried out across all focus area teams
* The problems being solved are the right problems
* The features being built are the right features
* The system is being built in an extendible and flexible way
* The PO has enough information to make credible and informed decisions for the health and well-being of the system.

Federal grants management experience will help with coordinating efforts that align with OHS’s long-term goals.

## Focus Area 8: Help Desk

HSES is a large and complex system, and requires a fully-staffed help desk to provide tiered, multi-modal support services for the system’s active user base.

### Needs for help desk:

The help desk is the first line of contact for HSES users who are experiencing problems or are new to the system. They will respond to calls and emails, triage issues, assist users with straightforward problems and escalate all other problems to the development team. This help desk coordinates with development teams to ensure timely resolution of all problems and gives users insight into the status of their problem. Additionally, the help desk staff will need to include some Spanish language coverage for regular support hours.

## Focus Area 9: Documentation and Communications

### Background Details:

Clear, usable, and actionable documentation for both internal and external audiences is a key component of any complex system like HSES. Additionally, there are periodic OHS policy communications and system announcements sent via HSES that require copywriting, editing, and distribution. 

### Needs for documentation and communications:

Having a collaborative plan for creating, updating, and assessing documentation is an important part of this work, and empowers the OHS team. Specific documentation and communication types may include:
* Process documentation, written in plain language, following a logical step-by-step flow from the perspective of a learner/end user, assessed by periodic user testing. 
* Screenshots, screencasts, or videos for the specific documentation, as deemed appropriate. 
* Formal notices from OHS about the system or related reporting requirements.
* System overviews/guides or knowledge base articles, as needed.

[^1]: Static code analysis performed locally using the [SonarQube](https://www.sonarqube.org/) tool on HSES code from April 2021. Codebase has been worked on continuously since then.

[^2]: The [calculated number](https://docs.sonarqube.org/latest/user-guide/metric-definitions/) of linearly independent paths through a program’s source code.

[^3]: A (very rough) [estimate](https://docs.sonarqube.org/latest/user-guide/concepts/) of the amount of developer time it would require to fix all Maintainability Issues / potential code problems that were discovered in the system.

[^4]:  Source: A recent spreadsheet of open Jira tickets

## Responses to this RFI are due 10/26/2021 by 12pm EDT

[The RFI questions are available for your review](./rfi-questions.md) before submitting your responses.

Please use [this Google form to submit your responses.](https://docs.google.com/forms/d/e/1FAIpQLSdS5FCiLwibwZyjapR5LS0XPGk-Y8aK_Uq1EqISwG9smDbDyQ/viewform)
