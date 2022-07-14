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
   - username (String)
   - password (String)
 
   ### request
   - request_id (int) (primary identifier)
   - reason (String)
   - status (String)
   - amount (int)
   - approved_By (int)  
   

   ### User stories and associated unit/service tests 
   1. As a manager I want to view reimbursement requests so I can start addressing them
       - Unit tests
           - approve request 
               - method: approveRequest()
           - deny request
               - method: denyRequest()
           - see all requests in the database
               - method: getAllRequests()
       - Service tests: N/A
        
   2. As a manager I want to view global reimbursement statistics so I can see how much money the company has given in reimburesments
       - Unit tests
           - View all the approved reimbursement 
              - method: getAllRequest() 
       - Service test 
           - make sure only approved requests are added to the total
              - method: checkApprovedRequest() 
              
   3. As a manager I want to view my reimbursement statistics so I can see how much money I have given in reimburesments
       - Unit tests
           - Approved requests by manager
              - method: getAllRequests()
       - Service test
           - Requests by other manager is not allowed
             - method: checkRequestApprovedBy()
            
   4. As an employee I want to create a reimbursement request so I can get money back I spent for the company
       - Unite tests
           - add new request to database
              - method: createRequest() 
         
       - Service test
           - requests should have unique identifier
              - method: createRequest() **database will handle this*
           - request is not less than 0 and not more than 1000$
              - method: checkRequestAmount()
           - reason of request no longer than 500 characters
              - method: checkRequestReson() 
              
   5. As an employee I want to view my reimbursement statistics so I can see how much money I have been given in reimburesments
      - Unit tests
          - view all my approved requests
             - method: getEmployeeApprovedRequests()
      - Service tests
          - N/A   
