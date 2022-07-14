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
     - employee_id
     - employee_name
     - employee_role
   ### request
    - request_id
    - request_desc
    - status
    - amount

   ### User stories and associated unit/service tests 

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
