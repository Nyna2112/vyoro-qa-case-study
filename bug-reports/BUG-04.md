# BUG-004: Group chat option not working properly as per the functionality (should not be deleted but should show you are no longer a participant)

| Field | Detail |
|---|---|
| Severity | Medium |
| Priority | Low |
| Status | In progress |
| Environment | A few student and company accounts were created and the student application was accepted via company's account to test |
| Found by | Neyna Gunti |


## Requirement analysis
The users should have access to the group chat even if they finished their project.

## Test planning
Testing should be done on the group chat feature by exploratory, functional, manual, blackbox testing, userflow testing in order to see whether the user has access to the chat or not because it sometimes acts like a proof for the user or as a resource to attach any documents in that chat for applying to a job/project.

## Scenario
Group chat should not be deleted after the completion of the project – student portal

## Steps to reproduce
Same precondition as BUG-001 to BUG-003.

1. Go to student portal
2. Login via a student account
3. Go to projects section
4. Apply for a project
5. Go to track applications section
6. View the details of the project
7. Go to group chat option
8. Check for any resources and ask for any doubts there
9. Complete the project and submit it
10. Check if the chat is visible or not after the completion and successful verification of the project

## Expected result
Able to view the chat messages.

## Actual result
Not able to view it after completion.

## Severity and priority
- Severity: Medium because losing access to a chat that may contain deliverables or proof of collaboration removes something the student could reasonably expect to keep.
- Priority: Low because students are still able to complete the project and submit it and get verified.

## Observed behaviour
The chat becomes inaccessible from the student's view after project completion. It is not confirmed whether the chat data is deleted on the backend or only hidden from the UI. This needs backend/database confirmation from the development team.

## Test execution
Found the bug while testing the entire flow from application to completion of the project.

## Test closure
- Reported it to the developer 


