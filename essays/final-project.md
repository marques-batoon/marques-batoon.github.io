---
layout: essay
type: essay
title: "Final Project"
# All dates must be YYYY-MM-DD format!
date: 2023-11-01
published: true
labels:
  - Coding Standards
---
<!-- <img width="200px" class="rounded float-start pe-4" src="../img/codingStandardsWhatever.png"> -->

<small>
Authors:
Jianele Liu, Marques Batoon, Reyn Seki, Ryder Shintaku
</small>


## Overview 

Finding a toilet on campus that has a good clean to closeness ratio is always a lone struggle we studdents face each semester. We'd like to make this journey more collaborative by creating a social media web app where students are able to find nearest bathrooms to their location. 

The app will also allow students to rate a bathroom's cleanliness level and include things that others can be weary of. For example, the quality of soap in the bathroom, number of stalls, business at times of days, availability of female products, or if there are areas designated for users to place their belongings while using the premises.


## Mockup page ideas

After registering and signing in, users are able to gain access to the following content:
- **Homepage**: A random bathroom of the day will be featured based on user ratings.
- **Profile**: Each user will have their own profile page which will show their bathroom reviews.
- **Bathroom Directory**: A user can find the highest rating bathrooms near their location by choosing a UH Manoa buildling within the directory. Time pending, we will implement an algorithm to find the nearest bathrooms to a user based on their location. Bathroom directories will be organized by building and floor number. If a building or bathroom is not on the directory, users are able to add their own to the database with a submission form which automatically updates database.
- **Rating Page**: Each bathroom will have a page which shows all ratings and reviews by other students. On this page a user can rate a bathroom and input their own reviews which will automatically be added to the rating page.
- **Search Function**:Bathrooms will be separated by gender and users are able to upload and find gender neutral bathrooms. Users will also be able to find all bathrooms that offer female products.

## Use case ideas
It will be necessary to create a database for users and bathroom facilities. Bathrooms will be organized from building to floor and by gender. 

## Beyond the basics
Ratings submitted by users will automatically update the database and will be published on the site. Time permitting we'd also like to implement an algorithm to find nearest bathrooms to the user based on location and add a schedule feature to each profile
