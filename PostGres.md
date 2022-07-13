# Tech-Project Database
    endpoint:techproject.cumkbny97iwq.us-east-1.rds.amazonaws.com
    Db name:techproject
    user:techproject
    password:techproject
   
    
# Create Tables DDL

    DROP TABLE IF EXISTS employees;

    DROP TABLE IF EXISTS requests;

    CREATE TABLE employees(
    employee_id INT GENERATED ALWAYS AS IDENTITY,
    employee_name VARCHAR(255) NOT NULL,
    employee_role VARCHAR(255) NOT NULL,
    PRIMARY KEY(employee_id)
    );

    CREATE TABLE requests(
    request_id INT GENERATED ALWAYS AS IDENTITY,
    employee_id INT,
    request_desc VARCHAR(500),
    reason VARCHAR(500),
    amount INT,
    status VARCHAR(50),
    PRIMARY KEY(request_id),
    CONSTRAINT fk_employee
        FOREIGN KEY(employee_id) 
        REFERENCES employees(employee_id)
    );


    select * from employees;

    select * from requests;

# Insert Update Delete  DML 

    select * from employees;

    insert into employees values (default, 'Manager', 'Manager');
    insert into employees values (default, 'employee1', 'employee');
    insert into employees values (default, 'employee2', 'employee');
    insert into employees values (default, 'employee3', 'employee');
    insert into employees values (default, 'employee4', 'employee');


    select * from requests;

    insert into requests values (default, 1, 'shopping', 'for company', 200, 'pending' );
    insert into requests values (default, 1, 'shopping', 'personal', 400, 'Denied' );
    insert into requests values (default, 2, 'shopping', 'for company', 700, 'Accepted' );
    insert into requests values (default, 2, 'shopping', 'for company', 1200, 'pending' );

# Grant Control for manager and employees
  
    create user manager;
    create user employee;

    alter user manager with password 'manager';
    alter user manager with password 'employee';

    grant select, update, insert,delete on employees to manager;

    grant select, update, insert,delete on requests to manager;

    grant select, insert,delete on requests to employee;

    revoke select, update, insert, delete on employees from employee;
