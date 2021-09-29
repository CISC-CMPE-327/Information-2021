<h1 align='center'>🍿 Sprint #2 Backend Development 🍿</h1>

<p align='center'>CISC 327  -  Fall 2021</p>


## 💺 Customer Requirement

Continuing from our requirements from the last sprint, the customers have agreed that the system has to provide at least four entities with at least the attributes indicated below: 

- user (email, password, user_name, shipping_address, postal_code, balance)
- product (id - incremental, title, description, price, last_modified_date, owner_email)
- transaction (id - incremental, user_email, product_id, price, date)
- review (id - incremental, user_email, score, review - text)

In this sprint, we will focus on developing and testing the backend logic of the system following the requirements, negotiated by your PM with your customer (us). 
The backend module, which consists of callable functions, should provide the functionalities listed below:

- Register: create a new user in the database
  - R1-1: Both the email and password cannot be empty.
  - R1-2: A user is uniquely identified by his/her email address.
  - R1-3: The email has to follow addr-spec defined in RFC 5322 (see https://en.wikipedia.org/wiki/Email_address for a human-friendly explanation). You can use external libraries/imports.
  - R1-4: Password has to meet the required complexity: minimum length 6, at least one upper case, at least one lower case, and at least one special character.
  - R1-5: User name has to be non-empty, alphanumeric-only, and space allowed only if it is not as the prefix or suffix.
  - R1-6: User name has to be longer than 2 characters and less than 20 characters.
  - R1-7: If the email has been used, the operation failed. 
  - R1-8: Shipping address is empty at the time of registration.
  - R1-9: Postal code is empty at the time of registration.
  - R1-10: Balance should be initialized as 100 at the time of registration. (free $100 dollar signup bonus). 

- Login: 
  - R2-1: A user can log in using her/his email address and the password. 
  - R2-2: The login function should check if the supplied inputs meet the same email/password requirements as above, before checking the database.

- Update user profile:
  - R3-1: A user is only able to update his/her user name, shipping_address, and postal_code.
  - R3-2: Shipping_address should be non-empty, alphanumeric-only, and no special characters such as `!`.
  - R3-3: Postal code has to be a valid Canadian postal code. 
  - R3-4: User name follows the requirements above.

- Create Product:
  - R4-1: The title of the product has to be alphanumeric-only, and space allowed only if it is not as prefix and suffix.
  - R4-2: The title of the product is no longer than 80 characters.
  - R4-3: The description of the product can be arbitrary characters, with a minimum length of 20 characters and a maximum of 2000 characters.
  - R4-4: Description has to be longer than the product's title. 
  - R4-5: Price has to be of range [10, 10000].
  - R4-6: last_modified_date must be after 2021-01-02 and before 2025-01-02.
  - R4-7: owner_email cannot be empty. The owner of the corresponding product must exist in the database.
  - R4-8: A user cannot create products that have the same title.

- Update product:
  - R5-1: One can update all attributes of the product, except owner_email and last_modified_date.
  - R5-2: Price can be only increased but cannot be decreased :) 
  - R5-3: last_modified_date should be updated when the update operation is successful.
  - R5-4: When updating an attribute, one has to make sure that it follows the same requirements as above. 

It is up to you how to define your function signature (required input and expected outputs). 

### 🍱 Step 1 - CI Template

First, the scrum master sets up the project structure and CI pipeline following the template [here](https://github.com/CISC-CMPE-327/Python-CI-2021). 
The scrum master can first test the template locally, then push it to the repo, adjust, and move the models from the last assignment to the repo.
To reduce the scrum master's workload, the scrum master at this point can directly edit/create/delete/push files on the main branch using the web interface or CLI.
But after the sprint started as below, the team is not allowed to do so again. 

Each team member has to understand the template and this document thoroughly. 
The scrum master has no responsibility to explain everything line-by-line. 
The scrum master or any team member should refuse to explain things to other team members if he/she hasn't fully gone through this document or the template.
A team member can only ask questions to the other members about a specific part of this document and the template, but not general/vague questions such as `what should I do?` 

If you choose another language, make sure you have a similar setup to the template, where testings and style checks are conducted automatically for each PR.


### ✈️ Step 2 - Planning

This sprint is then kicked off by a planning meeting, where the scrum master and the team members sit down, 
- Create a new scrum board.
- Create columns (the detailed version but not the simple version).
- Put cards on the backlog. (we have five features so at least 5 cards).
- One possible way of assignments: 2 on login/register/update_profile and 2 on product/update_product. Each of the two members can work on different constraints (e.g. username limit/email format etc.)
- Assign members and reviewers to the cards.
- Assignees move the cards to the todo column


### 🎨 Step 3 - Design

Once the assignee starts working on this assignment, move the corresponding card to the design column.
The team member designs the signature of the functions associated with the card (inputs/outputs) with an empty function body (such as pass/or print). 

### 🚀 Step 4 - Daily-Scrum (Dev+Test)

The team members start implementing the features and testing code to meet the requirement. 
For each constraint/requirement, each team member should implement the testing code first before writing the actual body of the function. 
Each team member then can proceed with implementing the features/constraints and adjust the test case if necessary. 


### ✅ Step 5 - Review/Approve
Once a card is done with the implementation and local testing (on your workstation/laptop), you can proceed to PR, request review, and seek approval for merge. 
When you create a PR, your branch (with the PR) will be automatically tested through CI. Fix any errors before you request any reviews. 


### 📝 Step 6 - Review & Retrospect
Review your PRs again, create tag, and make a submission through onQ.  


## 💺 Rules

All the assignments, starting from this point, will follow these rules:

- No file changes/uploads through the web interface. We can tell.
- No direct change to the master/main branch of your repository. 
- All the changes to the repository have to go through Pull Request (PR).
- All the PRs require reviews and approval before merging. 
- Each PR requires at least 2 reviewers, and each member has to do at least two reviews.
- All the reviews must provide at least one comment (constructive & specific) for improvement. 
- All the team members must have at least a PR for each assignment (sprint).
- All the project activities have to be planned through the scrum board before coding and testing.
- All the cards for each sprint have to go through each column of your team's scrum board (cannot just directly jump from todo to done).
- All the PRs should be associated with at least one card in your scrum board (by mentioning the PR number using `#` in the card)
- All the PRs should follow the agreed PR template.
- All the documentation has to follow the [markdown format](https://guides.github.com/features/mastering-markdown/).
- All the merged code must follow the selected coding style guide. 
- Each of the PR's titles should have emojis. 

Additional rules for this assignment:
- Your main branch's badge has to be build-passing at the time of assignment submission. 


Violation of any of the above rules (except the one about emoji) will result in a grade penalty.
All the team members, through the principle of collective ownership, must ensure other team member's PR/code does not violate any of the rules above.
For any violations that can be tracked down, a penalty will apply for both the reviewers and the related contributors. 

## 💺 Grading:

- Scrum practices (max 2 for the deduction, .25 for each violation, maximum number of violations before deduction 2)
- PR and git practices, including code review (max 3 for the deduction, .25 for each violation, maximum number of violations before deduction 3)
- Code style compliance (max 3 for the deduction, .1 for each style error, the maximum number of violations before deduction 2)
- Documentation and comments - each file/class/method/attribute should have comments. (max 1 for deduction, .1 for each violation)
- Completeness of the data models covering all the above customer requirements (max 1 for the deduction, missing one required entity minus .25)

