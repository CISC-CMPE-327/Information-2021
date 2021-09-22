<h1 align='center'>🍿 A Scrum Course Project: qBay 🍿</h1>

<p align='center'>CISC 327  -  Fall 2021</p>


## 💺 Project Teams and Process

You have formed a team of four (preferably four) people to design, implement, document, and deliver a two-part software product.  
All phases should follow the scrum software development process as much as it applies with some XP practices - in particular, 

- continuously maintained test suites as requirements and quality control
- pair programming
- code review of all code
- a simplest possible solution to every problem
- continuous redesign and rearchitecting
- automation in testing and integration
- **All the code/documentation contributions will go through the pull-request/review process**

Every 1–2 weeks, you will deliver a progress report or other evidence of your team’s efforts as required by project assignments.


## 💺 Project Phases

The project will be done in several phases, each of which will be an assignment. 
Phases will cover steps in the process of creating a quality software result in the context of a scrum software development process model.
Each phase of the project corresponds to a single sprint in the Scrum software development process.
Assignments will be on the quality control aspects of requirements, rapid prototyping, design, coding, integration, and analysis of the building's product. 
Your final products will be tested and evaluated by an independent evaluator or an automated system.

## 💺 Getting Start

1. [***Important***] One elected team member, preferably the most experienced one, acts as a Scrum master. 

2. [***Important***] The Scrum master, after negotiating with the team, select a style guide for the programming language in the project. (e.g. PEP 8 for python). If any new languages are added to the project later on, such as JavaScript later for the front-end, the scrum master has to add a new style guide for that language.  

3. [***Important***] The scrum master follows this [guide](https://docs.github.com/en/free-pro-team@latest/github/building-a-strong-community/creating-a-pull-request-template-for-your-repository) to create a pull request template agreed upon by the team members. 
[Example](https://embeddedartistry.com/blog/2017/08/04/a-github-pull-request-template-for-your-projects/) of a PR template. Starting from this point of the assignments, all the PRs have to follow the agreed template. This template should be used in each PR.
The template must include the selected style guides in the checklist. 

4. [***Important***] The Scrum master creates a project for this sprint (i.e. assignment 1) through the GitHub Projects tab of your repository. Populate the required columns for a scrum development model.


## 💺 Project Requirement

The product you are to design and build is qBay, similar to eBay, for C2C online shopping. The instructor and the TAs will be your customers.
The customers have decided that:

- A registered user can buy and sell products through this online application. 
- A transaction represents a successful purchase.
- A verified buyer can also leave a product review. 
- Shipping and handling will be carried out offline, assuming that the product is always shipped and arrived instantly. 
- User payment is directly through their balance on the online application.
- A user can add money to their account through online banking (transfer directly from their own banking account).

For this sprint, the development team (you) decided to first define data models based on the application concept above,
in which the entity types in the system are specified; so the customer (us) can check if these entities have enough attributes to reflect the required information per entity.

- At the moment, the customers do not have any ideas about the constraints (e.g. password complexity, username constraint, possible attributes) of the entities. 
So feel free to include anything. Then, the customer will discuss it and provide you further requirements changes and constraints in the next sprint.

The tasks for this sprint:

- Identify the entities of the application (hint in total at least 4, can be more depending on your design).
- Create cards (backlog) on your scrum board for this sprint to implement the entities.
- Assign team members and reviewers for each card (task). 
- Implement the data models following the python example below. All the code must have detailed comments. All the models can be in a single file.
- PR, Review, and Merge the PR.
- Testing: all the code follow the selected coding guideline. (for example, [pep8 for python](https://flake8.pycqa.org/en/latest/))
- Sprint review: review each card and each PRs, ensuring that they didn't violate any of the rules defined below. Create a tag for A1 submission through onQ.


```python
from flask import Flask
from flask_sqlalchemy import SQLAlchemy

app = Flask(__name__)
app.config['SQLALCHEMY_DATABASE_URI'] = 'sqlite:///db.sqlite'
db = SQLAlchemy(app)


class User(db.Model):
    id = db.Column(db.Integer, primary_key=True)
    username = db.Column(db.String(80), unique=True, nullable=False)
    email = db.Column(db.String(120), unique=True, nullable=False)

    def __repr__(self):
        return '<User %r>' % self.username

```

## 💺 Rules

All the assignments, starting from this point, will follow these rules:

- No file changes/uploads through the web interface. We can tell.
- No direct change to the master/main branch of your repository. 
- All the changes to the repository have to go through Pull Request (PR).
- All the PRs require reviews and approval before merging. 
- All the reviews must provide at least one comment (constructive & specific) for improvement. 
- All the team members must have at least a PR for each assignment (sprint).
- All the project activities have to be planned through the scrum board before coding and testing.
- All the cards for each sprint have to go through each column of your team's scrum board (cannot just directly jump from todo to done).
- All the PRs should be associated with at least one card in your scrum board (by mentioning the PR number using `#` in the card)
- All the PRs should follow the agreed PR template.
- All the documentation has to follow the [markdown format](https://guides.github.com/features/mastering-markdown/).
- All the merged code must follow the selected coding style guide. 
- Each of the PR's titles should have emojis. 


Violation of any of the above rules (except the last one about emoji) will result in a grade penalty.
All the team members, through the principle of collective ownership, must ensure other team member's PR/code does not violate any of the rules above.
For any violations that can be tracked down, a penalty will apply for both the reviewers and the related contributors. 

## 💺 Grading:

- Scrum practices (max 2 for the deduction, .25 for each violation, maximum number of violations before deduction 2)
- PR and git practices, including code review (max 3 for the deduction, .25 for each violation, maximum number of violations before deduction 3)
- Code style compliance (max 3 for the deduction, .1 for each style error, maximum number of violations before deduction 2)
- Documentation and comments - each file/class/method/attribute should have comments. (max 1 for deduction, .1 for each violation)
- Completeness of the data models covering all the above customer requirements (max 1 for the deduction, missing one required entity minus .25)




