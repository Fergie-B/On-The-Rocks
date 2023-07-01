# On the Rocks | A Cocktail Making Class Booking System and Blog Website

[Am I responsive] (docs/)

**Developer: Barry Ferguson**
 
 ## Table of Contents
 
 - [About the Site](#about-the-site)
 
 - [User Experience](#user-experience)
    * [Target Audience](#target-audience)
    * [User Requirements and Expectations](#user-requirements-and-expectations)
    * [User Goals](#user-goals)
    * [Site Owner Goals](#site-owner-goals)
    * [User Stories](#user-stories)
        - [EPIC 1 Site Navigation and Design](#epic-1-site-navigation-and-design)
        - [EPIC 2 CRUD Functionality](#epic-2-crud-functionality)
        - [EPIC 3 Site Administration](#epic-3-site-administration)
        - [EPIC 4 Site Register and Logging](#epic-4-site-register-and-logging)
        
  - [Project Managment](#project-management)

  - [Database Schema](#database-schema)
     * [Models](#models)
        - [User Model](#user-model)
        - [Sessions Model](#sessions-model)
        - [Booking Model](#booking-model)
        - [Post Model](#post-model)
        - [Comment Model](#comment-model)
        - [Category Model](#category-model)
        - [Contact Model](#contact-model)

  - [UI Design](#ui-design)

  - [Features](#features)

  - [Future Features](#future-features)


 
## About the Site
 On the Rocks is a Cocktail Recipe blog and website where users can find and read Cocktail recipes, and by creating an account can post their own recipes and comment on the site content.
 <hr>
 
## User Experience
 
### Target Audience
- Adult users that wish to find a cocktail to make
- Adult users that want to post and share a cocktail that they have made
- Adult users that want find a cocktail to make for the Spirits they have to hand
- Hospitality Industry staff looking to research cocktail types for customers requests
- Hospitality Industry staff that want to post cocktails they have made to increase awareness of their premises

### User Requirements and Expectations
- Fully Responsive on all devices
- Accessibility
- User Friendly interface design
- Social Media presence
- Ability to contact the site administrators
 
### User Goals
- To be able find new cocktails to make
- To be able to find cocktails that match the Spirits they have in stock
- To be able to view and interact with Blog Posts
- To be able to post to a Blog
- To be able to contact the Site Administrators
  
### Site Owner Goals
- Provide a fuly responsive website
- Provide a site that meets WCAG accessibility requirements
- Provide a facility to allow Cocktail enthusiast to post recipes and interact with one another online

### User Stories

#### EPIC 1 Site Navigation and Design

##### Site Navigation
- As a **User** I can **navigate the site with ease** so that **I can find the information that I am looking for** (Must Have)
- As a **User** I can **utilise the sites inbuilt Navbar, Footer and Social Media Links** so that **I can access the site links, pages and social media presence** (Must Have)
- As a **User** I can **view a list of cocktail recipes** so that **I can make my choice of which one to read** (Must Have)
- As a **User** I can **access a list of cocktail recipes filtered by type of spirit** so that **I can find a cocktail to make from the Spirits I have to hand** (Must Have)
- As a **User** I can **search for an ingredient** so that **I can find a cocktail to make from the ingredients I have to hand** (Should Have)

##### Site Design
- As a **User** I can **browse a fully responsive website** so that **I can view the blog on any device** (Must Have)
- As a **User** I can **browse an accessible website** so that **I can view a site that meets WCAG accessibility requirements** (Must Have)

#### EPIC 2 CRUD Functionality

##### User Recipes
- As a **User** I can **add a Cocktail recipe to the blog** so that **other users can view it** (Must Have)
- As a **User** I can **update or delete my recipe posts** so that **edits can be made to my recipes going forward** (Must Have)
- As a **User** I can **create a draft post** so that **I can save my work and edit it later** (Must Have)
- As a **User** I can **tag my cocktail recipe posts** so that **they are searchable and can be grouped with other similar cocktail recipes** (Should Have)
- 
##### User Interaction
- As a **User** I can **like a cocktail recipe post or article** so that **I can browse it later** (Must Have)
- As a **User** I can **make comments on cocktail recipes** so that **I can provide feedback to other users**(Must Have)
- As a **User** I can **update and edit comments I have made** so that **I can edit any possible inaccuracies in my comments** (Must Have)
- As a **User** I can **view likes on posts** so that **I can see how popular a Cocktail is in other users opinions** (Must Have)
- As a **User** I can **like comments on recipes** so that **I can express gratitude to other users for commenting on my posts** (Must Have)
- As a **User** I can **use a contact form on the site** so that **I can contact the site administrator to raise any issues or seek information** (Must Have)

#### EPIC 3 Site Administration
- As a **Site Administrator** I can **create, read, update and delete posts and comments** so that **so that I can manage the sites content if any is deemed inappropriate** (Must Have)
- As a **Site Administrator** I can **mark recipes as featured content** so that **so that I can highlight users input to the blog any encourage a sense of community on the blog** (Must Have)

#### EPIC 4 Site Register and Logging
- As a **User** I can **register a user account on the site** so that **I can create and interact fully with the sites content** (Must Have)
- As a **User** I can **log in and out of the site** so that **I can like and comment on cocktail recipe posts, and compose my own content** (Must Have)
- As a **User** I can **log into the site** so that **I can book a class** (Must Have)
- As a **User** I can **view my login status** so that **I can determin if I am logged in or out of the site** (Must Have)

[Back to top ⇧](#table-of-contents)

## Project Management
- Github projects was utilised in the project management of the development process. The project's Kanban board can be viewed [here](https://github.com/users/Fergie-B/projects/5)
- 4 Epics were created: Site Navigation and Design, CRUD Functionality, Site Administration and Site Register and Logging - Site Navigation and Design, and CRUD Functionality were further broken
down into Site navigation, Site Design, User Recipes and User Interaction to better visualize the tasks
- MoSCoW Prioritization was utilised to prioritize issues in the Epics that were Must Have and Should Have needs for the application

## Database Schema

### Models 

#### User Model

| Key        | Name         | Type        |
| ---------- | ------------ | ----------- |
| PrimaryKey | user_id      | AutoField   |
|            | password     | VARCHAR(40) |
|            | last_login   | VARCHAR(40) |
| 	          | is_superuser | BOOLEAN     |
| ForeignKey | username     | VARCHAR(40) |
|            | first_name   | VARCHAR(40) |
|            | last_name    | VARCHAR(40) |
|            | email        | VARCHAR(40) |
|            | is_staff     | BOOLEAN     |
|            | is_active    | BOOLEAN     |
|            | date_joined  | VARCHAR(40) |


#### Post Model

| Key        | Name           | Type      |
| ---------- | -------------- | ----------|
| PrimaryKey | post_id        | AutoField |
| ForeignKey | author         | User Model|
|            | created_on     | DateTime  |
| 	          | updated_on     | DateTime  |
|            | description    | TextField |
|            | method         | TextField |
|            | ingredients    | TextField |
|            | featured_image | Cloudinary|
|            | excerpt        | TextField |
|            | slug_unique    |           |
|            | status         | intField  |
|            | category       | Char(255) |

#### Comment Model

| Key        | Name         | Type                            |
| ---------- | ------------ | ------------------------------- |
| PrimaryKey | comment_id   | AutoField                       |
| ForeignKey | post         | Post model Cascade on delete    |
|            | name         | Char(80)                        |
| 	          | email        | EmailField                      |
|            | body         | TextField                       |
|            | created_on   | DateTimeField auto_now_add_true |
|            | approved     | BooleanField default False      |

#### Category Model

| Key        | Name         | Type                         |
| ---------- | ------------ | ---------------------------- |
| PrimaryKey | category_id  | AutoField                    |
| ForeignKey | post         | Post model Cascade on delete |
|            | created_at   | GuestModel                   |
| 	          | updated_at   | GuestModel                   |
|            | title        | Char(255)                    |


#### Contact Model

| Key        | Name         | Type       |
| ---------- | ------------ | ---------- |
| PrimaryKey | contact_id   | AutoField  |
| ForeignKey | name         | GuestModel |
| ForeignKey | email        | GuestModel |
| ForeignKey | phone        | GuestModel |
| ForeignKey | body         | TextField  |


[Back to top ⇧](#table-of-contents)

## UI Design
 
[Back to top ⇧](#table-of-contents)

## Features

### Home page
Includes
- Header
- Main Body
- Footer

### Header
Includes
- Logo
- Navigation Bar
- Search Field

#### Navigation Bar
Includes Links
- Home
- Recipes Dropdown
  - Vodka
  - Whiskey
  - Rum
  - Gin
  - Tequila
- Blog
- Contact Us
- Register
- Login/Logout

#### Logo
Custom Logo Designed by myself in Adobe Illustrator

#### Search Field
Search Field in header to alow the user to search for pertinient terms

<hr>

### Footer
Includes
- Social Media Links
- Copyright Disclaimer

#### Social Media Links
Includes
- Font Awesome Icon Link to Twitter.com
- Font Awesome Icon Link to my LinkedIn profile
- Font Awesome Icon Link to my GitHub profile

<hr>

### Recipes
- This page displays all published recipes from the blog by most recent first
- The Filtered list in the recipes dropdown displays all published recipes by the chosen ingredient link
- A Card displays the cocktail image, and Title.
- Clicking inside the card will display the recipe posting

#### Recipe Detail Page
- These pages display the cocktail recipe posting in detail
Includes
 - Title
 - Short Description
 - Author Name
 - Published date
 - Add Comment Link
 - Featured Image
 - Introduction text
 - Ingredients
 - Method/Steps
 - Comment Form

### Blog
- This page displays all published blog post by most recent first
- A Card displays the blog posting image, and Title.
- Clicking inside the card will display the blog posting

#### Blog post Detail Page
- These pages display the blog post/cocktail recipe posting in detail
Includes
 - Title
 - Short Description
 - Author Name
 - Published date
 - Add Comment Link
 - Featured Image
 - Introduction text
 - Ingredients
 - Method/Steps
 - Comment Form

#### Comments

#### Categories

<hr>

### Register

### Login

### Logout


<hr>

### Contact Us

### 404 Page

[Back to top ⇧](#table-of-contents)
