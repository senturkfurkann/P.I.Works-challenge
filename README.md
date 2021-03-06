# P.I.Works-challenge
Challenge for P.I. Works (Junior Software Product Design Engineer)
#### Requirements
- New screen design on FrontEnd side
- Adding new methods on BackEnd side as a CreateUser, UpdateUser and GetAll methods.
- 2 tables should be created on the DB side.

Define Username and Display Name as VARCHAR (size) on the back and assign 100 characters. After that, Phone and Email parts should be defined as TEXT (size).

Expressions need to be checked on the front of the screen. Even if the phone accepts more than one format, it should be sent to the service registered on the back in the following format. RegExr checks should be done.

90/500/000/0000
Mail Expression
^\S+@\S+$

Phone Expression
/^[0-9]*^[()-]*$/


For TABLE2, UserType (User roles such as Guest, Admin or Superadmin) must be defined as an ID assigned and the number that comes to each ID.

TABLE1
ID  	Username	Display Name	Phone	 Email	    UserRolesId	Enabled	Record
8345	aaaa	    eeee	         679941	 aa@g.com	1	        true	null
3535	bbbb	    ffff	         384752	 ab@g.com	2	        true	null
9068	cccc	    gggg	         569783	 ac@g.com	3	        true	null
5345	dddd	    hhhh	         498549	 ad@g.com	2	        true	null

TABLE2	
ID	RoleCode
1	Admin
2	Guest
3	SuperAdmin

In addition, soft deletion should be done according to space/fullness ratio of the records. Record field should be filled, Record IsNull check should be done in Backend request for users to be shown on the screen.