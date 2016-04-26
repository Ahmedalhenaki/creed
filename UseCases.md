#Use Cases

###Use Case 1
**Title:** Developer commits code to be examined for vulnerabilities

**Primary Actor:** Developer

**Goal in Context:** Gather vulnerability information for all external source code that is used by developers

**Stakeholders:** Developer / Manager

**Preconditions:** Developer is able to check in external source code to vulnerability system. NIST vulnerability database is up to date.

**Main Success Scenario:** Developer checks in code and vulnerability information is recorded to the Risk DB. 

**Failed End Conditions:** Developer is unable to check in code. Checked in code is not checked for vulnerabilities, failing to update Risk DB. 

**Trigger:** Code check in 

<br/>

###Use Case 2
**Title:** Check Project Info Against Policy

**Primary Actor:** Corporate Manager

**Goal in Context:** Check Projects against company policy to locate CVEs and other important factors.

**Stakeholders:** Manager

**Preconditions:** Corporate Manager is able to submit requests to the Policy Database. Policy Database must be up to date and the Project Info should be current.

**Main Success Scenario:** Manager receives a policy report that passes CVEs.

**Failed End Conditions:** Manager does not receive correct info about the project in the policy report.

**Trigger:** Manager puts in the request.

<br/>

###Use Case 3
**Title:** Corporate manager requests to creat manifest and recives a respond.

**Primary Actor:** Corporate manager.

**Goal in Context:** Corporate Manager sends a request to the manifest process and have information on the project and its vulnerbilites.

**Stakeholders:** Corporate manager.

**Preconditions:** Corporate manager does not have full information on the project and manifest file.

**Main Success Scenario:** Corporate manager recives project inforomation and manifest file and information from risk data base.

**Failed End Conditions:** Corporate manager does not recive information and manifest file.

**Trigger:**  Manager puts in the request.
