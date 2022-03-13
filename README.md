# Zoho-level1-assessment-Contacts-Manager-app
An application  to manage  Contact details using e-mail and secret password.
# Steps to run the application
1. First of all, ensure that you have the latest version NodeJS, NPM and MongoDB installed on your system.

2. Clone the github repository on your local system using the command :

       git clone https://github.com/Akshathachaya/Zoho-level1-assessment-Contacts-Manager-app.git

3. Locate the root folder of the application on your terminal using the command.
        
       cd Zoho-level1-assessment-Contacts-Manager-app

4. Install all the dependencies using the following command:
       
       npm install

5. Ensure that you have a running MongoDB server on a different terminal tab. For information
   on how to setup and run a MongoDB server refer the 
   following documentation https://docs.microsoft.com/en-us/windows/wsl/tutorials/wsl-database (goto "Install MongoDB").

6. Now run this command on your terminal

       npm start 

7. Open a brower tab and type the following command on the search bar and press enter.
  You can see the application running on your browser.
       
       localhost:3000/signup 

 Alternatively you can also visit https://contacts-management.herokuapp.com/signup to see the deployed application.

# Description of various code blocks
 > The routes folder contains two files.

* auth.js - Contains the code that handles all the requests relating to the authentication i.e. Sign In, Sign Up and Sign out.

* index.js - Contains the code that handles storing the contacts into the database as well as displaying the appropriate contacts according to the signed in user.

* The index.js file also contains this middleware function which is used to check if any user is currently signed in or not. If a user is currently signed in then the function redirects to carries on to display the required page else it redirects to the sign in page

       
       function isLoggedIn(req, res, next){
         if(req.isAuthenticated()){
            return next();
         }
         res.redirect("/signin");
      } 
> The models folder contains two files.

* contact.js - contains the mongoose schema for the stored contact details.

* user.js - contains mongoose schema for the users of this application.

> The views/index directory contains the HTML markup for showing the Sign In, Sign Up and Contacts form and Contacts List pages

> The views/partials directory contains the header and footer sections of the HTML boilerplate.

> The app.js file is the entry point of this application which is used to setup all the frameworks used in this application.

# Screenshots
![image](https://user-images.githubusercontent.com/90977508/158030644-9d67a216-1b46-4435-9cdc-3edaf3c11d3d.png)

                                          Contact Form and Contact List Page


![image](https://user-images.githubusercontent.com/90977508/158030721-0f64ae45-5339-4488-b3d2-0981fa1e82cc.png)
                                                    
![image](https://user-images.githubusercontent.com/90977508/158030813-81beaf1a-f2fb-4349-9d1a-2b26bc8fcf92.png)
                                          
                                           
