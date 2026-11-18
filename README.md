# Urban Scooter- Web & Mobile Testing
Web and Mobile Testing Project
> 📁**Documentation & Evidence Portfolio:** [Access Google Drive Folder](https://drive.google.com/drive/folders/1yJaGwSv-lekeJWRRGNCIPCVFgioWaYKz?usp=sharing)

## Objective

To test Urban Scooter, an electric scooter rental platform, by validating its web and mobile applications, API functionality, and core user flows to safeguard revenue, operational continuity, and user retention.

## Defining the problem & Business Impact

In a shared mobility service like Urban Scooter, system reliability directly dictates financial performance and brand reputation:

**User Retention & Revenue:** Broken registration or booking flows cause immediate drop-offs, leading to lost transactions and negative user reviews.

**Operational Efficiency:** Delays or failures in courier push notifications disrupt order fulfillment, resulting in unassigned scooters, delayed service, and inflated support costs.

**System Stability & Costs:** Inadequate input validation and unhandled API errors (e.g., returning 504 Gateway Timeout instead of 400 Bad Request) expose backend infrastructure to unnecessary server load, inaccurate data persistence, and security vulnerabilities.

A rigorous, end-to-end testing strategy was required to uncover functional defects early, validate input boundaries, ensure cross-browser compatibility, and verify secure, predictable REST API behavior.

## What I Did

- **Requirements & Design Analysis:** Analyzed functional specifications and Figma mockups to extract edge cases and business rules prior to execution.

- **Test Design & Architecture:** Modeled complex user flows into structured mind maps, checklists, and comprehensive test cases using Equivalence Partitioning and Boundary Value Analysis.

- **Cross-Platform & Functional Execution:** Performed manual end-to-end testing across Chrome and Firefox DevTools to verify responsive layouts and UI integrity.

- **API Validation:** Utilized Postman to execute REST API tests covering authentication, order placement, vehicle retrieval, and cancellation endpoints.

- **Defect Lifecycle Management:** Logged and tracked 40 detailed bug reports in Jira, documenting precise steps to reproduce, expected vs. actual behavior, and severity levels.

## Technologies Used

Figma · Chrome DevTools · Postman · Jira · Requirements Analysis · Test Case Design · Equivalence Partitioning · Functional Testing · Cross-Browser Testing · Mobile Testing · REST API Testing

## Results & Business Implications

- **40 Defect Reports Identified & Logged in Jira:**
  
  - Business Impact: Uncovered critical functional and UI issues prior to release, preventing user frustration during key conversion funnel steps (sign-up and payment).

- **Prevented Data Corruption via Input-Validation Testing:**
  
    - Business Impact: Catching input boundary failures early ensured clean data persistence in customer profiles, preventing downstream errors in billing and account security.

- **Exposed Backend Error-Handling Discrepancies in REST API (e.g., 504 vs. 400):**
  
    - Business Impact: Identified that authentication failures returned a 504 Gateway Timeout instead of a client-side 400 Bad Request. This mismatch misleads frontend applications, causes unexpected app crashes, and complicates system monitoring for technical teams.

- **Validated Courier Push Notification Delivery Under Unstable Network Conditions:**
  
    - Business Impact: Guaranteed operational continuity by identifying scenarios where field couriers missed task assignments, preventing idle fleet inventory and unfulfilled rental requests.

## Learnings

- Improved the ability to translate Figma designs and business requirements into actionable test suites using Equivalence Partitioning.
- Developed a strong defect management cadence in Jira, prioritizing bug reports based on their risk to core business workflows.
- Strengthened API troubleshooting capabilities by inspecting payload responses and HTTP status codes in Postman to isolate frontend vs. backend failures.

## Strategic Recommendations & Product Decision Support

Based on the testing findings and identified defects, the following actions are recommended for Product Owners and Engineering Leads to optimize system performance and strategic decision-making:

**1. Standardize API HTTP Response Codes (High Priority)**

- Risk Identified: Returning 504 Gateway Timeout when the user makes a mistake (like typing a wrong password) confuses both the user and the system, making it seem like the server crashed when it didn't.
- Product Decision: Developers should update the API to return standard client errors (400 Bad Request or 401 Unauthorized). This helps Product Managers analyze real user login errors accurately in system reports without triggering false alarms about server outages.

**2. Enforce Client-Side Input Validation**

- Risk Identified: Submitting malformed data to the server causes unnecessary API requests and server strain.
- Product Decision: Implement immediate UI-level validation on registration and rental forms. This reduces server infrastructure costs and provides instant, friendly feedback to end-users, lowering support ticket volume.

**3. Implement Push Notification Retry Queue**

- Risk Identified: Couriers in low-connectivity zones miss dispatch notifications, leaving scooters unserviced.
- Product Decision: Operations and development should prioritize an offline message queue with automatic retry logic. This safeguards fulfillment rates and maintains service SLA compliance in high-demand areas.

**4. Automate Core Regression Test Suites**

- Risk Identified: Verifying repetitive manual tests for key flows (like order creation and API status checks) before every release consumes valuable time and slows down testing cycles.
    
- Product Decision: Gradually transition high-priority manual tests into automated Python/PyTest scripts. This speeds up future regression testing cycles and frees QA resources to focus on detailed exploratory testing for new features.

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

<img width="799" height="505" alt="imagen(1)" src="https://github.com/user-attachments/assets/907d6770-bbc4-4b9d-83c5-8905bb0ee01a" />


<br><br>


<p>- A total of 40 bug reports were identified during requirements analysis</p>
<p>
<img width="1513" height="762" alt="imagen (3)" src="https://github.com/user-attachments/assets/c04bd13f-0713-4b1e-8fd7-d51c59f49d54" />
</p>


