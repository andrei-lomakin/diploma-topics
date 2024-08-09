# **Task 3: Online surveys**                                                                               

## **Technical Requirements**                                                                                    

1. **General**                                                                                
* `Stack`: **Python3**, **Django**, **Django REST Framework**.                                                                                                                                                              
* `DataBases`: **PostgreSQL** \ **MySQL** (and \ or other non-relational DB).                                                                                                                                                              
2. **Models**                                                                                                                       
**Survey**                                                                               
* `id`: The unique identifier for the survey.                                                                               
* `title`: The title of the survey.                                                                               
* `description`: The description of the survey.                                                                               
* `start_date`: The date the survey started. This field should not change                                                                                                                                                               
once the survey has started.                                                                                                                                                              
* `end_date`: The date the survey ends.                                                                               
* `is_active`: The activity status of the survey (active/inactive).                                                                               

**Question**                                                                               
* `id`: The unique identifier of the question.                                                                               
* `survey`: Link to the survey (ForeignKey to Survey).                                                                               
* `text`: The text of the question.                                                                               
* `question_type`: The type of question (e.g. Single Choice, Multiple Choice, Text Answer).                                                                               

**AnswerOption**                                                                               
* `id`: Unique identifier for the answer option.                                                                               
* `question`: The relationship to the question (ForeignKey to Question).                                                                               
* `text`: The text of the answer choice.                                                                               

**UserResponse**                                                                               
* `id`: Unique identifier of the user response.                                                                               
* `question`: Link to question (ForeignKey to Question).                                                                               
* `selected_option`: The selected answer option (ForeignKey to AnswerOption).                                                                                                                                                               
Can be null for text responses.                                                                                                                                                              
* `text_response`: The user's text response. Used for text questions only.                                                                               
* `user_id`: The ID of the user who left the answer. Can be anonymous or                                                                                                                                                               
associated with a user account.                                                                                                                                                              

## **Functional Requirements**                                                                               

**CRUD**:                                                                               

1) **User**                                                                               
Create User(**POST**)                                                                               
Get all Users(**GET**)                                                                               
Get user by ID(**GET**)                                                                               
Update User(**PUT\PATCH**)                                                                               
Delete User(**DELETE**)                                                                               
Login(**POST**)                                                                               
Logout(**POST**)                                                                               
Change password(**POST**)                                                                               
Reset password(**POST**)                                                                               

2) **Question**                                                                               
Create Question(**POST**)                                                                               
Get all Questions(**GET**)                                                                               
Get Question by ID(**GET**)                                                                               
Update Question(**PUT\PATCH**)                                                                               
Delete Question(**DELETE**)                                                                               

3) **AnswerOption**                                                                               
Create Answer(**POST**)                                                                               
Get all Answers(**GET**)                                                                               
Get Answer by ID(**GET**)                                                                               
Update Answer(**PUT\PATCH**)                                                                               
Delete Answer(**DELETE**)                                                                               

4) **Survey**                                                                               
Create Survey(**POST**)                                                                               
Get all Surveys(**GET**)                                                                               
Get Survey by ID(**GET**)                                                                               
Update Survey(**PUT\PATCH**)                                                                               
Delete Survey(**DELETE**)                                                                               
Get survey's questions(**GET**)                                                                               
Get survey's answers(**GET**)                                                                               
Get survey's answers by question(**GET**)                                                                               
Get survey's statistics(**GET**)                                                                               

5) **UserResponse**                                                                               
Create UserResponse(**POST**)                                                                               
Get all UserResponses(**GET**)                                                                               
Get UserResponse by ID(**GET**)                                                                               


**Filtering and sorting:**                                                                               
* Filtering surveys by questions                                                                               
* Sorting surveys by date                                                                               

---

# **Permissions**                                                                               
1) **Admin**:                                                                               
* Managing all surveys                                                                                                                                                              
* Managing all users                                                                               
2) **User**:                                                                               
* Managing only himself profile                                                                               
* Have possibility to answer on surveys                                                                               
---

