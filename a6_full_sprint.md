<h1 align='center'>🍿 #6 - A Complete Sprint 🍿</h1>

<p align='center'>CISC 327  -  Fall 2021</p>


## 💺 Customer Requirement


Up until this point, we have divided different stages of development into separate sprints. In reality, most of them happened in a single sprint. In this final sprint, we will walk through the whole process again to deliver additional features in order to complete the system:

- Placing order
  - A user can place an order on the products.
  - A user cannot place an order for his/her products.
  - A user cannot place an order that costs more than his/her balance.
  - A sold product will not be shown on the other user's user interface.
  - A sold product can be shown on the owner's user interface.

🛳️ 🚢 🛳️ 🚢 🛳️ 🚢 🛳️ 🚢 🛳️ 🚢 🛳️ 🚢 🛳️ 🚢 🛳️ 🚢 🛳️ 🚢

**Again, each team member should read thoroughly the instruction and the provided template.**

### Planning

This sprint is then kicked off by a planning meeting, where the scrum master and the team members sit down, 
- Grab a drink.
- Create a new scrum board.
- Create columns (the detailed version but not the simple version).
- Put cards on the backlog.
  - Instead of using user stories as cards, your team can create tasks corresponding to the different stages:
   - backend development
   - backend testing
   - frontend development
   - frontend integration testing
   - security testing 
   - deployment (update docker image)
- Assign members and reviewers to the cards.
- Assignees move the cards to the todo column.

For this assignment, we no longer list out the steps. It is up to your team how to run through the process since we have already gone through the same process many times. 

For the teams that used to have team collaboration issues, you can assign the most dependable team member for the high-priority task (the one that needed to be done at the beginning), and assign the least dependable team member for the last task. 

### Daily-Scrum (MVC Dev)

Daily standup meeting - Following the way we described in the lecture, the scrum master has to host **two** scrum meetings at least 2 days before the deadline, and 2 days apart.
The scrum master has to take a screenshot of their board (and upload it to their git repository - can be through the web interface) and create a markdown file 
with the updates from each team member. Each team member is supposed to have started the work before the daily scrum meeting, 
and report the progress or any difficulties. Each team member has to mention: 
1) what is the branch he/she worked on (has to be pushed to the repo). 
2) what is the progress so far.
3) any difficulties.
4) what is the plan for next.



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
- All the team members have to attend the daily scrum meeting with certain progress
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
  - This includes the test case comments (need to mention the requirement and/or its ID, the testing method if any)
  - This includes the testing file/name structure (see the Review & Retrospect step)
- Completeness of the features front-end, back-end, and all the testing (max 4 points for deduction)
