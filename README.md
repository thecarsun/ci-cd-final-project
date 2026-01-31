# CI/CD Tools and Practices Final Project
## project name: ci-cd-final project

<a name="top"></a>

## Table of Contents
- [Intro/Background](#Intro/Background)
- [Exercise-0](#Exercise-0)
- [Exercise-1](#Exercise-1)
- [Exercise-2](Exercise-2)
- [Exercise-3](#Exercise-3)
- [Exercise-4](#Exercise-4)
- [Exercise-5](#Exercise-5)
- [Exercise-6](#Exercise-6)


### Intro/Background

This is my final project for the *Continuous Integration and Delivery (CI/CD)* course. Part of the [IBM Applied DevOps Engineering](https://www.coursera.org/professional-certificates/ibm-applied-devops-engineering). 

This final project is about building a CI/CD pipeline.
The GitHub respository is cloned from the [IBM repository template](https://github.com/ibm-developer-skills-network/wtecc-CICD_PracticeCode)

Lab environment used for all the exercises and tasks: **euphemeral**

[⬆ Back to top](#top)

---
### Exercise 0
#### Push Cl code to GitHub

**Task** 
- test workflow and CI pipeline
- commit changes
- push branch back to GitHub respository

**What I've done:** 
- prep environement / GitHub Personal Access Token(PAT)
- Note: GitHub -> Developer Setting -> Personal Access tokens -> Token (Classic)
- clone and create my own Github repository 
- initialize **Development Environment**
- edit *README.md* in the **euphemeral** terminal, add screenshot of Git Push action
- format: `markdown`

![Git Push Action confirmation screeshot](https://github.com/thecarsun/ci-cd-final-project/blob/main/image-cicd/exercise0%20-%20gitpush.jpg)


**For Option 1 - AI Graded Submission and Evaluation**
- [`Readme.md`](https://github.com/thecarsun/ci-cd-final-project/blob/main/README.md)


[⬆ Back to top](#top)

---

### Exercise 1
#### Create basic workflow

 **Task**
 create Cl Workflow.yml

**What I've done:**
- created the `CI workflow`
- writing steps 
- [workflow.yml](https://github.com/thecarsun/ci-cd-final-project/blob/main/.github/workflows/workflow.yml)
- push to GitHub

[⬆ Back to top](#top)

---

### Exercise 2
#### Add the linting step to Cl workflow

**Task**
- add the `Lint` step to the GitHub workflow
- use `Flake8` module for linting 

**What I've done:**
- added name/run section to the exisiting Cl workflow
- [workflow.yml](https://github.com/thecarsun/ci-cd-final-project/blob/main/.github/workflows/workflow.yml)
- push to Github

[⬆ Back to top](#top)

---

### Exercise 3
#### Add the test step to Cl workflow

**Task**
- add `Test` step to the Github workflow
- use `Nose` module for running tests

**What I've done:**
- add name/run section to the existing Cl workflow 
- [workflow.yml](https://github.com/thecarsun/ci-cd-final-project/blob/main/.github/workflows/workflow.yml)
- push to Github

[⬆ Back to top](#top)

--- 

### Exercise 4
#### Validate GitHub Actions Workflow

**Task**
- validate the workflow through GitHub web -> action 

**What I've done:"**
- first try; failed 

![validation fail](https://github.com/thecarsun/ci-cd-final-project/blob/main/image-cicd/exercise4%20-validateghactionworkflow-fail.png)

- troubleshoot; issue with indentation error 
- more errors followed in the following areas: `flake8`, `Lint`, `nose`
- many many many fixes and pushes later.. finally 

![Finally working](https://github.com/thecarsun/ci-cd-final-project/blob/main/image-cicd/exercise4%20-validateghactionworkflow.png)

**Option 1 - AI Graded Sumbmission and Evaluation:**
 - terminal output of `action workflow` 

 ![cicd-github-validate](https://github.com/thecarsun/ci-cd-final-project/blob/main/image-cicd/cicd-github-validate.png)


 [⬆ Back to top](#top)

 ---

### Exercise 5
#### Create cleanup Tekton task

**Task**
- add a `cleanup` `task`
- task will have single step remove

**What I have done:**
- created tasks.yml 
- added details and steps
- validate `tkn task describe cleanup`

![sunceeded](https://github.com/thecarsun/ci-cd-final-project/blob/main/image-cicd/ecercise5-Tekton%20validate.png)


**Option 1 - AI Graded Submission and Evaluation**
- [tasks.yml](https://github.com/thecarsun/ci-cd-final-project/blob/main/.tekton/tasks.yml)

[⬆ Back to top](#top)

--- 

## Exercise 6
### Create test Tekton task

**Task**
- add `nose` under the `cleanup` task

**What I have done:**
- add `nose` under the `cleanup` task in tasks.yml 
- run `kubectl apply -f .tekton/tasks.yml`
- run `tkn task ls`
![validate](https://github.com/thecarsun/ci-cd-final-project/blob/main/image-cicd/ecercise6.png)


**Option 1 - AI Graded Submission and Evaluation**
- [.tekton/tasks.yml](https://github.com/thecarsun/ci-cd-final-project/blob/main/.tekton/tasks.yml)

[⬆ Back to top](#top)

---

## Exercise 6
### Create OpemShift pipeline

**Task**
- create CD pipeline
- use OpenShift from lab
- create PVC through terminal from the `Administrator` perspective

**What I've done:**
- define buildah task
- in OpenShift (from lab), setup PVC 
- create a new pipeline (cleanup, git clone, flake8, nose, buildah)
- fix all the error in the pipelines







#Task 6 - screenshots
#task 8 - screenshots
#task 9 - screenshots
#Task 7 - text response
#Task 10 - text response


