# **Task 1. Development of API for To-Do List management (To-Do List)**                                                                               

## **Technical Requirements**                                                                               
1. **General**                                                                               
* `Stack`: **Python3**, **Django**, **Django REST Framework**.                                                                               
* `DataBases`: **PostgreSQL** \ **MySQL** (and \ or other non-relational DB).                                                                               
2. **Models**                                                                               
   * **Task**:
        * `id`
        * `created_by`
        * `title`
        * `description`
        * `status`
        * `completed`
        * `created_at`
        * `completed_at`
        * `updated_at`
        * `deleted_at`
        * `deleted`
        * `category`
        * `priority`
   * **Category**:
        * `id`
        * `name`
        * `description`
        * `created_at`
        * `updated_at`
        * `deleted_at`
        * `deleted`
   * **Priority**:
        * `id`
        * `name`
        * `created_at`
        * `updated_at`
        * `deleted_at`
        * `deleted`

---

## **Functional Requirements**                                                                               

**CRUD**:                                                                               

1) **User**                                                                               
* Create User (**POST**)                                                                               
* Get all users (**GET**)                                                                               
* Get user by ID (**GET**)                                                                               
* Update user (**PUT/PATCH**)                                                                               
* Delete user (**DELETE**) (soft delete **by user**, and hard delete **by admin**)                                                                               
* Login (**POST**)                                                                               
* Logout (**POST**)                                                                               
* Change password (**POST**)                                                                               
* Reset password (**POST**)                                                                               

2) **Task**                                                                               
* Create Task (**POST**)                                                                               
* Get all tasks for user (**GET**)                                                                               
* Get all tasks by status (**GET**)                                                                               
* Get all tasks by category (**GET**)                                                                               
* Get all tasks by priority (**GET**)                                                                               
* Get user's task by ID (**GET**)                                                                               
* Update task (**PUT/PATCH**)                                                                               
* Delete task (**DELETE**) (soft delete **by user**, and hard delete **by admin**)                                                                               

3) **Category**                                                                               
* Create Category (**POST**)                                                                               
* Get category by ID (**GET**)                                                                               
* Update category (**PUT/PATCH**)                                                                               
* Delete category (**DELETE**) (soft delete **by user**, and hard delete **by admin**)                                                                               

4) **Priority**                                                                               
* Create Priority (**POST**)                                                                               
* Get priority by ID (**GET**)                                                                               
* Update priority (**PUT/PATCH**)                                                                               
* Delete priority (**DELETE**) (soft delete **by user**, and hard delete **by admin**)                                                                               

**Filtering and sorting:**                                                                               
* Filtering tasks by execution status                                                                               
* Sorting by creation date and/or execution status                                                                               

---

# **Permissions**                                                                               
1) **Admin**:                                                                               
* Managing all tasks                                                                               
* Managing all users                                                                               
2) **User**:                                                                               
* Managing only himself tasks, categories, priorities, tasks statuses                                                                               
* Managing only himself profile                                                                               

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
**Administrator**                                                                               
1) **User Management**:                                                                               
* **As an administrator, I want to be able to** view all users to                                                                                
manage accounts.                                                                               
* **As an administrator, I want to be able to** create new users to                                                                                
grow the user base.                                                                               
* **As an administrator, I want to be able to** update user data to                                                                               
keep information current.                                                                               
* **As an administrator, I want to be able to** delete users                                                                                
(hard delete) to manage the user database.                                                                               


2) **Task Management:**                                                                               

* **As an administrator, I want to be able to** create, view, edit and                                                                                
delete any tasks to manage all aspects of tasks in the system.                                                                               


3) **Category and Priority Management:**                                                                               

* **As an administrator, I want to be able to** manage categories and                                                                                
priorities of tasks to allow for more accurate organization and                                                                               
scheduling of tasks.                                                                               


**Regular user**                                                                               

1) **Managing my own tasks:**                                                                               

* **As a user, I want to be able to** create, view, edit and delete                                                                                
(**soft delete**) my own tasks to manage my to-do's effectively.                                                                               
* **As a user, I want to be able to** mark tasks as completed to                                                                               
track my progress.                                                                               


2) **Personal Profile Management:**                                                                               

* **As a user, I want to be able to** update my profile, including                                                                                
changing my password, to keep my personal information up to date.                                                                               


3) **Working with categories and priorities:**                                                                               

* **As a user, I want to be able to** manage categories and priorities                                                                                
for my tasks to better organize my tasks.                                                                               

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

---

### **Additionally**                                                                               
**Docker и Nginx**:                                                                               
* Project containerization using [**Docker**](https://www.docker.com/).                                                                               
* [**Nginx**](https://www.nginx.com/) must proxy requests to the application.                                                                               
