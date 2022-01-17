# journi

## Goal

Design a social media where people can share their trips with an online community which incorporates maps and ratings. 

## Timeframe

Timeframe: 1 week.

## Inspiration

We were inspired to create something which circulated around social media with a strong influence centred around the feed and using a map API.

## Project Overview

<!-- video -->

## Deployment 

The website can be viewed here, however, we have found out that the api only works locally:

https://journi-media.herokuapp.com/login

## Getting Started

As a team we did the backend together, following guidance from previous homework from the Bootcamp.

On the backend we created our own database which gave ownership to account posts and created a following system.

First of all we created a register and login page, and then we focused on the homepage, where you can see a map and on the side is the feed.

The feed works well, and is influenced by your friends posts and is ordered by the date it was posted. 

We used mapBox to create our own map which had points and locations attached to it based on the locations put within the posts, this created almost a pinning map system which was the main focus when creating this platform.

So when you click on a post it will show you the exact location on the map.

I was focussed on integrating the frontend with the backend, home and profile page, search bar, as well as other small functionalities and styling.

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
    <img width='300' height='450' src='https://user-images.githubusercontent.com/60261970/149829138-bf29fa87-e25e-4c9b-b34b-354dbf4c3d1b.png'>
  <img width='300' height='450' src='https://user-images.githubusercontent.com/60261970/149829143-cd703d50-b7bc-4d40-8613-3496e2979caa.png'>
  <img width='300' height='450' src='https://user-images.githubusercontent.com/60261970/149829149-6af4055f-bec2-4cef-be7d-1abb7dbb25e6.png'>
</p>

And we had a wireframe to show how we wanted the home page to look like:
<p align='center'>
    <img width='500' height='360' src='https://user-images.githubusercontent.com/60261970/149829460-21284d69-dba2-44da-83ff-a2687d4fbfb2.png'>
</p>

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

## Future Enhancements

* I think I can make some styling adjustments, not much to be done, just more styling in the profile page.


## Key Learnings

* Create and populate a mongo database + working with express and node.
* React Bootstrap, for me, is one of the best frameworks for styling.
* CRUD: Learning how to implement CRUD functionalities.

## Teamwork

The final product had many functions and worked very well, but we had prepared our backend to accept other forms of requests which we did not end up having enough time to incorporate but this did not stop us from going past our MVP and creating a working, functional social media platform.

In general we work well as a group, with many ideas and always considering the other opinions.


## How to Use it

The user is able to register and login, and when they are in the profile page, they can add their own photo, bio description and see their followers. 

They can see a map with their own posts and add posts as well.

With the search bar, the user can look for location or other users.

When the user is in someone else's profile they can see their posts and also follow this account.

In the home page the user will see the map and the feed with the accounts they follow, and they can leave comments in other accounts' posts.
