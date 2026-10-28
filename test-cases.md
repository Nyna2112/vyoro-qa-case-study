# Vyoro Test Cases

Scope: student portal, project submission and student registration (UI and API). Every case has an ID, a scenario, a precondition, exact steps, the test data used, the expected result, the actual result, a status, and a severity and priority where a bug was found.

## Project submission

### TC_Submission_Of_Project_01
- **Scenario:** Ensuring that there is an option to submit the completed project by the student through their student portal from the track applications section (Happy path)
- **PreCondition:**
  1. Student needs a verified account registered first and then logged in to the student portal
  2. Must be applied and got accepted for at least one project
- **Test steps:** Satisfy the precondition first
  1. Go to Track applications page once logged in from the student account
  2. Select the project which has the status as accepted
  3. Check for a way to submit the project (assuming that the project is completed and ready for submission)
- **Test data:** N/A
- **Expected result:** Should have a button to Submit the project
- **Actual result:** A way to submit the completed project was not found
- **Status:** Fail
- **Severity / Priority:** High / High
- **Comments:** Tested by Neyna, 1 Oct 2026, 8:15 pm (see BUG-001)

### TC_Submission_Of_Project_02
- **Scenario:** Student trying to submit the project without being accepted (Negative path / Alternate flow)
- **PreCondition:**
  1. Student needs a verified account registered first and then logged in to the student portal
  2. Must be applied to a project but has not been accepted yet
- **Test steps:** Satisfy the precondition first
  1. Go to Track applications page once logged in from the student account
  2. Select the project which has the status as pending
  3. Check for a way to submit the project
- **Test data:** N/A
- **Expected result:** Should not have the button to submit the project yet
- **Actual result:** Don't have a button to submit the project yet
- **Status:** Pass
- **Severity / Priority:** Medium / Low
- **Comments:** Tested by Neyna, 2 Oct 2026, 7:25 pm

### TC_Submission_Of_Project_03
- **Scenario:** Student trying to submit the project without completing the project after being accepted (Negative path / Alternate flow)
- **PreCondition:**
  1. Student needs a verified account registered first and then logged in to the student portal
  2. Must be applied to a project and has been accepted
- **Test steps:** Satisfy the precondition first
  1. Go to Track applications page once logged in from the student account
  2. Select the project which has the status as accepted
  3. Check for a way to submit the project (assuming that the project is completed and ready for submission)
- **Test data:** N/A
- **Expected result:** Should not have the button to submit the project yet until the progress of the project is 100% verified by the company
- **Actual result:** Don't have a button to submit the project yet
- **Status:** Pass
- **Severity / Priority:** —
- **Comments:** Tested by Neyna, 2 Oct 2026, 7:25 pm

### TC_Submission_Of_Project_04
- **Scenario:** Student trying to submit the project with no file attached (Negative path / Alternate flow)
- **PreCondition:**
  1. Student needs a verified account registered first and then logged in to the student portal
  2. Must be applied to a project and has been accepted
- **Test steps:** Satisfy the precondition first
  1. Go to Track applications page once logged in from the student account
  2. Select the project which has the status as accepted
  3. Click on the submit project button and don't attach any file to submit and try to click submit (assuming that the project is completed and ready for submission)
- **Test data:** N/A
- **Expected result:** Either the button should not get highlighted until the file is attached or there should be an error message displayed "Please attach the project file"
- **Actual result:** —
- **Status:** —

### TC_Submission_Of_Project_05
- **Scenario:** Student submitting file with the maximum allowed size (Edge case)
- **PreCondition:**
  1. Student needs a verified account registered first and then logged in to the student portal
  2. Must be applied to a project and has been accepted
- **Test steps:** Satisfy the precondition first
  1. Go to Track applications page once logged in from the student account
  2. Select the project which has the status as accepted
  3. Click on the submit project button and attach the file with the maximum allowed size and click submit (assuming that the project is completed and ready for submission)
- **Test data:** [file name and size of the file used]
- **Expected result:** Should take the attached file and submit the project to show it to the company admin in the participants section of the project (whoever posted that project)
- **Actual result:** —
- **Status:** —

### TC_Submission_Of_Project_06
- **Scenario:** Student submitting file with the size greater than the maximum allowed size (Edge case)
- **PreCondition:**
  1. Student needs a verified account registered first and then logged in to the student portal
  2. Must be applied to a project and has been accepted
- **Test steps:** Satisfy the precondition first
  1. Go to Track applications page once logged in from the student account
  2. Select the project which has the status as accepted
  3. Click on the submit project button and attach the file with the size exceeding maximum allowed size and click submit (assuming that the project is completed and ready for submission)
- **Test data:** [file name and size of the file used]
- **Expected result:** Should display a proper error message that "Attached File exceeding the limit" or a better message
- **Actual result:** —
- **Status:** —

## Student registration (UI)

### TC_StudentRegistration_01
- **Scenario:** OTP verification screen after submitting registration details (via Recent graduate registration method)
- **PreCondition:** User has no existing account with this email
- **Test steps:**
  1. Launch the student portal and click on Get started for free on the onboarding screen
  2. Select Recent graduate registration method from the dropdown
  3. Enter Full Name
  4. Enter Email address
  5. Select university from the drop down
  6. Select course/branch from the drop down list
  7. Enter Password
  8. Click on Create account
