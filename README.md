# P.I.Works-challenge
Challenge for P.I. Works (Junior Software Product Design Engineer)

In the desired interface, the lists of the contacts will appear on the left side of the screen, and the contact adding or updating operations will be performed on the right side of the same screen. I divided the interface into 3 parts, I am going to explain them down below.

- Label 1
- Part 1
- Part 2

Label 1
======

 ```
 [+New User]     [ ] Hide Diasble User          [Save User]
```

---

- The "+ New User" button (left corner)  is a button that adds a new user.  To add this user database, the "Save User" button (right corner ) will be clicked. Besides, if we do not want to see databased people who are not enabled, a click button named "Hide Disabled User" will be placed.


Part 1
======



| ID      | User Name | Email                | Enabled |
| --------|:---------:|:--------------------:|---------|
| 1       | AdminUser | admin@piworks.net    | true    |
| 2       | Test User | testuser@piworks.net | true    |

---


- This part will cover the left side of the interface screen and it is the area where ID information and other information will appear in a list. Here, the desired results will be displayed in a list easily by filtering in the desired category (User Name, Phone, etc.). When a new person is added to the list or the person's information is updated, it will be displayed in this section. It will also be added to the sorting button. In order to view the people in the list easily, white background in a color suitable for our theme and a background in another color will be made. For the person to be updating or deleting will be done by right-clicking the mouse.

Part 2
======
```
New User
```
Username:
```
```
Display Name:
```
```
Phone:
```
```
Email:
```
```
User Roles:
```
[Select user roles...]
```    
```        
                            | Guest      |
                            | Admin      |
                            | SuperAdmin |
```

 Enabled: 
 ```
 [ ]
```
---

- Eventually, the information of the user will be entered into the new one in this section and the information of the existing user will be updated here. Turkish characters will not be used in the "Username" section. RegExr check will be made for the "Phone" and "Email" sections. One of the three alternatives should be select in the part of "User Role" section. A click button will be set for the "Enable" part.


In addition
======

- It is important to make Pixel Perfect when designing. The project interface to be made should be made by the colors or emblem of the company. While doing these, some programs should be using such as Sketch, Figma, or Adobe Illustrator. An interface that is not confusing to the user and practices should be designed. Nevertheless, with its Responsive design, it ought to be designed at which points it will break, at which points it will change, or how it should be transitioning. In the meantime designing the interface, it should be designed following the tablet, phone, or desktop devices to be used. In fact, they all work over the same address and all use the same code, it is only displayed differently with CSS and made harmonious. The localization of the design should be done well and the separation of roles should be made clear way.
 

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
