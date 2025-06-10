# Functional Specifications: Online Exercise Prescription

This document details the functional requirements for the Online Exercise Prescription feature.

### 1.0 User Stories

**User Story 1: Assigning an Exercise Program**
* **As a** Physiotherapist,
* **I want to** search an exercise library and add specific exercises to my patient's profile,
* **So that** I can create a customized recovery program quickly and efficiently.

**User Story 2: Viewing an Exercise Program**
* **As a** Patient,
* **I want to** log in to the patient portal and see the exercises my physiotherapist has assigned me,
* **So that** I can follow my program correctly at home and track what I need to do.

**User Story 3: Modifying an Exercise Program**
* **As a** Physiotherapist,
* **I want to** be able to modify the parameters (sets, reps, frequency) of an exercise in a patient's program,
* **So that** I can progress or regress their exercises as their condition changes.

---

### 2.0 Use Cases & Acceptance Criteria (Gherkin Format)

This section defines the specific rules for each user story.

#### **Use Case 2.1: Physiotherapist Assigns a New Exercise**

* **Scenario:** A physiotherapist adds a "Quad Set" exercise to a patient's program.
    * **Given** I am a logged-in Physiotherapist viewing my patient "John Smith's" profile,
    * **And** I navigate to the "Exercise Prescription" tab,
    * **When** I search for "Quad Set" in the exercise library and click "Add",
    * **And** I enter "3" for sets, "10" for reps, and "Hold for 5 seconds" in the instructions,
    * **Then** the "Quad Set" exercise must appear in John Smith's "Current Program" section with the specified parameters.

#### **Use Case 2.2: Patient Views Their Assigned Exercises**

* **Scenario:** A patient logs in to view their program.
    * **Given** I am a logged-in Patient,
    * **When** I click on the "My Exercises" tab in the portal,
    * **Then** I must see a list of all exercises assigned to me.
    * **And** each exercise must clearly display the prescribed sets, reps, and any additional instructions.
    * **And** each exercise must have a clickable video link.

#### **Use Case 2.3: Patient Interacts with Video Link**

* **Scenario:** A patient needs to see how to perform an exercise.
    * **Given** I am viewing my assigned exercise program,
    * **When** I click the "Watch Video" link next to the "Quad Set" exercise,
    * **Then** a video player must open in an overlay or new tab and play the correct demonstration video.

#### **Use Case 2.4: Invalid Search by Physiotherapist**

* **Scenario:** A physiotherapist searches for an exercise that does not exist.
    * **Given** I am a logged-in Physiotherapist in the "Exercise Prescription" tab,
    * **When** I search for an exercise named "Gibberish Exercise",
    * **Then** the system must display the message "No results found. Please check your spelling or add a new exercise to the library."

---
