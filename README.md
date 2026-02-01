# CI/CD Tools and Practices Final Project
## project name: ci-cd-final project

<a name="top"></a>

## Table of Contents
- [Intro/Background](#Intro/Background)
- [Exercise-0](#Exercise-0)
- [Exercise-1](#Exercise-1)
- [Exercise-2](#Exercise-2)
- [Exercise-3](#Exercise-3)
- [Exercise-4](#Exercise-4)
- [Exercise-5](#Exercise-5)
- [Exercise-6](#Exercise-6)
- [Exercise-7](#Exercise-7)


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
**1. Submit the GITHUB URL of the `README.md` file that contains the Project name details**
- [`README.md` URL] https://github.com/thecarsun/ci-cd-final-project/blob/main/README.md


[⬆ Back to top](#top)

---

### Exercise 1
#### Create basic workflow

 **Task**
 create Cl Workflow.yml

**What I've done:**
- created the `CI workflow`
- writing steps 
- push to Github


[⬆ Back to top](#top)

---

### Exercise 2
#### Add the linting step to Cl workflow

**Task**
- add the `Lint` step to the GitHub workflow
- use `Flake8` module for linting 

**What I've done:**
- added name/run section to the exisiting Cl workflow
- push to Github

**For Option 1 - AI Graded Submission and Evaluation**
**2. Provide the GitHub URL of `.github/workflows/workflow.yml` showing the code snippet for the Lint with flake8 step or ESlint and the code snippet for the Run unit tests with nose step or Jest-test**
- [`workflow.yml` URL] https://github.com/thecarsun/ci-cd-final-project/blob/main/.github/workflows/workflow.yml


[⬆ Back to top](#top)

---

### Exercise 3
#### Add the test step to Cl workflow

**Task**
- add `Test` step to the Github workflow
- use `Nose` module for running tests

**What I've done:**
- added `test` `nose` section to the existing Cl workflow 


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
**5. Provide the text of terminal output named `cicd-github-validate(.png)`showing details of GitHub actions running successfully in the actions workflow containing all the steps**
 ![`cicd-github-validate`](https://github.com/thecarsun/ci-cd-final-project/blob/main/image-cicd/cicd-github-validate.png)


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
- validate

![suceess!](https://github.com/thecarsun/ci-cd-final-project/blob/main/image-cicd/ecercise5-Tekton%20validate.png)


**For Option 1 - AI Graded Submission and Evaluation**
**3. Provide the GitHub URL of `.tekton/tasks.yml` showing the code snippet for the cleanup task and the code snippet for the nose task or Jest-test**
- [`tasks.yml` URL]https://github.com/thecarsun/ci-cd-final-project/blob/main/.tekton/tasks.yml


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


[⬆ Back to top](#top)

---

## Exercise 7
### Create OpenShift pipeline

**Task**
- create CD pipeline
- use OpenShift from lab
- create PVC through terminal from the `Administrator` perspective

**What I've done:**
- in OpenShift (from lab), setup PVC 
- create a new pipeline (cleanup, git clone, flake8, nose, buildah)
- fix all the error in the pipelines
- tried many many times to fix all the many errors 
- ..... many painful hours and computer crashes later
- it worked!!

**Option 1 - AI Graded Submission and Evaluation**
**4. Provide the screenshot of the OpenShift PersistentVolumeClaim details in a file named `oc-pipelines-console-pvc-details.png`**
![`oc-pipelines-console-pvc-details.png`](https://github.com/thecarsun/ci-cd-final-project/blob/main/image-cicd/oc-pipelines-console-pvc-details.png)

**Option 1 - AI Graded Submission and Evaluation**
**6. Provide the screenshot showing details of the OpenShift Pipeline `oc-pipelines-oc-final.png`**
![`oc-pipelines-oc-final.png`](https://github.com/thecarsun/ci-cd-final-project/blob/main/image-cicd/oc-pipelines-oc-final.png)

**Option 1 - AI Graded Submission and Evaluation**
**7. Provide the screenshot showing details of the OpenShift Pipeline running successfully in a file named `oc-pipelines-oc-green.png`**
![`oc-pipelines-oc-green.png`](https://github.com/thecarsun/ci-cd-final-project/blob/main/image-cicd/oc-pipelines-oc-green.png)

**Option 1 - AI Graded Submission and Evaluation**
**8. Provide the text response showing details of the OpenShift application logs**
![Logs](https://github.com/thecarsun/ci-cd-final-project/blob/main/image-cicd/oc-pipeline-app-logs.png)


[⬆ Back to top](#top)
