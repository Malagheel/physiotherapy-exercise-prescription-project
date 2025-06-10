# UAT & QA Test Plan: Online Exercise Prescription

### 1.0 Objective
To verify that the Online Exercise Prescription feature functions according to the specifications, is free of critical defects, and meets the needs of both physiotherapists and patients.

### 2.0 Scope
* **In Scope:** All functionality related to searching, assigning, modifying, and viewing exercise programs as defined in the Functional Specifications Document. Testing will be performed on modern web browsers (Chrome, Firefox) and mobile devices.
* **Out of Scope:** Testing the patient login/authentication system, patient registration, the underlying server infrastructure, or adding new exercises to the main library.

### 3.0 User Acceptance Testing (UAT) Plan

* **Testers:**
    * 3-4 Physiotherapists from the clinic.
    * 5-8 volunteer Patients with active, non-critical recovery plans.
* **Timeline:** UAT will be conducted over a 2-week period after the feature is deployed to a staging (test) environment.
* **Process:** Testers will be provided with login credentials and a list of scenarios to perform (e.g., "Assign a 3-exercise program to your test patient," "Log in and find the 'Quad Set' exercise your physio assigned you."). A simple feedback form will be provided to log any issues or suggestions. A weekly check-in meeting will be held to discuss findings.

---

### 4.0 Quality Assurance (QA) Test Cases

This is the detailed, internal test script.

| Test Case ID | Feature | Test Steps | Expected Result | Actual Result | Status |
| :--- | :--- | :--- | :--- | :--- | :--- |
| QA-001 | Physio - Search | 1. Log in as a Physio. 2. Navigate to a patient's profile. 3. Go to the "Exercise Prescription" tab. 4. In the search bar, type "Bridge". | A list of exercises containing the word "Bridge" appears. | | Pass/Fail |
| QA-002 | Physio - Search | 1. Follow steps from QA-001. 2. In the search bar, type "qwertyuiop". | The message "No results found" is displayed. | | Pass/Fail |
| QA-003 | Physio - Assign | 1. Follow steps from QA-001. 2. Click "Add" on "Glute Bridge". 3. Enter "3" sets and "12" reps. 4. Click "Save Program". | The "Glute Bridge" exercise appears in the patient's current program with the correct sets/reps. A success message is shown. | | Pass/Fail |
| QA-004 | Patient - View | 1. Log in as the Patient from QA-003. 2. Navigate to "My Exercises". | The "Glute Bridge" exercise is visible with instructions, sets, reps, and a video link. | | Pass/Fail |
| QA-005 | Patient - Video | 1. Follow steps from QA-004. 2. Click the "Watch Video" link for "Glute Bridge". | A video player opens and plays the correct demonstration video. | | Pass/Fail |
| QA-006 | Physio - Modify | 1. Log in as the Physio. 2. Navigate to the patient's program. 3. Change the reps for "Glute Bridge" from "12" to "15". 4. Click "Save Program". | The reps for the exercise are updated to 15. | | Pass/Fail |
| QA-007 | Patient - Data | 1. As the Patient, log out and log back in. 2. Navigate to "My Exercises". | The "Glute Bridge" exercise correctly shows "15" reps. | | Pass/Fail |

---
