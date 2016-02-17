#Data Flow Diagram Dictionary
Entities:
Corporate Developer - Sends Files and/or Packages to NIST CPE Information Data Storage for processing. Does not get a response back.
Corporate Manager - Requests information on projects in the Risk Database. Receives Project info in response.
National Vulnerability Database - Receives requests for CPE from the NIST CPE Information data storage and responds with CPE Information.

Processes:
Manage Code Streams - Takes Files and/or Packages from Corporate Developers and queries the Package to the NIST CPE Information data storage. CPE Information is sent back with the Package and is sent together to the Risk Database.
Manage CPE Information (Daily Job) - Sends requests to the National Vulnerability Database for CPE. When the National Vulnerability Database responds with CPE Information, it is sent to the NIST CPE Information data storage to be attached to the corresponding Package.
Manage Project Information - Receives project info request from a Coporate Manager then sends a Package Information Request to the Risk Database. Receives a response from the Risk Database then sends the project info back to the Corporate Manager.

Data Storage:
Risk Database - Contains Package and CPE Information for projects for the use of Coporate Managers.
NIST CPE Information - Receives CPE Information from the National Vulnerability Database and pairs them to the Packages provided by the Corporate Developers which are then sent off to the Risk Database.

Data Flows: 
File / Package - Corporate Developers create Files and Packages to be examined for vulnerabilities and attached to CPE Information in a project.
Package Query / CPE information - The query is the name of the package. CPE Info will be tagged to the package name and sent back to the Manage Code Streams process.
CPE File - structured naming scheme for information technology systems, software, and packages frovided by the National Vulnerability Database.
CPE Request/Response - 
Package and CPE Information
Package Information Request/Response - 
Project Info Request/Response - 