- **Test data:** Test, test@gmail.com, Kakatiya University, B.Tech Computer Science, [password]
- **Expected result:** It should take the user to a screen to enter the OTP received to the given email while registering
- **Actual result:** Takes to the page where a user needs to enter the otp for the verification process
- **Status:** Pass
- **Comments:** Tested by Neyna, 2 Oct 2026, 8:47 pm

### TC_StudentRegistration_02
- **Scenario:** OTP verification screen after submitting registration details (via University email registration method)
- **PreCondition:** User has no existing account with this email
- **Test steps:**
  1. Launch the student portal and click on Get started for free on the onboarding screen
  2. Select University email registration method from the dropdown
  3. Enter Full Name
  4. Enter university email address
  5. Select university from the drop down
  6. Select course/branch from the drop down list
  7. Enter Password
  8. Click on Create account
- **Test data:** Test, test@ku.com, Kakatiya University, B.Tech Computer Science, [password]
- **Expected result:** It takes the user to the screen where it says that "Your account has been created and waiting for the approval from your university"
- **Actual result:** It takes to the screen where it displays the proper message
- **Status:** Pass

### TC_StudentRegistration_03
- **Scenario:** Account created message after submitting registration details (via College id registration method)
- **PreCondition:** User has no existing account with this id
- **Test steps:**
  1. Launch the student portal and click on Get started for free on the onboarding screen
  2. Select College id registration method from the dropdown
  3. Enter Full Name
  4. Upload the front and back sides of the college id
  5. Select university from the drop down
  6. Select course/branch from the drop down list
  7. Enter Password
  8. Click on Create account
- **Test data:** Test, front.png, back.png, Kakatiya University, B.Tech Computer Science, [password]
- **Expected result:** It takes the user to the screen where it says that "Your account has been created and waiting for the approval from your university"
- **Actual result:** It takes to the screen where it displays the proper message
- **Status:** Pass

### TC_StudentRegistration_04
- **Scenario:** Verifying that it displays a proper error message when the user tries to enter the already registered email via recent graduate registration method (Negative path)
- **PreCondition:** User should have an existing account with this email or refer TC_StudentRegistration_01
- **Test steps:**
  1. Launch the student portal and click on Get started for free on the onboarding screen
  2. Select Recent graduate registration method from the dropdown
  3. Enter Full Name
  4. Enter Email address
  5. Select university from the drop down
  6. Select course/branch from the drop down list
  7. Enter Password
  8. Click on Create account
- **Test data:** Test, test@gmail.com, Kakatiya University, B.Tech Computer Science, [password]
- **Expected result:** It displays the error message that "an account with this email already exists"
- **Actual result:** —
- **Status:** Pass

### TC_StudentRegistration_05
- **Scenario:** Verifying that it handles the mismatch of the allowed file size uploaded for the college id field (Edge case)
- **PreCondition:** User should not have an account with this college id
- **Test steps:**
  1. Launch the student portal and click on Get started for free on the onboarding screen
  2. Select College id registration method from the dropdown
  3. Enter Full Name
  4. Upload the front and back sides of the college id exceeding the allowed file size limit (5 MB)
  5. Select university from the drop down
  6. Select course/branch from the drop down list
  7. Enter Password
  8. Click on Create account
- **Test data:** Test, front.png, back.png, Kakatiya University, B.Tech Computer Science, [password]
- **Expected result:** It handles it by showing the error message "Please upload the file with a maximum size of 5MB"
- **Actual result:** —
- **Status:** —
- **Severity / Priority:** Major S2 / Medium P3
- **Comments:** Tested by Neyna, 5 Oct 2026, 12:31 pm

### TC_StudentRegistration_06
- **Scenario:** Testing the full name field input validation if it's left empty – recent graduate registration method (Negative case)
- **PreCondition:** User should not have an account with this email
- **Test steps:**
  1. Launch the student portal and click on Get started for free on the onboarding screen
  2. Select Recent graduate registration method from the dropdown
  3. Leave Full Name field empty
  4. Enter Email address
  5. Select university from the drop down
  6. Select course/branch from the drop down list
  7. Enter Password
  8. Click on Create account
- **Test data:** (empty name), test6@gmail.com, Kakatiya University, B.Tech Civil, [password]
- **Expected result:** It should display an error message that please enter your full name after clicking on create account or after coming out of that field immediately
- **Actual result:** Error 'Please enter your full name' shown under the Full Name field after clicking Create account.
- **Status:** Pass
- **Comments:** Tested by Neyna, 17 Oct 2026, 10:10 am

## Student registration (API)

### TC_StudentRegistration_API_06
- **Scenario:** Verify the registration API rejects an empty full_name (negative). /registration/6 – register – status code 400
- **PreCondition:** User should not have an account with this email
- **Test steps:** Method: POST, url: [API base URL]/registration/6
- **Test data:** {"full_name": "", "email": "test6@gmail.com", "university": "Kakatiya University", "Course": "B.Tech Civil", "Password": "********"}
- **Expected result:** 400, error on full name field
- **Actual result:** Actual status code: 400
- **Status:** Pass
- **Comments:** Tested by Neyna, 17 Oct 2026, 10:10 am
