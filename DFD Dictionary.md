#Data Flow Diagram Dictionary

##Entities:
```
Corporate Developer - Sends Files and/or Packages to NIST CPE Information Data Storage for processing. Does not get a response back.

Corporate Manager - Requests information on projects in the Risk Database. Receives Project info in response.

National Vulnerability Database - Receives requests for CPE from the NIST CPE Information data storage and responds with CPE Information.
```

##Processes:
```
Manage Code Streams - Takes Files and/or Packages from Corporate Developers and queries the Package to the NIST CPE Information data storage. 

Combine Package and CPE Info - Receives the CPE Info from NIST Database and sends the Package and CPE Info to the developer and to the Risk Database.

Manage CPE Information (Daily Job) - Sends requests to the National Vulnerability Database for CPE. When the National Vulnerability Database responds with CPE Information, it is sent to the NIST CPE Information data storage to be attached to the corresponding Package.

Manage Project Information - Receives project info request from a Coporate Manager then sends a Package Information Request to the Risk Database. Receives a response from the Risk Database then sends the project info back to the Corporate Manager.

Create Manifest - Corporate Manager requests a manifest to be made at the end of every stage of the project. This queries the Risk Database and sends it the manifest back to the Manager.

Check Against Policy - Managers request a policy report on a project, it is checked against the policies listed in the Policy Database and a report is made, this would contain any CVEs and other useful info and is sent back to the manager.

```

##Data Storage:
```
Risk Database - Contains Package and CPE Information for projects for the use of Coporate Managers.

NIST CPE Information - Receives CPE Information from the National Vulnerability Database and pairs them to the Packages provided by the Corporate Developers which are then sent off to the Risk Database.

Policy Database - Contains the policies for the company and is used to check project info and create policy reports on those projects.
```

##Data Flows: 
```
File / Package - Corporate Developers create Files and Packages to be examined for vulnerabilities and attached to CPE Information in a project.

Package Query / CPE information - The query is the name of the package. CPE Info will be tagged to the package name and sent back to the Manage Code Streams process.

CPE File - structured naming scheme for information technology systems, software, and packages frovided by the National Vulnerability Database.

CPE Request/Response - A query asking for CPE info and the returned CPE info

Package and CPE Information - Packages sent by developers are paired with the CPE info from the NIST CPE Info Database.

Manifest - a form that records thehistory and actions that occur to and in a project.

Creation Request - Corp. Managers request a manifest to be created when altering a project.

Project Info Query - The Create Manifest process queries for project info from the Risk Database.

Request Policy Report - Corporate Managers request policy reports from the Policy Database.

Policy Reports - Policy reports are made when a corporate manager sends a request. It checks the project information against the policy in the database and reports any CVEs and other important info to pay attention to.

Project Info Request/Response - A process requests info from the risk Database and is returned when found.
```
