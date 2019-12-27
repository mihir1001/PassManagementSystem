Pass Management System:

I have used Java, Spring Boot, Gradle, Postgres, Flyway , Postman to build this Project

1: I have created 3 Classes / Tables / Models Visible under Model Folder ( User, Pass, Vendor)
2: I created 3 Repositories For respective Models to Store Data ( Under Repository Folder)
3: I Have used Postgres Database to store the Data ( Check application.properties) And update values according to your Postgres Credentials 
4: I have used Flyway to for initial Set up of Data, I wrote 2 SQL files to one created All tables and one to Insert Vendor and User Data. I have created 5 Vendors and 10 Users. (Check resources -> db -> migration folder)
5: I have created One Controller which contains all of the following methods 
	(i) get all vendors data 
	(ii) get all users data 
	(iii) get all passes data
	(iv) add pass method to add pass to the system (vendors and users are preloaded, check step 4)
	(v) cancel pass method to delete / cancel the pass 
	(v) is active method to check if pass is active by checking its expiry date 
	(vi) renew method to renew pass by 1 year every time 
	(vii) vendor verification method is used to check if pass is valid for given vendor
6: Please check URL to access appropriate method 
7: I have created 1 Service class where resides all logic of updating passes
8: For testing I have used Validators to check all the inputs and if wrong input is entered then appropriate error message is  shows to help enter valid data ( Check Validator folder)
9: I have created Custom Exceptions to handle Exceptions generated in Step 8

Steps to Run Following Application
A: Unzip folder 
B: Change application.properties file and provide Postgres Credentials 
C: Start the Application and it should load User and Vendor data in your database 
D: use(localhost:8080/get-all-users) to see all users data 
E: use(localhost:8080/get-all-vendors) to see all vendors data
F: use(localhost:8080/get-all-passes) to see passes data ( Initially it will be empty as you will have to Add Passes)
G: use(localhost:8080/add-pass?vendorName=Boston_Travel&expireDate=27-12-2018&userId=200) to Add Pass 
H: use (localhost:8080/renew-pass?passId=1) to renew pass by a year 
I: use(localhost:8080/cancel-pass?passId=1) to cancel / delete pass
J: use(localhost:8080/is-active?passId=22) to check if pass is valid / hasn’t expired
K: use(localhost:8080/vendor-varification?passId=3&vendorId=50) to check pass is valid for given Vendor 

I hope you are able to run and see all the results if somehow you can not run the system to contact me.. 

Regards
