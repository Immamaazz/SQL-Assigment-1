# SQL-Assigment-1
Problem 1. Please create the following tables for a helpdesk ticket database withappropriate primary keys & foreign keys. Please include drop table statements (withcascade constraints) in the beginning. [50 points]Assumptions: You will create a set of tables for managing an IT helpdesk ticket system.1. Clients can submit tickets.2. Each ticket is associated with a topic. Topics form an hierarchy where each topicmay have a parent topic (the top level topic does not have parent).3. Each ticket will be assigned to a support staff.4. Interactions between support staff and a client about a ticket will be recorded in aticket_detail table

Tables and columns:
client table: information about a client who submits ticket
- clid -- client ID
- clname -- client name
- clemail -- client email
support table: information about supporting staff
- sid -- support id
- sname -- support name
- semail -- support email
topic table: topics of problems, a topic can have a parent topic
- tid -- topic id
- tname -- topic name
- ptid -- parent topic id, points to an existing topic as parent
ticket table: ticket being submitted
- tkid -- ticket id
- clid -- client id
- tid -- topic id
- sid -- assigned support id
- tktime -- ticket submission time
- rstime -- resolved time
- status -- current 
- status: 1 submitted, 2 assigned, 3 resolved.
- description --- description of problemticket_detail 
table: detail communication about a ticket
- tdid -- ticket detail id
- - tkid -- ticket id
- sid -- support who entered the record
- - tdtime -- timestamp for this record
- content -- content of the communication
- Problem 2. Insert at least three rows of data to each table. Make sure you keep theprimary key and foreign key constraints. use select * statements to return data inserted in each table
