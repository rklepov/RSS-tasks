## Sprint 2: Login, Registration, and Main Pages Implementation

In the second sprint, the team will focus on implementing the login, registration and main pages, including input validation, integration with an authentication service, managing user authentication state, saving the authentication token, providing buttons to navigate between the login and registration pages, and implementing routing for proper navigation. The team's progress will be evaluated through a cross-check process, where other students will assign points based on achieving specific goals and milestones. The mentor will also evaluate the team's progress using separate evaluation criteria.

### Working with the Repository

- Create a new branch for the current sprint (e.g., `feat/sprint_2`) from the previous sprint's branch (`develop`).
- Merge all feature branches into the current sprint's branch.
- At the end of the sprint, create a pull request from the current sprint's branch (`feat/sprint_2`) to the previous sprint's branch (`develop`).
- Share the pull request link with the mentor for review and evaluation.

### CrossCheck Criteria (260 points):

### Login Page Implementation (90 points - Total)

#### Requirements

#### 1. Input Validation (30 points)

- **(20 points)** Implement client-side validation for the login form, including email and password fields. [RSS-ECOMM-2_01](./Sprint2/RSS-ECOMM-2_01.md)
- **(10 points)** Display clear error messages indicating any validation issues, such as an improperly formatted email. [RSS-ECOMM-2_02](./Sprint2/RSS-ECOMM-2_02.md)

#### 2. Integration with Authentication Service (25 points)

- **(15 points)** Integrate the login form with a chosen authentication service (CommerceTools) to handle user authentication. [RSS-ECOMM-2_03](./Sprint2/RSS-ECOMM-2_03.md)
- **(10 points)** Implement error handling for failed authentication attempts, such as incorrect email or password, and display user-friendly error messages. [RSS-ECOMM-2_04](./Sprint2/RSS-ECOMM-2_04.md)

#### 3. State Management and Redirection (20 points)

- **(10 points)** Redirect users to the application's main page upon successful login. [RSS-ECOMM-2_05](./Sprint2/RSS-ECOMM-2_05.md)
- **(10 points)** Redirect users who are already logged in to the main page if they try to access the login page. [RSS-ECOMM-2_06](./Sprint2/RSS-ECOMM-2_06.md)

#### 4. Handle Authentication Token (10 points)

- **(10 points)** Obtain the authentication token securely after a successful login attempt by sending a request to the token endpoint (e.g., https://auth.europe-west1.gcp.commercetools.com/oauth/project_key/customers/token), allowing for seamless user authentication across the application. [RSS-ECOMM-2_07](./Sprint2/RSS-ECOMM-2_07.md)

#### 5. Navigation to Registration Page (5 points)

- **(5 points)** Add a button or link on the login page that allows users to navigate to the registration page. [RSS-ECOMM-2_08](./Sprint2/RSS-ECOMM-2_08.md)

### Registration Page Implementation (100 points - Total)

#### Requirements

##### 1. Input Validation (30 points)

- **(20 points)** Implement client-side validation for all required fields in the registration form, such as email, password, first name, last name, date of birth, and address fields (e.g., street, city, postal code, and country) for proper use with CommerceTools. [RSS-ECOMM-2_09](./Sprint2/RSS-ECOMM-2_09.md)
- **(10 points)** Display clear error messages indicating any validation issues, such as an improperly formatted email or a weak password. [RSS-ECOMM-2_10](./Sprint2/RSS-ECOMM-2_10.md)

##### 2. Integration with Authentication Service (20 points)

- **(10 points)** Integrate the registration form with a chosen authentication service, such as commercetools, to handle user registration. [RSS-ECOMM-2_11](./Sprint2/RSS-ECOMM-2_11.md)
- **(10 points)** Implement error handling for failed registration attempts, and display user-friendly error messages. [RSS-ECOMM-2_12](./Sprint2/RSS-ECOMM-2_12.md)

##### 3. State Management, Automatic Login, and Redirection (15 points)

- **(15 points)** Redirect users to the application's main page upon successful account creation and automatic login. [RSS-ECOMM-2_13](./Sprint2/RSS-ECOMM-2_13.md)

##### 4. Integration with commercetools (or alternative) for User Profiles and Addresses (30 points)

- **(15 points)** Allow users to set a default address during registration. [RSS-ECOMM-2_14](./Sprint2/RSS-ECOMM-2_14.md)
- **(15 points)** Enable users to select different billing and shipping addresses or choose a single address for both billing and shipping during the registration process. [RSS-ECOMM-2_15](./Sprint2/RSS-ECOMM-2_15.md)

##### 5. Navigation to Login Page (5 points)

- **(5 points)** Add a button or link on the registration page that allows users to navigate to the login page. [RSS-ECOMM-2_16](./Sprint2/RSS-ECOMM-2_16.md)

### Main Page Enhancements (20 points - Total)

#### Centralized Navigation (20 points)

- **(10 points)** Add links to all the functional pages of the application on the main page. These should include, but are not limited to, the login and registration pages. [RSS-ECOMM-2_17](./Sprint2/RSS-ECOMM-2_17.md)
- **(10 points)** Each link should redirect the user correctly to the corresponding page without any errors. [RSS-ECOMM-2_18](./Sprint2/RSS-ECOMM-2_18.md)

### Routing Implementation (30 points - Total)

- **(15 points)** Implement routing for navigation between login, registration, and main pages. [RSS-ECOMM-2_19](./Sprint2/RSS-ECOMM-2_19.md)
- **(15 points)** Implement a 404 (Not Found) page for invalid route requests. [RSS-ECOMM-2_20](./Sprint2/RSS-ECOMM-2_20.md)

### Evaluation Criteria for Header (20 points - Total)

- **(10 points)** Navigation to login and registration pages for unauthorized users [RSS-ECOMM-2_21](./Sprint2/RSS-ECOMM-2_21.md)
- **(5 points)** Ability to access the main page for all users [RSS-ECOMM-22](./Sprint2/RSS-ECOMM-22.md)
- **(5 points)** Logout functionality for authorized users [RSS-ECOMM-2_23](./Sprint2/RSS-ECOMM-2_23.md)

### Mentor Evaluation Criteria (60 points - Total):

1. **Code Review Participation (10 points):** Students actively participate in code reviews, providing constructive feedback and suggestions to their peers.
2. **No Merges Without Approvals (10 points):** Pull requests are not merged without approvals from other team members, ensuring the quality of code contributions.
3. **Pull Request Descriptions (10 points):** Pull requests include detailed descriptions, outlining the changes made and the purpose of the changes, facilitating better understanding and review.
4. **Task Board Management (10 points):** Students maintain and regularly update a task board (e.g., Trello, Jira), ensuring that tasks are moved according to their progress and completion.
5. **Active Participation in Development Discussions (5 points):** Students take an active role in discussing the development process, sharing ideas, and collaborating on solutions and improvements.
6. **Unit Test Coverage (15 points):** The codebase has a minimum of 25% unit test coverage, ensuring the reliability and robustness of the implemented features.

### Useful Links and Resources

1. [Get started with the TypeScript SDK](https://docs.commercetools.com/sdk/js-sdk-getting-started)
2. [AuthMiddleware](https://docs.commercetools.com/sdk/js-sdk-middleware#authmiddleware)
3. [commercetools-sunrise-data](https://github.com/commercetools/commercetools-sunrise-data)

### Here is the final points distribution:

- Login Page Implementation: 90 points
- Registration Page Implementation: 100 points
- Main Page Implementation: 20 points
- Routing Implementation: 30 points
- Header Implementation: 20 points
- Mentor Evaluation Criteria: 60 points
- Total points for Sprint 2: 320 points
