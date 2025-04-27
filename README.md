# Student and Program Management API

This is a RESTful API built using Flask that allows you to manage students, their courses, and academic programs. The API provides endpoints for CRUD operations on students and programs, as well as functionality to check if a student has completed the requirements for a specific program.

## Features

- **Student Management**:
  - Add, update, retrieve, and delete student records.
  - Validate student information, including `personnummer` and course IDs.
  - **Program Management**:
  - Retrieve program details and their required courses.
  
- **Completion Check**:
  - Verify if a student has completed all the required courses for a specific program.

## Endpoints

### Student Endpoints

- **GET** `/student`  
  Retrieve all students.

- **GET** `/student/<id>`  
  Retrieve a specific student by ID.

- **POST** `/create`  
  Add a new student.  
  **Request Body** (JSON):
  ```json
  {
    "name": "John Doe",
    "personnummer": "920223-9999",
    "courses_passed": ["CSE1110", "CSE1111"]
  }
PUT /update/<id>
Update an existing student by ID.
Request Body (JSON):

DELETE /delete/<id>
Delete a student by ID.

Program Endpoints
GET /program
Retrieve all programs.

GET /program/<id>
Retrieve a specific program by ID.

Completion Check Endpoint
GET /finished/<student_id>/<program_id>
Check if a student has completed all the required courses for a program.
Response:  

{
  "status": true,
  "completed_courses": 10
}  

Data Validation
Personnummer: Must follow the format YYMMDD-XXXX and include valid month and day values.
Course IDs: Must follow the format ABC1234 (3 letters followed by 4 digits).

 Installation
Clone the repository:
git clone https://github.com/mhtbtanvir/RESTful-API-.git
cd RESTful-API-
Install dependencies:

Download and install python 3.12 
In a terminal: 

Enter the directory where app.py is located. 
Install the Python package flask: python -m pip install flask 
Set the following environmental variables: 
set FLASK_APP=app.py 
set FLASK_ENV=development 
(on mac/linux, “export” instead of “set”) 
Start flask: python –m flask run or flask run 


Access the API at http://127.0.0.1:5000.

Testing the API
You can use tools like Postman or curl to test the API endpoints. Ensure that the request body is in JSON format where required.

Folder Structure
rest-api-postman/
├── [app.py](http://_vscodecontentref_/0)          # Main Flask application
├── README.md       # Project documentation
├──app.py
├──

License
This project is licensed under the MIT License. See the LICENSE file for details.

Author
Developed by [Tanvir Mahtab]. Feel free to reach out for any questions or suggestions!
