# journi

## Goal

Design a social media where people can share their trips with an online community which incorporates maps and ratings. 

Group project with [Preston Ng](https://github.com/sungchun) and [Reisli Hysa](https://github.com/ReiHysa).


## Timeframe

Timeframe: 1 week.


## Project Overview

My third project on the General Assembly Software Engineering Immersive course at General Assembly and my first group project. 

We were inspired to create something which circulated around social media with a strong influence centred around the feed and using a map API.

<!-- video -->

## Deployment 

The website can be viewed here, however, we have found out that the api only works locally:

https://journi-media.herokuapp.com/login


## Getting Started

1. Clone or download the repo in your CLI.
2. Install dependencies `npm i`.
3. Start the database on your CLI with `mongod --dbpath ~/data/db`, close the terminal, then open again and use `mongosh`.
4. Open the backend folder and start server using nodemon `yarn start`.
5. Change into front-end folder `cd frontend`.
6. Run the frontend with `npm start`.

## Technologies Used

* MongoDB
* Mongoose
* JavaScript
* ReactJS
* Express
* NodeJS
* CSS3
* Bootstrap
* VS Code
* Chrome
* Google Fonts
* Git and GitHub

## Planning and Pseudocode

As we learnt through the course, it is best practice to start with a pseudocode.

<p align='center'>
    <img width='310' height='400' src='https://user-images.githubusercontent.com/60261970/149829138-bf29fa87-e25e-4c9b-b34b-354dbf4c3d1b.png'>
  <img width='310' height='400' src='https://user-images.githubusercontent.com/60261970/149829143-cd703d50-b7bc-4d40-8613-3496e2979caa.png'>
  <img width='310' height='400' src='https://user-images.githubusercontent.com/60261970/149829149-6af4055f-bec2-4cef-be7d-1abb7dbb25e6.png'>
</p>

And we had a wireframe to show how we wanted the home page to look like:
<p align='center'>
    <img width='500' height='320' src='https://user-images.githubusercontent.com/60261970/149829460-21284d69-dba2-44da-83ff-a2687d4fbfb2.png'>
</p>


### Work Split 

#### Backend

* As a team we did the backend together, following guidance from previous homework from the Bootcamp.
* On the backend we created our own database with a few posts and main users.

<p align='center'>
    <img width='760' height='320' src='https://user-images.githubusercontent.com/60261970/149957335-49812daa-52cd-4e5c-b685-2ad2d1b46f82.png'>
    <img width='450' height='440' src='https://user-images.githubusercontent.com/60261970/149958279-3fe79121-abd8-49e7-bbbd-35c4cd161c86.png'>
</p>

* Register and Login.

    * Register function will create a new User in the database, using `.create`, and welcoming the new user when the registration is successful.
    * Login function will look for the User username in the database and check if the password is valid, if valid it will assign a token for the user for 7 days, if not will return an 'unauthorised' message.

<p align='center'>
    <img width='440' height='220' src='https://user-images.githubusercontent.com/60261970/149964175-3ef29ed0-72c4-47f1-b520-09ab59829c5d.png'>
    <img width='460' height='300' src='https://user-images.githubusercontent.com/60261970/149964202-62442df2-38d5-41b4-94e5-28323fabe08b.png'>
</p>

* Follow/Unfollow functions.

    * Follow function will check the User id with `.findById`, check if the user already follow that account, if not it will use `push` and `save` to 'following' and 'followers', and 'me' and 'profileToFollow' variables.
    * Unfollow function will check if the user follows that account, and then will use `indexOf` and `splice` to remove the user account from the other followers count.

<p align='center'>
    <img width='450' height='400' src='https://user-images.githubusercontent.com/60261970/149963577-39df997e-2e2e-4617-987e-985e96834631.png'>
    <img width='450' height='400' src='https://user-images.githubusercontent.com/60261970/149963585-1f0dc8f1-1eac-4433-b526-2393d30bf877.png'>
</p>

#### Frontend

* Preston
    * Display map from MapBox API.
    * Show points on map.
    * Implemented search bar so the user can look for places.
    * When you click on a post location it will show you the exact location on the map.

<p align='center'>
    <img width='400' height='340' src='https://user-images.githubusercontent.com/60261970/149959131-c056b8c8-b75a-4a31-9a05-75318a855bbb.png'>
</p>

    
* Reisli
    * Created a register and login page.
    * Created follower/following sistem.

<p align='center'>
    <img width='320' height='400' src='https://user-images.githubusercontent.com/60261970/149959163-9a8f262f-339b-481a-8059-efe678e3b658.png'>
    <img width='320' height='400' src='https://user-images.githubusercontent.com/60261970/149959176-74477d20-fb1c-4d2f-9992-e83e28ffb180.png'>
</p>

    
* Monia
    * Created homepage, where you can see a map card and on the side is the feed card.
    * Profile page, where you can see details about the user, a map card and at the bottom the user feed, where you can see the images and the name of the location.
    * Nav bar with links, logo and search bar.
    * Search bar where the user can look for other accounts.
    
    <p align='center'>
    <img width='440' height='440' src='https://user-images.githubusercontent.com/60261970/149959373-9001db3e-297d-4b7d-9387-da22a4e7f6e1.png'>
    
    <img width='440' height='440' src='https://user-images.githubusercontent.com/60261970/149959382-a9bc53c0-8e15-452c-9dd1-8d94917a8f1c.png'>
</p>

https://user-images.githubusercontent.com/60261970/149960117-8ae73c73-5a8c-41b3-921f-dbe94d672692.mov


#### Styling

* Preston
    * MapBox.
    
* Reisli
    * Uploading image on profile.
    * Add bio description.
    * Follow button.
    * Comment section.
    
* Monia
    * Profile card, with space for image and description.
    * Profile feed with images and name of the location.
    * Add a new post with a modal from React Bootstrap.
    * Journi logo.
    

## Known Bugs

* On deployment the MapBox API did not show.
* Some styling did not work well when resizing the page.

## Challenges

* For us as a group the main challenge was time, we had many good ideas but we didn't have time to apply all of them.
* At the beginning we had a little trouble with the map API, and at the end with the followers/following, but everything worked just fine.
* The comments section didn't have much styling, but we managed to make it look better.


## Wins

* The biggest win was to make the map API work with the pinpoints.
* The search bar where the user can search for places in the globe as well as other accounts.
* Follower/Following working perfectly well.
* Comments displaying nicely.
* The final product had many functions and worked very well, but we had prepared our backend to accept other forms of requests which we did not end up having enough time to incorporate but this did not stop us from going past our MVP and creating a working, functional social media platform.
* In general we work well as a group, with many ideas and always considering the other opinions.


## Future Enhancements

* I think I can make some styling adjustments, not much to be done, just more styling in the profile page.


## Key Learnings

* Create and populate a Mongo database + working with express and node.
* React Bootstrap, for me, is one of the best frameworks for styling.
* CRUD: Learning how to implement CRUD functionalities.

