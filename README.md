# Project1-events
-------------------------------
StartDate : July-10-2017

Template:https://startbootstrap.com/template-overviews/sb-admin/Objective : 
Objective: Event registration.
1> Create members login pages. User Logs in registers events and adds email addresses for the event email to be sent.
b. All entered email-id’s get a temporary guest id generated 
c. Guest gets a link on the email with From and the Subject – Guest Accepts, Tentative or Declinesd. Accepts : Guest’s email address gets stored and Phone number is required for confirmation(Optional)e. Declines/Tentative : Popup opens and the guest can specify a reason for declining DB : 

Tables :CREATE TABLE ALL_Users(U_ID         INT(10),U_EMAIL                                   VARCHAR(25),U_PASSWD                                  VARCHAR(25),U_MFA                                     VARCHAR(25),U_SecurityQ                               VARCHAR(30),CONSTRAINT User_PrimKey PRIMARY KEY (U_ID ,U_EMAIL));
CREATE TABLE Events(Ev_ID     INT(10),U_ID                                    INT(10),Ev_Name                                 VARCHAR(25),Ev_Desc                                 VARCHAR(25),Ev_Type                                 VARCHAR(30),Ev_Contact    VARCHAR(25),Ev_StartTime                            DATETIME,Ev_EndTime                              DATETIME,Ev_Status                               VARCHAR(25),CONSTRAINT Event_PrimKey PRIMARY KEY (Ev_ID)CONSTRAINT FK_User_primKey FOREIGN KEY (U_ID) REFERENCES all_users(U_ID));
--------------------------------------------------------
CREATE TABLE User_details(U_ID         INT(10),FNAME                                     VARCHAR(30),LNAME                                     VARCHAR(30),ADDRESS                                   VARCHAR(200),STATE                                     VARCHAR(25),CITY                                      VARCHAR(20),ZIP                                       VARCHAR(10),PHONE                                     VARCHAR(15),COUNTRY                                   VARCHAR(30),PROFESSION                                VARCHAR(25)Key);
