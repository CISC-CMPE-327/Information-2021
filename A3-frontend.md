<h1 align='center'>🍿 Sprint #3 Front-end Prototyping 🍿</h1>

<p align='center'>CISC 327  -  Fall 2021</p>


## 💺 Customer Requirement

Continuing our requirements from the last sprint, now you have the backend models up running. 
In this sprint, we will prototype frontends for the customers to try.
The purpose of this sprint is to build a front-end prototype that is directly connected with your tested backend.
The demo prototype should contain:

- user login page
- user registration page
- user profile update page
- user home page (with links to the pages below)
  - product creation page
  - product update page

The customer does not have additional requirements at the moment.
Detailed specifications with constraints will be provided in the next sprint after the customer tried out the prototype. 

**Therefore, there is no need for extensive frontend testing or backend testing. 🔥**

The team is only required to provide a runnable demo (aka manual smoke test - run it and put out fires if any 🚒 )

**Again, each team member should read thoroughly the instruction and the provided template.**


### 🍱 Step 1 - Frontend Options

For this project, you have the following two options for frontend prototyping:

- [We Interface](https://github.com/CISC-CMPE-327/Python-CI-2021/tree/option_web) (later tested with selenium)
  -  MVC design - Testing will be done by auto-clicking the webpage and checking the presence of elements/text.
  - [Summary of files changes](https://github.com/CISC-CMPE-327/Python-CI-2021/pull/1/files)
- [CLI interface](https://github.com/CISC-CMPE-327/Python-CI-2021/tree/option_cli) (later tested with standard IO)
  - Command-line interface (e.g. enter 1,2,3 for navigations). Testing will be done by manually creating command-line inputs and checking all the terminal outputs (e.g. check if the terminal prints `welcome`, then `Logging in the system`, then `enter your email:` etc.)
  - [Summary of files changes](https://github.com/CISC-CMPE-327/Python-CI-2021/pull/2/files)

The team should vote and pick the option that is more applicable for the members' skill set.
Example template can be found by clicking the links above this paragraph.
Please note that the first option may require you to learn additional knowledge outside this course.
Specifically, template-based MVC web services and Selenium-based web testing. 
These techniques, especially selenium, itself is not covered in any other courses, since it is a tool rather than a framework.
It will be worth it to pick them up by doing this course. 
Many of the last year's students found that these tools/knowledge are very helpful for landing/doing their internship.
But again, there is no grading preference for either of them.
It is up to the team to discuss what is the best option.


### ✈️ Step 2 - Planning

This sprint is then kicked off by a planning meeting, where the scrum master and the team members sit down, 
- Create a new scrum board.
- Create columns (the detailed version but not the simple version).
- Put cards on the backlog. There should be at least four cards for the team.
- Assign members and reviewers to the cards.
- Assignees move the cards to the todo column.


### 🎨 Step 3 - Design

Once the assignee starts working on this assignment, move the corresponding card to the design column.
The team member designs the HTTP routes interface and the HTML file names (empty files), following our frontend template. 
If it is the CLI option, then design the screens. 

### 🚀 Step 4 - Daily-Scrum (MVC Dev)

With the given tested backend interface (Model), the team members start implementing the front-end pages (View) and HTTP routes (Controller)
Each team member should develop and test their frontend before making a PR. 


### ✅ Step 5 - Review/Approve
Once a card is done with the implementation and local testing (on your workstation/laptop), you can proceed to PR, request review, and seek approval for merge. 


### 📝 Step 6 - Review & Retrospect
Review your changes, and record a walkthrough demo video for your client (on Youtube). 


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
- The demo video shows that all the frontend pages are runnable.


Violation of any of the above rules (except the one about emoji) will result in a grade penalty.
All the team members, through the principle of collective ownership, must ensure other team members' PR/code does not violate any of the rules above.
For any violations that can be tracked down, a penalty will apply for both the reviewers and the related contributors. 
**For any teamwork issue, penalties will only apply to the member that causing the issue. If there are any teamwork issues for the last/current sprint, please come to my office during the office hour**

## 💺 Grading:

- Scrum practices (max 1 for the deduction, .25 for each violation)
- PR and git practices, including code review (max 1 for the deduction)
- Code style compliance (max 1 for the deduction, .1 for each style error)
- Documentation and comments - each file/class/method/attribute should have comments !!!! (max 3 for deduction, **.2** for each violation)
- Completeness of the features for front-end (max 4 for the deduction, 1 for each missing/incompleted frontend, no partial grades)
