# **Booking**                                                                                                           

## **Project description**                                                                                              
**Purpose**:
The application is designed for booking hotel rooms. Users can view hotels,                                             
and available rooms, book rooms for specific dates and view their                                                       
reservations. There is also functionality to leave comments                                                             
and ratings for hotels.                                                                                                 

## **Technical Stack**
* **Backend**: Django (**Python**)                                                                                      
* **Frontend**: (if needed): Python, HTML(Django templates), CSS(if needed)                                             
* **Database**: PostgreSQL \ MySQL                                                                                      
* **API**: **Django REST framework**                                                                                    
* **Additional tools**: **Docker** (for application containerization), **Nginx**                                        

## **Functional Requirements**
**Functionality**
Viewing a list of hotels                                                                                                
View available rooms at each hotel                                                                                      
Booking rooms for specific dates                                                                                        
View and manage your reservations                                                                                       
Leave comments and ratings for hotels                                                                                   
Protect against double bookings of the same room for the same dates                                                     

---

### **Models**
* **Hotel**: id, name, location, description, photos, rating,                                                                 
created_at, updated_at, deleted_at, deleted                                                                                      
* **Room**: id, hotel_id, room_type, photos, price_per_night, available                                                   
created_at, updated_at, deleted_at, deleted                                                                             
* **Booking**: id, user_id, room_id, check_in_date, check_out_date, created_at,                                           
updated_at, deleted_at, deleted                                                                                         
* **User**: id, username, email, password, bookings, created_at, updated_at                                               
* **Review**: id, user_id, hotel_id, comment, rating, created_at,                                                         
updated_at, deleted_at, deleted                                                                                         


### **Roles**                                                                                                           
**User**:                                                                                                               
* View hotels and rooms                                                                                                 
* Booking rooms                                                                                                         
* View and manage your reservations                                                                                     
* Leaving comments and ratings                                                                                          
**Administrator**:                                                                                                      
* Manage your hotel and room list                                                                                         
* Manage all reservations                                                                                                   

### **Functional Requirements**                                                                                         
**CRUD system**                                                                                                         
* **Hotels and Rooms** (Create, Read, Update, Delete)                                                                     
* **Reservations** (Create, Read, Update, Delete)                                                                             
* **User comments and ratings** (Create, Read, Update, Delete)                                                          

---

#### **User Requirements**                                                                                          
##### **User:**                                                                                          
1) **View hotels**                                                                                          
* **As a user, I want to** view a list of all hotels to familiarize myself with                                               
possible accommodation options.                                                                                           
* **As a user, I want to** see detailed information about the hotel (e.g.                                                                                           
location, description, reviews) so that I can make an informed choice.                                                                                          

2) **View Rooms**                                                                                          
* **As a user, I want to** browse available rooms at the selected hotel to find the                                                                                           
right fit.                                                                                           
* **As a user, I want to** see detailed information about a room                                                                                           
(room type, price per night, amenities) to make sure it meets my needs.                                                                                           

3) **Room Reservations**                                                                                          
* **As a user, I want to** easily book a room for specific dates to plan my trip.                                                                                          
* **As a user, I want to** receive a booking confirmation to be sure of my reservation.                                                                                          

4) **Manage Reservations**                                                                                          
* **As a user, I want to** view my current and upcoming bookings to have a                                                                                           
clear view of my plans.                                                                                          
* **As a user, I want to** be able to modify or cancel reservations to adapt                                                                                           
to changing circumstances.                                                                                          

5) **Reviews and ratings**                                                                                          
* **As a user, I want to** leave comments and ratings for hotels after a stay                                                                                           
to share my experience with others.                                                                                          
* **As a user, I want to** read reviews from other users to make more informed                                                                                          
decisions when choosing a hotel.                                                                                          

6) **Personal Profile**                                                                                          
* **As a user, I want to** be able to register and log in to save my details                                                                                           
and booking history.                                                                                          
* **As a user, I want to** manage my profile (edit personal details and contact                                                                                           
information) to keep my information up to date.                                                                                                                                    

##### **Admin**                                                                                          

1) **Manage hotels**                                                                                          
* **As an administrator, I want to** add, edit and delete hotel information                                                                                           
(name, description, location, photos) to keep the hotel catalogue up to date.                                                                                          
* **As an administrator, I want to** view user reviews and ratings about hotels                                                                                          
to keep track of the quality of the offerings.                                                                                           

2) **Room Management**                                                                                          
* **As an administrator, I want to** add, edit and delete hotel room information                                                                                           
(room type, price, amenities, photos) to ensure an accurate and up-to-date                                                                                           
representation of available rooms.                                                                                           
* **As an administrator, I want to** manage room availability to                                                                                          
prevent double bookings.                                                                                           

3) **Manage reservations**                                                                                          
* **As an administrator, I want to** view all current and upcoming bookings to have                                                                                           
a complete overview of scheduled stays.                                                                                          
* **As an administrator, I want to** be able to cancel or modify reservations as                                                                                           
needed to respond to emergencies or special requests.                                                                                          

4) **Monitoring and analytics**                                                                                          
* **As an administrator, I want to** have access to analytics of app usage (e.g.                                                                                           
number of bookings, popular hotels) to understand user needs                                                                                          
and improve the service.                                                                                          

---

#### **Security**                                                                               

1) **Authentication**:                                                                               
* Consider implementing an authentication system (e.g. **Token Authentication**).                                                                               

2) **Data Validation**:                                                                               
* Check for correct input data for all operations.                                                                               

---

#### **Testing**                                                                               
1) **Unit tests**:                                                                               
* Writing tests to verify the functionality of all **CRUD** operations.                                                                               
2) **Integration tests**:                                                                               
* Testing the interaction of system components.                                                                               


---
#### **Rules for working with **Git** for thesis writing and development. Branch organization**                                                                               
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
