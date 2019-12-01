## Entry Management Web Application


A simple and beautiful web application for Entry Management in offices . It uses Postgresql Database in Backend , which is The World's Most Advanced Open Source Relational Database, along with nodejs and express.

Database Contains 4 Tables :-

                        
# Table Name : public.history

<pre>                    
Column Name     Type                             Constraints
id              bigint                        not null primary key
phone_no        character(10)                 not null
checkin_time    timestamp without time zone   not null
checkout_time   timestamp without time zone   
entry_gate      integer                       not null
exit_gate       integer                       
isemployee      boolean                       not null  
</pre>

# Table Name : "public.emp"

<pre>   
    Column            Type                        Constraints
 emp_id       integer                           not null  primary key
 first_name   character varying(80)             not null  
 last_name    character varying(80)             not null  
 email        character varying(80)             not null  
 phone_no     character(10)                     not null  
 designation  character varying(30)             not null  
</pre>

# Table Name : "public.visitor"                       
<pre>
    Column                Type                           Constraints 
 phone_no      character(10)                           not null primary key 
 email         character varying(80)                   not null          
 first_name    character varying(80)                   not null  
 last_name     character varying(80)                   not null  
 sex           character varying(8)                    not null  
 checkin_time  timestamp without time zone             not null  primary key
 </pre>


# Table "public.visit_summary"
<pre>
      Column                  Type                        Constraints

 phone_no          character(10)                           not null  
 checkin_time      timestamp without time zone             not null  
 person_to_visit   integer                                 not null  
 purpose_of_visit  character varying(100)                  not null  
</pre>

# It contains 4 rest api end points :-
<pre>
/employee/entry :- For making entry of employee... It checks whether input is
 valid employee id and then check entry before exit error.
/employee/exit  :- For making exit of employee... It checks whether input is
 valid employee id and then check exit before entry error.
/visitor/entry :- For entry of visitor it also stores the visitor details for   future reference. It email and sms host telling all Visitor's Details.
/visitor/exit :- For making exit of visitor. It Thanking emails and sms Vistor  telling complete visitor summary.
</pre>
<pre>

# For easy maintainence for the application 6 error codes are used....

0 :- Internal Server Error ..
     Error while querying the database.
     Error while connecting to database.
     Error while server fault.
     
1 :- Successful

2 :- Entry Before Exit

3 :- Exit Before Entry

4 :- Employee Does not exist

5 :- Employee is absent.
</pre>

# Scope for future development :-

1. Implementing Trie Data Structure to show the details of all employee in /visitor/entry page.
2. Adding Adhar card feature to fetch the details of visitor so to increase the visitor's comfort.
3. Use of RFID Card at gates to make system more reliable and accessible/

Thankyou Innovacer for giving me such a good project . I have learned a lot while completing it. 
Some things I learned are  Postgresql,es6 async await features,database management and little bit of 
jquery,nodejs,express.
