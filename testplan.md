# Test Plan
 ## Technologies to be used
   - Java
   - Maven
   - Hibernate
   - AWS RDS (Postgres)
   - Selenium
   - Cucumber
   - Junit
   - HTML
   - CSS
   - JavaScript

 ## Entities Tracker
   ### employee:
   - employee_id (int) (primary identifier)
   - employee_name (String)
   - employee_role (String)
   ### request
   - request_id (int) (primary identifier)
   - request_desc (String)
   - status (String)
   - amount (int)

   ### User stories and associated unit/service tests 
   1. As a manager I want to view reimbursement requests so I can start addressing them
       - Unit tests
           - approve request 
               -method: approveRequest()
           - deny request
               -method: denyRequest()  
       - Service tests:
       - +        
   2. As an employee I want to create a reimbursement request so I can get money back I spent for the company
       - Unite tests
Positive Test- Manager/Employee login successful 
Negative Test - Manager/Employee login unsuccesful

Postive Test - Manger successful Views reimbursments on home page
Negative Test- Manger unsuccessful Views reimbursments on home page

Positive Test - Manager successful Approve/Deny Reimbursement Requests 
Negative Test-  Manager unsuccessful Approve/Deny Reimbursement Requests 

Positive Test- Employee successful creates a reimbursement request 
Negative Test- Employee unsuccessful creates a reimbursement request

Positive Test- Employee successful view previous reimbursement requests
Negative Test- Employee unsuccessful view previous reimbursement requests

Positive Test- Employee/Manager successfully Logs out of their homepage


Service Testing
    Service Test -Employees Successfully see their own reimbursement requests 

    Service Test- Employees can request up to $1000 dollars per request

    Service Test- Employees provides a reason for the reimbursement request no longer than 500 characters successful

    Service Test- Managers provides a reason for approving or denying a reimbursement request no longer than 500 characters Successfully
    
    Service Test- Usernames are unique
