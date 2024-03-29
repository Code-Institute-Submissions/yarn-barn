# Yarn Barn
![Mock-up of site](static/images/mock-up.png)
## Goal for this Project

Have you ever wondered what yarn is going to be best for your next project? Is a yarn value for money? How easy is a yarn to work with? Well look no further as at Yarn barn you can search an review yarns to make a more informed decision on the yarn for your next project.

---
## Table of contents 
* [UX](#ux)
    * [Site Owners Goals](#site-owners-goals)
    * [User Goals](#user-goals)
    * [User Stories](#user-stories)
    * [User Requirements and Expectations](#user-requirements-and-expectations)
    * [Design Choices](#design-choices)
* [Wireframes](#wireframes)
* [Features](#features)
    * [Existing Features](#existing-features)
    * [Features to be implemented](#features-to-be-implemented)
* [Technologies used](#technologies-used)
* [Testing](#testing)
* [Bugs](#bugs)
* [Deployment](#deployment)
* [Credits](#credits)
---

## UX Design

### Site Owners Goals
* to create a library of yarns with reviews for future projects

[Back to Top](#table-of-contents)

### User Goals
* to make an informed choice of yarn for the next project
* to see what other crafters think about potential yarns
* to review yarns that the user has worked with

[Back to Top](#table-of-contents)

### User Stories

* As a user, I want to be able to easily navigate the site
* As a user, I want to be able to leave a review of a yarn that I have worked with to help other crafters.
* As a user, I want to be able to register for an account
* As a user, I want to be able to log in and out of the site to leave reviews.
* As a user, I want to be able to add yarns to the library.
 
[Back to Top](#table-of-contents)
### User Requirements and Expectations
### Requirements
* Users requires easy navigation of site
* Easy to use search function
* Images of yarns being reviewed
* Users want to be able to leave their own reviews

### Expectations

* An easy to navigate site
* Yarn reviews on a variety of yarns
* Ability to add the the library of yarns

[Back to Top](#table-of-contents)
## Design Choices

I used [coolers](https://coolors.co/) to help select a color palette for the site.
I selected a variety of bright pastel colors as it is calming yet engaging at the same time.

![color palette](static/images/YarnBarnColourPalette.png)

* Color #F28428 will be used as the main background color
* Color #84A59D will be used for the nav bar as it is in high contrast to the main page color
* Color #F6BD60 will be used as a border color to highlight images and text areas

Ultimately I decided against using the ligh pink colours and stayed with the bolder oranges and greens keeping the site bright and fun. Over time the colour might change seasonally but the oranges reflect the summer/ autumn season that we are currently in.
### Fonts

I have used [Google Fonts](https://fonts.google.com/) for  the fonts used for this site, I have chosen AmaticSC for the Title font and Roboto for the main text used.


[Back to Top](#table-of-contents)

## Wireframes
I decided to use [Balsamiq](https://balsamiq.com/) to make the wireframes, theay can be viewed below.
## Desktop Wireframes

[Home Page](Wireframes/HomePageDesktop.png)

[Login Page](Wireframes/LoginDesktop.png)

[Registration Page](Wireframes/RegistrationDesktop.png)

[Profile Page](Wireframes/ProfileDesktop.png)

[Yarn Reviews](Wireframes/YarnReviews.png)

## Tablet Wireframes

[Home Page](Wireframes/YarnBarnHomeTablet.png)

[Login Page](Wireframes/YarnBarnLoginTablet.png)

[Registration Page](Wireframes/YarnBarnRegistrationTablet.png)

[Profile Page](Wireframes/YarnBarnProfileTablet.png)

[Yarn Reviews](Wireframes/YarnBarnYarnsTablet.png)

## Mobile Wireframes

[Home Page](Wireframes/YarnBarnHomeMobile.png)

[Login Page](Wireframes/YarnBarnLoginMobile.png)

[Registration Page](Wireframes/YarnBarnRegistrationMobile.png)

[Profile Page](Wireframes/YarnBarnProfileMobile.png)

[Yarn Reviews](Wireframes/YarnBarnYarnsMobile.png)


I used [draw.io]() to create a flowchart for how I paln to make the functions work
[Flowchart](Images/YarnBarnFlowchart.drawio.png)

## Database

I chose to use MongoDB for my database and set it up with the following collections:

### Users

| Key | Value |
|---- | ----- |
| _id | ObjectId |
| username | string |
| password | string |

### Yarns

| Key | Value |
|---- | ----- |
| _id | ObjectId |
| yarn_name | string |
| yarn_producer | string |
| yarn_weight | string |
| yarn_colour | string |
| yarn_review | string |
| created_by | string |



[Back to Top](#table-of-contents)
## Features
### Existing Features

* Registration Functionality
* Sign in and sign out function
* CRUD functions
    * CREATE: create a review/comment about a yarn and add it to the database.
    * READ: look up and read about yarns in the library.
    * UPDATE: Add reviews/ comments to existing yarns.
    * DELETE: Delete a yarn entirely.


[Back to Top](#table-of-contents)
### Features to be implemented 

* an 'About me' section on the profile page
* a search function to look up particualr producers or yarn types.
* the ability to like/favourite yrans that you can then see in your profile so be able to refer back to them
* a where to buy yarns from section

[Back to Top](#table-of-contents)

## Technologies Used

### Languages

* HTML
* CSS
* JavaScript
* Python

### Libraries and Frameworks

* [Google Fonts](https://fonts.google.com/)
* [Font Awesome](https://fontawesome.com/)
* [Bulma](https://bulma.io/)
* [Coolers](https://coolors.co/)
* Flask
* PyMongo
* Jinja
### Tools

* Git
* Gitpod
* Heroku
* MongoDB Atlas
* Balsamiq
* W3C HTML Validataion Service
* W3C CSS Validation Service


[Back to Top](#table-of-contents)

## Testing

### As a user, I want to be able to easily navigate the site
#### Navbar
#### Plan
The navbar can be seen on larger screens but on small screens is too crowded so will have a burger dropdown menu.

#### Results
The burger element of the navbar was trickier to implement than I initially realised buut ultimatley works well, the burger on the small mobile screen size keeps the look of the site clean and consistent. All items from the nav appear in the dropdown menu so all functionality is available on small devices as well as large screens.
the nav bar keeps all the navigation elements in one place so the user will be able to move through the site with ease.

### As a user, I want to be able to register for an account
### Registration/ Sign Up
#### Plan
There will be a form to fill in to create a username and password. When the form is filled in correctly then there will be a flash message for the user to show succes and they will be redirected to their profile page. If the username already exists the user will be shown a message to say that name is already in user and redirected to the sign up page to choose another one.

#### Results
After a giltch with the connection with Mongo URI this function is now fully working I have tested it by setting up usernames and also by trying to set up an account with an exicstung username to check that the messages are correctly shown for the user.
During Testing I also found that I had forgotten to add the required class to the username and password fields meaning that if you hit the submit button and the firlds were empty the whole site crashed! After adding the needed fields the function works as expected.


### As a user, I want to be able to log in and out of the site to leave reviews.
### Login/ Log out functionality
#### Plan
The user will be able to login to the site as well as logout when finished using the site.
#### Results
There are clear buttons in the navbar to log in and out of the site, both functions work correctly and have been tested by myself and others to access accounts created.

### As a user, I want to be able to add yarns to the library.
### Add a Yarn
#### Plan
The user will be able to add new yarns to the library.
#### Results
In the navbar there is a link to the form to fill in with infromation about a yarn that a user wants to add to the library.
I have tested that the function pushes the infromation to the database and other users have added yarns to the library as well.
### Update Yarn
#### Plan
Users should be able to update yarn records with additional information or corrections to information on the cards.
#### Results
There is an edit button on each yarn card so that the user can update yarns with ne information or correct any information that is incorrect. But I then decided that it would be better if the user could only update records that they had created, as a security measure so that a user couldn't log in and just change every record. This has been tested by myself and other users.

### Delete A Yarn
#### Plan
Users can delete a yarn.
This was an additional function that I decided to add in case a yarn was discontinued.
#### Results
There is now a function to delete yarns from the library wich I have tested. As with the edit function a user can only edit or delete a yarn that they created. This means that a user caouln't just ogin and delete all the record in the library.

[Back to Top](#table-of-contents)
## Bugs
### Registration/sign in function
When writing this function its initially wouldn't work despite the Python code being correct after searching through the code, with the help of a Tutor as second set of eyes we found that the password in the MONG_URI was not working so I reset the password for the admin and linked it up again. After this the registration function worked correctly and new users were saved to the database.
### Login function
The login function was not redirevting through to the profile page, this was due to an error in my coding where I had forgotten to pass in the username perameter to the redirect function. It now works fine.
### Adding a new yarn
Whilst the function was working the yarn producer name was not pulling through from the database, on closer insepction of my code I found that I had misspelt the key name so corrected this and then all the infromation was moving to and from the database correcty.
### Navbar
Hamburger icon was not working. This was due to an error in the javascript that I had written for it I had passed the element the wrong id, once this was corrected then the function workd.
This then threw another glitch as it was showing an error on the home page where the burger was not present as such I wrapped the function within an if statement so that the function could only be called whe the burger was present on the page. 
### Heroku app not connected to Database
During testing it came to light that the Heroku app was not connected to the Mongo database this was probably due to the earlier error with the Mongo URI in the registration function.To over come this I re-entered the details needed into the config vars and the app and database are now able to connect.

[Back to Top](#table-of-contents)
## Deployment
### Local Deployment

I have created the Dog Health Tracker project using Github, from there I used [Gitpod](https://gitpod.io/) to write my code. 
Then I used commits to git followed by "git push" to my GitHub repository. 
I've deployed this project to Heroku and used "git push heroku master" to make sure my pushes to GitHub were also made to Heroku. 

This project can be ran locally by following the following steps: (
I used Gitpod for development, so the following steps will be specific to Gitpod. 
You will need to adjust them depending on your IDE. You can find more information about installing packages using pip and virtual environments [here](https://packaging.python.org/guides/installing-using-pip-and-virtual-environments/)


To clone the project: 

1. From the application's repository, click the "code" button and download the zip of the repository.
    Alternatively, you can clone the repository using the following line in your terminal:

    ``` 
    git clone https://github.com/AnoukSmet/Dog-Health-Tracker.git
    ``` 

1. Access the folder in your terminal window and install the application's [required modules](https://github.com/AnoukSmet/Dog-Health-Tracker/blob/master/requirements.txt) using the following command:

    ```
    pip3 install -r requirements.txt
    ```

1. Sign-in or sign-up to [MongoDB](https://www.mongodb.com/) and create a new cluster
    * Within the Sandbox, click the collections button and after click Create Database (Add My Own Data) called dog_health_tracker
    * Set up the following collections: users, dogs, logs, food_metrics and weight [Click here to see the exact Database Structure](#database-structure)
    * Under ***food_metrics*** and ***weight_metrics***, add your preferred metrics in the collection with the following structure: 
        ```
        Key             | Value
        ----------------|-----------
        _id             | ObjectId          This will be automatically generated by MongoDB
        metric_name     | String            Replace string by kg, pounds, grams, ounces etc.
        ```

    * Under the Security Menu on the left, select Database Access.
    * Add a new database user, and keep the credentials secure
    * Within the Network Access option, add IP Address 0.0.0.0

1. In your IDE, create a file containing your environmental variables called env.py at the root level of the application. 
    It will need to contain the following lines and variables:
    ```
    import os
    os.environ["IP"] = "0.0.0.0"
    os.environ["PORT"] = "5000"
    os.environ["SECRET_KEY"] = "YOUR_SECRET_KEY"
    os.environ["DEBUG"] = "True"
    os.environ["MONGO_URI"] = "YOUR_MONGODB_URI"
    os.environ["MONGO_DBNAME"]= "DATABASE_NAME" 
    ```

    Please note that you will need to update the **SECRET_KEY** with your own secret key, as well as the **MONGO_URI** and **MONGO_DBNAME** variables with those provided by MongoDB.
    Tip for your SECRET_KEY, you can use a [Password Generator](https://passwordsgenerator.net/) in order to have a secure secret key. 
    I personlly recommend a length of 24 characters and exclude Symbols.
    To find your MONGO_URI, go to your clusters and click on connect. Choose connect your application and copy the link provided. 
    Don't forget to update the necessary fields like password and database name. 

    If you plan on pushing this application to a public repository, ensure that env.py is added to your .gitignore file.

1. The application can now be run locally. In your terminal, type the following command 
    ```
    python3 app.py. 
    ```

### To deploy your project on Heroku, use the following steps: 

1. Login to your Heroku account and create a new app. Choose your region. 
1. Ensure the Procfile and requirements.txt files exist are present and up-to-date in your local repository.  
    Requirements:
    ```
    pip3 freeze --local > requirements.txt
    ```
    Procfile:
    ```
    echo web: python app.py > Procfile
    ```
1. The Procfile should contain the following line:
    ```
    web: python app.py
    ```

1. Scroll down to "deployment method"-section. Choose "Github" for automatic deployment.
1. From the inputs below, make sure your github user is selected, and then enter the name for your repo. Click "search". When it finds the repo, click the "connect" button.
1. Scroll back up and click "settings". Scroll down and click "Reveal config vars". Set up the same variables as in your env.py (IP, PORT, SECRET_KEY, MONGO_URI and MONGODB_NAME):
    !You shouldn't set the DEBUG variable in under config vars, only in your env.py to prevent DEBUG being active on live website. 

    ```
    IP = 0.0.0.0
    PORT = 5000
    SECRET_KEY = YOUR_SECRET_KEY
    MONGO_URI = YOUR_MONGODB_URI
    MONGO_DBNAME = DATABASE_NAME
    ```

1. Scroll back up and click "Deploy". Scroll down and click "Enable automatic deployment".
1. Just beneath, click "Deploy branch". Heroku will now start building the app. When the build is complete, click "view app" to open it.
1. In order to commit your changes to the branch, use git push to push your changes. 


[Back to Top](#table-of-contents)
## Credits
Thanks as always to Simen [Eventyret_mentor](https://github.com/Eventyret) who has helped me through this project with helpful and insightful tips on what I've been trying to make! Thanks also to the awesome [Code Institute](https://codeinstitute.net/) tutors (especially Johann, who are there for you when ever you get stuck along the way.
Thanks to [Unsplash](https://unsplash.com/)for making their images available.
Thanks to the [Stackoverflow](https://stackoverflow.com/) for a great community always happy to help.
My family and friends have been a huge support in this this project as I may have overcommitted myself so Thanks for letting me bailout to go write code!

[Back to Top](#table-of-contents)

