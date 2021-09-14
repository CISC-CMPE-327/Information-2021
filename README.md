<h1 align="center"> :fire: GitHub Basics for Assignment Submission :fire: </h1>


<p align="center">
<img src="https://img.shields.io/badge/CISC.CMPE.327-awesome-brightgreen.svg?style=flat-square">
<img src="https://img.shields.io/github/issues/CISC-CMPE-327/Information-2021.svg?style=flat-square">
<img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square">
<img src="https://img.shields.io/badge/badges-awesome-green.svg?style=flat-square&color=brightgreen">
<img src="https://img.shields.io/github/license/Naereen/StrapDown.js.svg?style=flat-square&color=brightgreen">
</p>

<p align="center">
:+1: Created By: Matt Dixon, Cesur Kavaslar, Andrew Boulos, Steven Ding (who adds Emoji and the badges)
</p>
<p align="center">
:sparkles: Pull request welcomed! You name will be added here!!
</p>

<p align="center">
  <img src="/images/unknown.png" height="450px" alt="" />
</p>
<p align="center">
  <p align="center">[Credits: LammyJams]</p>
</p>


## 1. Create GitHub Account :star:
Many of you may already have a GitHub account, if you do you can skip this step. If you don’t have an account, go to [github.com](github.com) and create one:

<p align="center">
  <img width="600"  src="images/image8.png">
</p>

We recommend you choose the free plan for this course. You are able to skip all steps until you are asked to verify your email address. After verifying our email, you will be brought to your hello-world repository. 

## 2. Where to Ask a Question? :question:
There is an `issues` tab right up there :point_up:. Cannot find it? Click <a href='https://github.com/CISC-CMPE-327/Assignment-Instructions/issues'>HERE</a>. To ask a question, follow two steps:

- Frist, search for related issue using the `Filters` box. 
- If no one asked before, create an issue with a title that summazie your whole question. Then fill in the body of your question. You can copy screenshot and parse into the text box as well. 

## 3. Add Education License :heartpulse:
Go to https://education.github.com/discount_requests/new and add your Queen’s email to receive GitHub’s Education benefits for free.

<p align="center">
  <img width="600"  src="images/edu.png">
</p>

<p align="center">
  <img width="600"  src="images/image6.png">
</p>



You will be asked to verify the account in Email Settings. Once the address is verified, your benefits should be accessible.

## 4. Create a Private GitHub Repository :zap:
Now that you have an account, you can create your repository (repo) for the course. Only one person per group needs to create a repo. 
Navigate to your repositories page and click the green button in the upper-right labeled `New` to create a new repo. 


<p align="center">
  <img width="800"  src="images/image4.png">
</p>


Name your repo and make sure to change your repo to Private. As well, you’ll want to initialize your repo with a README file and add the license you chose for your project in Assignment 0. Also pick a `.gitignore` file according to your chosen programming language. Basically it contains list of rules to ignore certain file extensions to be tracked in the repository (so basically they are ignored)


<p align="center">
  <img width="600"  src="images/image1.png">
</p>


## 5. Add Collaborators :ocean:
Go to the Settings tab of your new repository and select the Collaborators option on the left.

<p align="center">
  <img width="600"  src="images/image3.png">
</p>


First, add each of your team members’ GitHub Accounts as collaborators to the repo.
Next, add each of the TA’s accounts as collaborators as well - this will allow us to mark your assignments.

***[please find each TAs GitHub name at the course home page]***

Congratulations, you’ve finished setting up your repo and now it’s time to start working! If you are unable to add more than 3 collaborators, make sure that you have added in your educational license in the 3 step.


## 6. Clone the Repository to Your Laptop :muscle:

Open a terminal on your laptop and let's create a local copy of your GitHub repository by:
```
git clone your_repository_homepage_url
```
You will be asked to sign in GitHub. Now open your file explorer or finder, you will find that there is now a new folder created. It contains the files from your repository.

## 7. Committing changes to Github :facepunch:

You can make changes to your local repository in any ways you want. For example, you can download necessary files from our template repository and put it to the folder. But make sure that you didn't modify the `.git` folder which contains repository data that tracks the changes you made over time. 

Every time you would like to commit your code to the repository, make sure that you have downloaded all the remote changes (made by other people) by executing:
```
git pull 
```
If there is any error, possibly caused by the modification conflict made by you and the others, merge and address any changes in the files accordling. You can take a look at the changes you have made to the local repository if you want:
```
git diff
```
Now, we are ready to commit our code. First, we add all the changes we made.
```
git add .
```
Then, we create a local commit with a message:
```
git commit -m `yo this is a message for the commit, it supports emoji!`
```
Then we push the local commit to GitHub:
```
git push
```
Done! Check your repository home page. You will see the updated files. If you have a GitHub Action workflow defined, you can see you test codes are running on the `actions` tab!


## 8. Creating a Tag for Assignment Submission :pray:

(For each assignment, specific instruction is given on how and what should your team submit. If not, by default, following the instruction below)

Now ready for submission? It is easy. Just create a tag of current version of your code:
```
git tag v0.0.1
```
v0.0.1 is your chosen name of current version. The conversion of the naming starts with `v`. You can put whatever number. This tag is just created locally. We need to push it to GitHub:
```
git push --tags
```
If the above command line does not work:
```
git push --follow-tags
```
You can checkout different tags on your repository home page here:

<p align="center">
  <img width="800"  src="images/tag.jpg">
</p>

Then submit the **link to your group repository** as well as the **tag name** to onQ. Want to update your submission? It is easy. Just create another **new tag**, and submit the **new tag name** and the **link to your group repository** to onQ. 

:clap::clap::clap::clap:
