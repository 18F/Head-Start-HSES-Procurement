# Appendix A: Technical details of HSES

The production environment is hosted on the cloud.gov platform providing services for security, user applications, and data exchange. A Secure Sockets Layer (SSL) Gateway is used for System Administration access. HSES is rated FedRAMP Low. 

HSES consists of:
* Languages:
  * Java v1.8
  * HTML5
  * Javascript
  * SQL
  * Bash
* Frameworks
  * Spring Boot v2.2.10
  * Wicket v8.9.0
  * Jquery v3.5.1
  * AWS SDK v1.11.847
  * Apache POI v4.1.2
  iText v2.1.7
* Major Tools
  * Liquibase v3.8.9
  * SpotBugs v4.1.3
  * Jacoco v0.8.5
  * Surefire v3.0.0-M5
  * FailSafe v3
  * OWASP Dependency Check v6.0.2
* Infrastructure	
  * CloudFoundry - Version managed by cloud.gov
  * AWS RDS - Postgres - Version managed by cloud.gov
  * AWS S3 - Version managed by cloud.gov
  * CI/CD Bitbucket Pipelines - Version managed by Bitbucket
  * Git - Version managed by Bitbucket

Upstream dependencies of HSES are:
* GrantSolutions (GS)
* Head Start Aligned Monitoring System (IT-AMS)

Downstream dependencies are:
* GS
* IT-AMS
* Early Childhood Learning & Knowledge Center (ECLKC)
* TTA SmartHub (TTA)

The current infrastructure components are:
* [cloud.gov](https://cloud.gov/) This is a GovCloud-based platform-as-a-service that removes almost all of the infrastructure monitoring and maintenance from the system, is already procured for OHS, and has a [FedRAMP Joint Authorization Board Provisional Authority to Operate (JAB P-ATO)](https://marketplace.fedramp.gov/#/product/18f-cloudgov?sort=productName) on file. FedRAMP is a standardized federal security assessment for cloud services, and the FedRAMP ATO helps agencies by providing confidence in the security of cloud solutions and security assessments. 
* [Bitbucket Pipelines](https://bitbucket.org/product/features/pipelines) This is a CI/CD system. It is used to automate builds, testing, and deployments from Bitbucket.

