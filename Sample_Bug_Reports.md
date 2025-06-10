# Sample Bug & Incident Reports

This document provides examples of how bugs or incidents would be formally reported in a system like JIRA for the development team to action.

---
### **Bug Report 1**

| | |
| :--- | :--- |
| **Title:** | **[Bug]** Video link for "Glute Bridge" exercise is broken |
| **ID:** | BUG-PT-045 |
| **Reported By:** | Chris (QA Tester) |
| **Priority:** | High |
| **Related Test Case:** | QA-005 |

**Description:**
When a patient clicks the "Watch Video" link for the "Glute Bridge" exercise, they are taken to a 404 "Page Not Found" error instead of the correct demonstration video. All other video links appear to be working.

**Steps to Reproduce:**
1.  Log in as the patient who was assigned the "Glute Bridge" exercise.
2.  Navigate to the "My Exercises" page.
3.  Find the "Glute Bridge" exercise in the list.
4.  Click the "Watch Video" link.

**Expected Result:**
A video player should open and play the demonstration for the "Glute Bridge" exercise.

**Actual Result:**
The browser opens a new tab with a "404 Not Found" error page. The URL points to an incorrect address.

---
### **Bug Report 2**

| | |
| :--- | :--- |
| **Title:** | **[Bug]** System allows negative numbers in the "Reps" and "Sets" fields |
| **ID:** | BUG-PT-046 |
| **Reported By:** | Chris (QA Tester) |
| **Priority:** | Medium |
| **Related Test Case:** | N/A (Exploratory Testing) |

**Description:**
A physiotherapist is able to enter and save negative values (e.g., -5) into the "Sets" and "Reps" fields when assigning an exercise. The system should only accept positive whole numbers.

**Steps to Reproduce:**
1.  Log in as a Physiotherapist.
2.  Navigate to any patient's profile and go to the "Exercise Prescription" tab.
3.  Add any exercise to the program.
4.  In the "Sets" input field, type `-3`.
5.  In the "Reps" input field, type `-10`.
6.  Click "Save Program".

**Expected Result:**
The system should display a validation error message, such as "Invalid input. Please enter a positive number for Sets and Reps." The program should not be saved with negative values.

**Actual Result:**
The system saves the program with the negative values. The patient can see "-3 sets" and "-10 reps" on their exercise plan.

---
