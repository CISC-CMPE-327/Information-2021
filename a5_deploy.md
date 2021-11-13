<h1 align='center'>🍿 Sprint #5 Testing & Deployment 🍿</h1>

<p align='center'>CISC 327  -  Fall 2021</p>

After the previous sprints, the customers are very happy with the system being built and its quality.
They decided to test-deploy in their own container-based deployment environment for an internal beta test run.
Now we are ready to ship! 🚢🚢🚢🚢🚢🚢🚢🚢🚢🚢

In this sprint, we have two main tasks:
- 🔥 Security Testing
- 🔥 Deployment

**Again, each team member should read thoroughly the instruction and the provided template.**


### 🍱 Step 1 - Understanding the tasks

Now your team has chosen the frontend option. For security testing, we have two different instructions:

- [We Interface](a5_sqmap_xss.md) (tested with existing tools)
- [CLI interface](q5_payload.md) (tested with pytest test cases)

For deployment, following [this instruction](a5_docker.md) to setup docker & docker compose.

### ✈️ Step 2 - Planning

This sprint is then kicked off by a planning meeting, where the scrum master and the team members sit down, 
- Grab a drink.
- Create a new scrum board.
- Create columns (the detailed version but not the simple version).
- Put cards on the backlog. There should be at least four cards for the team.
- Assign members and reviewers to the cards.
  - Based on the tasks, two team members can work on security testing and the other two work on deployment.
- Assignees move the cards to the todo column.


### 🎨 Step 3 - Design

Once the assignee starts working on this assignment, move the corresponding card to the design column.
The team member designs the structure of testing files/names. 

### 🚀 Step 4 - Daily-Scrum (MVC Dev)

If there are any adjustments needed before creating the test cases, the team member can move the card to in-progress/under-development and work from there.
Otherwise, one can directly move the card to the testing column.
Daily standup meeting - Following the way we described in the lecture, the scrum master has to host a scrum meeting at least 2 days before the deadline.
The scrum master has to take a screenshot of their board (and upload it to their git repository - can be through the web interface) and create a markdown file with the updates from each team member (can be through the web interface). Each team member is supposed to have started the work before the daily scrum meeting, 
and report the progress or any difficulties. Each team member has to mention: 
1) what is the branch he/she worked on (has to be pushed to the repo). 
2) what is the progress so far (at least some test cases written/some results/code available)
3) any difficulties.
4) what is the plan for the days before the deadline.


### ✅ Step 5 - Review/Approve
Once a card is done with the local testing (on your workstation/laptop), you can proceed to PR, request review, and seek approval for merge. 


### 📝 Step 6 - Review & Retrospect
Review the PRs and the Cards to make sure the team didn't violate any of the rules below.


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
- All the team members have to attend the daily scrum meeting with certain progress (some test cases done or some results available)



Violation of any of the above rules (except the one about emoji) will result in a grade penalty.
All the team members, through the principle of collective ownership, must ensure other team members' PR/code does not violate any of the rules above.
For any violations that can be tracked down, a penalty will apply for both the reviewers and the related contributors. 
**For any teamwork issue, penalties will only apply to the member that causing the issue. If there are any teamwork issues for the last/current sprint, please come to my office during the office hour**

## 💺 Grading:

- Scrum practices (max 1 for the deduction, .25 for each violation)
- PR and git practices, including code review (max 1 for the deduction)
- Code style compliance (max 1 for the deduction, .1 for each style error)
- Documentation and comments - each file/class/method/attribute should have comments !!!! (max 2 for deduction, **.2** for each violation)
  - This includes the test case comments (the CLI option, indicate the purpose and what is being tested)
  - This includes the required answers to the questions for the web option.
- Completeness of the tasks (max 6 for the deduction, **1.5** for each missing/incompleted/incorrect task)
  - This includes if your docker image has been successfully published on docker hub.
  - This includes if your docker-compose file works on our machine. 



