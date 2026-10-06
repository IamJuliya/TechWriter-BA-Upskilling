# Functional Requirements Document (FRD)

## Project
**Project Opportunities & Talent Readiness Enhancement**

## 1. Purpose

This FRD defines the functional requirements for the enhanced employee management process shown in the TO-BE process flow. The enhancement helps Project Managers publish upcoming project opportunities, enables employees to evaluate opportunities against their skills and readiness, and enables Resource Managers to review and shortlist suitable internal talent. Learning & Development supports skill-gap closure through tailored learning and assessment.

The solution supports staffing decisions but does not automatically allocate employees.

## 2. Scope of the Changed Process

The changed process covers:

- Project opportunity creation and publication
- Definition of mandatory and preferred skills
- Employee discovery and skill comparison
- Skill-gap identification
- Employee interest and withdrawal
- Employee availability and readiness updates
- Resource Manager review and shortlisting
- Waitlist handling for employees who are not ready by the required date
- Learning & Development support for skill-gap closure
- Tailored course enrollment, completion, assessment, retry, and certification
- Skill-profile update after certification
- Selection confirmation, opportunity closure, and outcome notification
- Management dashboards for talent availability, staffing, and training information

## 3. Actors

| Actor | Responsibility |
|---|---|
| Project Manager (PM) | Creates, defines, publishes, and updates project opportunities |
| Employee | Views eligible projects, compares skills, identifies gaps, expresses/withdraws interest, and updates readiness |
| Resource Manager (RM) | Reviews interested employees, evaluates suitability/readiness, shortlists candidates, and confirms selection |
| Learning & Development (L&D) | Uses skill-gap information to provide tailored learning, assessment, certification, and training plans |
| Management | Uses dashboards to monitor talent availability, staffing, and training information |

## 4. Functional Requirements

### Project Opportunity Management

**FR-01 – Create Project Opportunity**  
The system shall allow an authorized Project Manager to create a project opportunity with project role, dates, and other mandatory project information.

**FR-02 – Define Required Skills**  
The system shall allow the Project Manager to define mandatory and preferred skills for a project opportunity.

**FR-03 – Publish Project Opportunity**  
The system shall allow an authorized Project Manager to publish an opportunity with a closing date. The system shall prevent publication when mandatory information is missing.

**FR-04 – Update Project Requirements or Dates**  
The system shall allow an authorized Project Manager to update project requirements or start dates for an active opportunity. Affected employees shall be notified when such changes require them to re-check their interest or readiness.

**FR-05 – Close Project Opportunity**  
The system shall allow the authorized Resource Manager to close an opportunity after the selection outcome is confirmed.

### Employee Opportunity and Interest Management

**FR-06 – View Eligible Projects**  
The system shall allow employees to view upcoming project opportunities for which they are eligible or potentially suitable.

**FR-07 – Compare Skills**  
The system shall display the employee's recorded skills against the project's mandatory and preferred skills.

**FR-08 – Identify Skill Gaps**  
The system shall identify and display skill gaps between the employee profile and project requirements.

**FR-09 – Express Interest with Available Date**  
The system shall allow an employee to express interest in an opportunity and provide their available date.

**FR-10 – Withdraw Interest**  
The system shall allow an employee to withdraw previously expressed interest while the opportunity is still active.

**FR-11 – Update Readiness**  
The system shall allow an employee to update readiness information relevant to the project opportunity.

### Resource Manager Review and Staffing

**FR-12 – View Interested Employees**  
The system shall allow an authorized Resource Manager to view employees who have expressed interest in an opportunity.

**FR-13 – Review Candidate Information**  
The system shall display relevant skills, experience, availability, and readiness information to support the Resource Manager's review.

**FR-14 – Record Suitability and Readiness Decisions**  
The system shall allow the Resource Manager to record whether an interested employee is suitable and whether the employee is ready by the required date.

**FR-15 – Manage Shortlist and Waitlist**  
The system shall allow the Resource Manager to shortlist suitable and ready employees and place suitable but not-yet-ready employees on a waitlist with a reason where applicable.

**FR-16 – Support Unfilled Opportunity Handling**  
The system shall allow the Resource Manager to identify opportunities that remain unfilled after internal review and record a decision to consider external hiring.

**FR-17 – Confirm Selection and Allocate Resource**  
The system shall allow the Resource Manager to confirm the selected employee and record the staffing outcome. The system shall not automatically allocate an employee without authorized confirmation.

### Learning & Development

**FR-18 – Use Skill-Gap Information**  
The system shall provide relevant skill-gap information to Learning & Development for employees who need additional skills for an opportunity.

**FR-19 – Enroll Employee in Tailored Course**  
The system shall allow Learning & Development to enroll an employee in a tailored course based on identified skill gaps.

**FR-20 – Record Course Completion and Assessment**  
The system shall allow L&D to record course completion and assessment results.

**FR-21 – Manage Assessment Retry**  
The system shall support assessment retries up to the configured maximum number of attempts. Employees who reach the maximum attempts without passing shall be returned to the talent pool or handled according to the defined business process.

**FR-22 – Certify and Update Skill Profile**  
The system shall allow L&D to record certification for a successfully assessed employee and update the employee's skill profile accordingly.

**FR-23 – Plan Training from Skill-Gap Data**  
The system shall allow L&D to use aggregated skill-gap information to plan future training activities.

### Notifications and Reporting

**FR-24 – Notify Affected Users**  
The system shall notify relevant employees of important project changes, selection outcomes, and other defined process events.

**FR-25 – Management Dashboards**  
The system shall provide management views of talent availability, staffing status, and training information based on data from PM, RM, Employee, and L&D activities.

## 5. Business Rules

- Only authorized Project Managers can create and publish project opportunities.
- Mandatory skills must be defined before an opportunity can be published.
- Employees can express interest only while the opportunity is active and before its closing date.
- An employee should not be able to submit duplicate interest for the same opportunity.
- Employees may withdraw interest while the opportunity is active, subject to the defined business process.
- A project opportunity with a passed closing date should not accept new expressions of interest.
- Skill comparison is based on the employee's recorded skill profile and the project's mandatory/preferred skills.
- Suitability and staffing decisions remain with the authorized Resource Manager.
- Automatic project allocation is outside the scope of this enhancement.
- External hiring is considered only when the internal process does not produce a suitable/ready resource, according to management policy.
- Assessment retry limits are configurable.
- Skill-profile updates following certification require an authorized L&D action.

## 6. Key Exceptions and Edge Cases

- Project cannot be published if mandatory project or skill information is missing.
- Employee attempts to express interest after the closing date.
- Employee attempts to submit duplicate interest.
- Project start date or requirements change after an employee has expressed interest.
- Employee withdraws interest before the RM review is completed.
- Employee is suitable but not ready by the required date.
- Tailored assessment is failed and retry limit is reached.
- No suitable internal employee is available and the opportunity remains unfilled.

## 7. Out of Scope

- Automatic project allocation without RM confirmation
- Recruitment processing and candidate hiring workflow
- Salary or compensation decisions
- Performance appraisal
- Automatic training assignment without L&D involvement
- Full workforce management or capacity planning
