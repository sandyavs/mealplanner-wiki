# Implementation of Social Login Use Case:
## Description:
Add Google and Facebook login support alongside the existing standard login (username/password), allowing users the flexibility to access the Mealplanner application through their preferred login method.

## Use Cases:
- **Use Case ID:** UC-001
- **Use Case Name:** Register Social Login User
- **Actor(s):** Admin
- **Description:** This use case describes the steps an admin takes to regsiter a new/existing user with their mode of social login (Google or Facebook) to the system.
- **Preconditions:** The admin must be logged in to the Mealplanner Admin application.
- **Postconditions:** 
	- A new social login user is registered with their preferred mode of login.
	- The user’s status is set to “Pending” by default to await activation in the Mealplanner application.
	- Admin must change the status to "InActive" when the user leaves the organization (ie., Greener Village).
- **Main Flow: Admin UI**
	1. Admin clicks on "Register User" button.
	2. System displays a form to input user details - name, emailID, role (admin, meal-designer, client), status (active, inactive, pending), modeOfLogin (Google or Facebook).
	3. Admin fills out the form and clicks "Register".
	4. System validates inputs and registers the user to the application with status set to “Pending”.
	5. Admin should have access to edit/delete the social login user anytime.
	7. Admin must provide social login access to only one mode (ie., Google or Facebook)
- **Alternate Flow:**
	- A1: System displays appropriate error messages for missing/invalid inputs.
	- A2: If email already exists in the system, display an error message.
	- A3: If the admin selects more than one mode of login, the system prompts an error: "Only one social login mode can be assigned per user."
- **Notes:** Under Users tab there will be 2 subtabs:
	- Standard Login Users (remains unaffected).
	- Social Login Users (new addition).

- **Use Case ID:** UC-002
- **Use Case Name:** Login with Google
- **Actor(s):** User
- **Description:** This use case describes the steps a user takes to log in to the Mealplanner application using their registered Google account.
- **Preconditions:**
	- The user must be registered by an admin using their Google email address.
	- The user is assigned only one login mode: either Google or Facebook.
	- The new user's initial status in the database is "Pending".
- **Postconditions:**
	- The user successfully logs in to the Mealplanner application using Google authentication.
	- Upon accepting the Terms & Conditions, the new user's status is updated to "Active".
	- Existing users who have already accepted the Terms & Conditions retain their current status.
- **Main Flow - Meal Planner UI:**
	1. User clicks the "Continue with Google" button on the login page.
	2. The system initiates Google OAuth and authenticates the user's email.
	3. The backend verifies if the email exists in the system and if the login mode is set to Google.
	4. If valid, access is granted, and the user is redirected to the "Terms & Conditions" page.
	5. User reads and either accepts or rejects the Terms & Conditions:
		a. If the user rejects, they are redirected back to the login page.
		b. If the user accepts and their current status is "Pending", the system updates their status to "Active".
		c. If the user is already Active, no change to status occurs.
	6. The user is granted access to the Mealplanner application dashboard.
- **Alternate Flow:**
	A1: If the email is not registered or the login mode does not match to Google, display an error: "This email is not authorized for Google login."
- **Notes:**
	1. A registered user can log in only through the assigned login method.
	2. The Terms & Conditions must be accepted to activate the user account firs-time Google login users.

- **Use Case ID:** UC-003
- **Use Case Name:** Login with Facebook
- **Actor(s):** User
- **Description:** This use case describes the steps a user takes to log in to the Mealplanner application using their registered Facebook account.
- **Preconditions:**
	- The user must be registered by an admin using their Facebook linked email address.
	- The user is assigned only one login mode: either Google or Facebook.
	- The new user's initial status in the database is "Pending".
- **Postconditions:**
	- The user successfully logs in to the Mealplanner application using Facebook authentication.
	- Upon accepting the Terms & Conditions, the new user's status is updated to "Active".
	- Existing users who have already accepted the Terms & Conditions retain their current status.
- **Main Flow - Meal Planner UI:**
	1. User clicks the "Continue with Facebook" button on the login page.
	2. The backend verifies if the email exists in the system and if the login mode assigned is set to Facebook.
	3. If valid, access is granted, and the user is redirected to the "Terms & Conditions" page.
	4. User reads and either accepts or rejects the Terms & Conditions:
		a. If the user rejects, they are redirected back to the login page.
		b. If the user accepts and their current status is "Pending", the system updates their status to "Active".
		c. If the user is already Active, no change to status occurs.
	5. The user is granted access to the Mealplanner application.
- **Alternate Flow:**
	A1: If the email is not registered or the login mode does not match to Facebook, display an error: "This email is not authorized for Facebook login."
- **Notes:**
	1. A registered user can log in only through the assigned login method.
	2. The Terms & Conditions must be accepted to activate the user account for firs-time Facebook login users.

