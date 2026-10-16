# Urban-Scooter-Portfolio
Web and Mobile Testing Project
> 📁**Documentation & Evidence Portfolio:** [Access Google Drive Folder](https://drive.google.com/drive/folders/1yJaGwSv-lekeJWRRGNCIPCVFgioWaYKz?usp=sharing)

## Objective

To test Urban Scooter, a service that allows users to rent electric scooters, by validating its web and mobile applications, API functionality, and key user flows

## Defining the problem

In a scooter rental platform like Urban Scooter, smooth user interactions across web, mobile apps, and backend APIs are vital for user retention. Unvalidated form fields, broken API response codes (e.g., returning 504 instead of 400), or delayed courier push notifications directly degrade the user experience, leading to frustrated customers, failed bookings, and potential revenue loss. 

The application required a comprehensive testing strategy to identify functional defects, validate input boundaries (preventing invalid data entry), ensure cross-platform compatibility, and verify secure API authentication and order creation.

## What I Did

-  Analyzed requirements and Figma designs to understand expected behavior and identify test scenarios.
-  Created mind maps, checklists, and test cases to validate user flows, the interface, and order form fields.
-  Executed functional tests in Chrome and Firefox, including cross-browser testing.
-  Tested mobile notifications and connectivity.
-  Used Postman to test REST API operations, including order creation, authentication, retrieval, and cancellation.
-  Documented functional and input-validation defects in Jira, recording test results and linking bug reports to the relevant tests.

## Technologies Used

Figma · Chrome DevTools · Postman · Jira · Requirements Analysis · Test Case Design · Equivalence Partitioning · Functional Testing · Cross-Browser Testing · Mobile Testing · REST API Testing

## Results 

- Identified and documented 40 bug reports in Jira during requirements analysis and test execution
- Catching input-validation defects early prevented incorrect data persistence in user profiles and rental forms.
- Validated REST endpoints using Postman; uncovered critical API discrepancies (such as a 504 Gateway Timeout returned instead of a 400 Bad Request during authentication failures), highlighting backend error-handling vulnerabilities that required developer attention.
- Verified push notification workflows under specific connectivity conditions, ensuring reliable task assignments for couriers.

## Learnings

- Improved the ability to translate Figma designs and software requirements into structured test cases using Equivalence Partitioning.
- Strengthened end-to-end defect tracking and reporting skills using Jira.

## Test Evidence
[Link to the complete mind map of the “Order” form](https://drive.google.com/file/d/1kFhY5c1sYZJ3bJnGAdRBF3rC8PhjI0vv/view?usp=drive_link)

Demonstrates the comprehensive test coverage for both the "Who is the scooter for?" and "Rental" forms. It maps out design (UI) requirements and functional workflows to identify edge cases and input boundaries.
<br>

- Excerpt from the mind map of the “Rental” form functionality within the order form
<img width="804" height="645" alt="mapa scooter" src="https://github.com/user-attachments/assets/b2f1aa15-2a72-4308-b1fb-09d84ed07d2f" />


<br><br>

**This evidence, the 3 tables below, verifies the expected vs. actual behavior for input fields (character limits, special characters) and courier push notifications under specific connectivity scenarios.**

<br>

Excerpt from the tests created to validate the fields on the “Place an Order” screen
<img width="1090" height="399" alt="imagen" src="https://github.com/user-attachments/assets/1dffa384-414c-4a5f-bb46-bf5144d73c46" />

<br>

Excerpt from the test cases designed to test the courier notification features for order completion and the lack of internet connectivity
<img width="1149" height="420" alt="imagen (1)" src="https://github.com/user-attachments/assets/425cc2b4-2f81-46f7-b9bd-6490f7d20846" />

<br>

Excerpt showing the checklist designed and the API tested against the requirements
<img width="730" height="319" alt="imagen (2)" src="https://github.com/user-attachments/assets/b13bfaf8-72b1-480f-9b82-8536769cf6f8" />



<br>

**Bug report and Postman screenshot as evidence**

<img width="404" height="713" alt="informe_error" src="https://github.com/user-attachments/assets/7bbb2842-c929-4bb0-b2d1-247f41096515" />

<br><br>

<p>- A total of 40 bug reports were identified during requirements analysis</p>
<p>
<img width="1513" height="762" alt="imagen (3)" src="https://github.com/user-attachments/assets/c04bd13f-0713-4b1e-8fd7-d51c59f49d54" />
</p>