## **Security**                                                                               

1) **Authentication**:                                                                                                                                                              
* Consider implementing an authentication system (e.g. **Token Authentication**).                                                                                                                                                              

2) **Data Validation**:                                                                                                                                                              
* Check for correct input data for all operations.                                                                               

---

## **Testing**                                                                               
1) **Unit tests**:                                                                               
* Writing tests to verify the functionality of all **CRUD** operations.                                                                               
2) **Integration tests**:                                                                               
* Testing the interaction of system components.                                                                               

---

## **Documentation**                                                                               

1) **README**:                                                                               
Project Description.                                                                               
List of technologies used to write the project.                                                                               
Instructions on how to install and run the application: commands one                                                                                                                                    
by one. How to run the project.                                                                                                                                     
2) **API documentation**:                                                                               
Description of endpoints, request and response formats. Examples of                                                                                                                                     
data that must be passed to process requests.                                                                                                                                       

---

# **User Flow \ User Journey**                                                                               

**For Admin:**                                                                               
* **As an admin, I want to be able to** create polls to give users                                                                               
different topics for polls.                                                                               
This includes providing a title, description, start and end date for the survey.                                                                               

* **As an administrator, I want to** be able to add questions to surveys                                                                               
to shape the content of each survey.                                                                               
Ability to select the type of question (single choice, multiple choice, text response).                                                                               

* **As an admin, I want to be able to** edit and delete surveys and                                                                               
questions to correct errors or update information.                                                                               

* **As an admin, I want to** be able to view statistics on user responses                                                                               
to analyze survey data.                                                                               

* **As an administrator, I want to be able to** manage users (create, edit,                                                                               
delete) to provide administration of the platform.                                                                               

**For User:**                                                                               
* **As a user, I want to be able to** view a list of available and active surveys                                                                               
so that I can select surveys of interest to participate in.                                                                               

* **As a user, I want to be able to** participate in surveys by selecting                                                                                
answers to questions to express my opinion or provide information.                                                                               

* **As a user, I want to be able to** view the results of surveys after they                                                                               
have been completed to see what participants think overall. (This is                                                                               
optional and depends on the survey's privacy policy.)                                                                               

* **As a user, I want to be able to** register and log in to have my responses                                                                                
linked to my account.                                                                               
* **As a user, I want to be able to** change my personal                                                                                
information and manage my account to keep my information up to date.                                                                               

---
### **Rules for working with **Git** for thesis writing and development. Branch organization**                                                                               
`One task - one branch`: You should create a separate branch from the                                                                                
main for each new task or functionality.                                                                                
The name of the branch should reflect the nature of the task.                                                                               

`Prohibit direct changes to the main`: All changes should be pushed into                                                                                
the main via **Pull Requests (PR)** after review and approval by other team members.                                                                               


**Commits**                                                                               
* `Many commits`: Make commits frequently to track progress and facilitate                                                                               
possible debugging.                                                                               
* `Informative commits`: Each commit should contain a clear and concise                                                                               
description of the changes made.                                                                               
* `Prefix commit system`:                                                                               
    * `doc`: To add or modify documentation.                                                                               
    * `feat`: To add new functionality.                                                                               
    * `fix`: For bug fixes or debugging.                                                                               

**Working with Pull Requests (PR)**                                                                                                                                                              
* `PR Description`: Each PR should contain a detailed description of the                                                                                
changes made and references to relevant tasks or requirements.                                                                               
* `Code-review`: Prior to merging with the main, the PR should be                                                                               
code-reviewed by at least one other team member.                                                                               
* `Testing`: Before creating a PR, make sure your code passes all                                                                                
tests and meets coding standards.                                                                               

**Regular updates**                                                                               
`Synchronize with main`: Regularly update your working branches by                                                                                
synchronizing them with the main branch of main to avoid merge conflicts.                                                                               
