Ticket 1: The "Blocker" (ReqRes Auth Issue)

Title: [BLOCKER] ReqRes API returning 401 Unauthorized - Missing x-api-key Header

Priority: High / Blocker

Component: Backend / Mock Services

Description: While verifying the ReqRes mock API for the login flow, a 401 Unauthorized error was discovered. The API now requires a mandatory x-api-key header which is currently missing from our request configurations.

Steps to Reproduce:

Send a GET request to https://reqres.in/api/users/2.

Observe the 401 error response.

Expected Result: 200 OK with User 2 data object.

Actual Result: 401 Unauthorized with message: "The x-api-key header is required for this endpoint."

Suggested Fix: Update environment headers to include a valid x-api-key.

Ticket 2: The "UI Defect" (Broken Image)

Title: [UI/UX] Broken Image Asset on Room Listing Page - room1.jpg

Priority: Medium

Component: Frontend / Assets

Description: The primary image for the "Single" room listing is failing to load on the Restful Booker Platform. This results in a broken image icon, impacting the professional look of the platform.

Steps to Reproduce:

Navigate to the landing page.

Scroll to the room listings section.

Observe the broken image for the first room.

Verify 404 Not Found in DevTools Network tab for .../img/room1.jpg.

Expected Result: Image renders correctly (200 OK).

Actual Result: 404 Not Found.

Ticket 3: Data Validation (ReqRes User Creation)

Title: [LOGIC] Missing Data Validation on POST /api/users

Priority: Low/Medium

Component: API Logic

Description: The user creation endpoint on ReqRes.in does not enforce mandatory fields.

Steps to Reproduce:

Send a POST request to /api/users.

Provide an empty JSON body {}.

Expected Result: 400 Bad Request or validation error message.

Actual Result: 201 Created with a generated id and createdAt timestamp for a null user.

The "Success" Update (Trivia API)

Post this in the #qa-team Slack channel:

Update: Completed contract validation for the Open Trivia Database.

Result: PASS ✅

Details: Verified "Hard" difficulty filter for General Knowledge. API correctly respects the &difficulty=hard parameter and returns valid JSON (Response Code 0).

Note: Content integrity confirmed; questions are appropriately difficult for the "Hard" tag.
