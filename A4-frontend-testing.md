<h1 align='center'>🍿 Sprint #4 Front-end Integration Testing 🍿</h1>

<p align='center'>CISC 327  -  Fall 2021</p>


## 💺 Customer Requirement

Continuing our requirements from the last sprint, now you have the backend models up running as well as frontend prototypes ready. 

The customers played the prototype with you. 
They are extremely happy. 
They decided to give your team an additional $0 budget to continue this project.
All the team members are very happy since they also got a promotion with a $0 raise 🔥. 

Now, it is the time for testing before the first delivery. 

The customer does not have additional requirements at the moment.
Detailed specifications with constraints will be provided in the next sprint after the customer tried out the prototype. 
Customers still have the same requirement as A2. 
But this time, we will test the frontend together with the backend as our integration testing. 

 🚒 🚒 🚒 🚒 🚒 🚒 🚒

**Again, each team member should read thoroughly the instruction and the provided template.**


### 🍱 Step 1 - Frontend Options

Now your team has chosen the frontend option. Example testing code can be found at:

- [We Interface](https://github.com/CISC-CMPE-327/Python-CI-2021/pull/6/files) (tested with selenium)
- [CLI interface](https://github.com/CISC-CMPE-327/Python-CI-2021/pull/5/files) (tested with standard IO)

Now, following these examples, test the program again following the requirement from A2. 

### ✈️ Step 2 - Planning

This sprint is then kicked off by a planning meeting, where the scrum master and the team members sit down, 
- Grab a drink.
- Create a new scrum board.
- Create columns (the detailed version but not the simple version).
- Put cards on the backlog. There should be at least four cards for the team.
- Assign members and reviewers to the cards.
- Assignees move the cards to the todo column.


### 🎨 Step 3 - Design

Once the assignee starts working on this assignment, move the corresponding card to the design column.
The team member designs the structure of testing files/names. 

### 🚀 Step 4 - Daily-Scrum (MVC Dev)

If there are any adjustments needed before creating the test cases, the team member can move the card to in-progress/under-development and work from there.
Otherwise, one can directly move the card to the testing column.
**The test cases from each member have to cover at least three different BlackBox testing methods.**
**The test cases must be annotated with the testing methods.**
Daily standup meeting - Following the way we described in the lecture, the scrum master has to host a scrum meeting at least 2 days before the deadline.
The scrum master has to take a screenshot of their board (and upload it to their git repository - can be through the web interface) and create a markdown file with the updates from each team member (can be through the web interface). Each team member is supposed to have started the work before the daily scrum meeting, 
and report the progress or any difficulties. Each team member has to mention: 
1) what is the branch he/she worked on (has to be pushed to the repo). 
2) what is the progress so far (at least some test cases written, more than 2)
3) any difficulties.
4) what is the plan for the days before the deadline.


### ✅ Step 5 - Review/Approve
Once a card is done with the implementation and local testing (on your workstation/laptop), you can proceed to PR, request review, and seek approval for merge. 


### 📝 Step 6 - Review & Retrospect
Review your changes, and document the structure (file/folder/test function name) in a single markdown on your home page (can be through the web interface). You can organize it in the way you prefer. 
The TA will rely on this to find your test cases.


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

**Additional rules for this assignment:**
- Your main branch's badge has to be build-passing at the time of assignment submission. 
- All the test cases passed, covering all the A2's requirements.
- All the team members have to attend the daily scrum meeting with certain progress (at least some test cases written, more than 2)
- The test cases from each member have to cover at least three different BlackBox testing methods.
- The test cases must be annotated with the testing methods.


Violation of any of the above rules (except the one about emoji) will result in a grade penalty.
All the team members, through the principle of collective ownership, must ensure other team members' PR/code does not violate any of the rules above.
For any violations that can be tracked down, a penalty will apply for both the reviewers and the related contributors. 
**For any teamwork issue, penalties will only apply to the member that causing the issue. If there are any teamwork issues for the last/current sprint, please come to my office during the office hour**

## 💺 Grading:

- Scrum practices (max 1 for the deduction, .25 for each violation)
- PR and git practices, including code review (max 1 for the deduction)
- Code style compliance (max 1 for the deduction, .1 for each style error)
- Documentation and comments - each file/class/method/attribute should have comments !!!! (max 3 for deduction, **.2** for each violation)
  - This includes the test case comments (need to mention the requirment and/or its ID, **the testing method if any as well as your analysis to come up the test case**)
  - This includes the testing file/name structure (see the Review & Retrospect step)
- Completeness of the test cases on the front-end (max 4 for the deduction, **1** for each missing/incompleted/incorrect test)
