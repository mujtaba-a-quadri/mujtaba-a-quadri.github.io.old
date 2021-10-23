---
layout: project
type: project
image: images/ProxamieLogo.png
title: Proxamie
permalink: projects/proxamie
# All dates must be YYYY-MM-DD format!
date: 2021-10-22
labels:
  - Hackathon
  - MongoDB
  - Meteor
  - Web App
  - COVID-19
summary: Team DAAJ (Dylan, Alyssia, Abdullah, Jolie)'s submission for the 2021 Meteor Hackathon!
---

<img class="ui large right floated rounded image" src="../images/AddAvailabilitiesPage.png">

In my (and all my team mates') first Hackathon, we developed an app to help groups plan/schedule hangouts. Users can create and log into accounts, dropping them into their personal profile page. From here they can indicate their availabilities using a [when2meet](https://www.when2meet.com/) style interface. 

They can also create and join groups from this page, leading them to the group page. The group page features a unique code to share with others, allowing them to join the group from their profile page. Finally, from the groups page, any member can click on a calendar which visualizes the group's overlapping availabilities. Clicking on a date will pop up a form to create a hangout, which will be visible to all group members.

For this project, I helped plan the database structure and created most of the collections (tables) in it. This was important because there were many relations we needed to display all the info we wanted. For example, users need to see all the groups they are a part of, but group pages also need to display all of the users in the group. We had a couple [many-to-many](https://en.wikipedia.org/wiki/Many-to-many_(data_model)) relationships like this and as such had to plan out join tables. 

<img class="ui large right floated rounded image" src="../images/CreateHangoutOptions.png">

My other primary contribution was the create hangout form and hangouts table. Clicking on a date on the group page displays a form to create a new hangout. This form prompts you to choose a time (selected from a dropdown which tells you who will be available at each time) and enter a name and description for the hangout. This info is then put into the hangouts table in the group, for all in the group to see. 

<img class="ui large right floated rounded image" src="../images/CreateHangoutWarning.png">

I also had the form display a warning when too many (>10) would be available for a hangout. Unfortunately this feature broke the morning that the hackathon ended as we had the site refresh on submit of the forms (making it impossible to create a hangout with >10 people). Maybe that's better anyways, we could've gotten in trouble; promoting hangouts of more than 10 people.


All in all, I learned a lot from my first hackathon! I saw just how much can be done in just under a week. I think my group handled the project very well, we didn't step on each other's work too much and made sure to communicate. We met almost every day (multiple times in the later days) and chatted often. I think we were all quite drained from the whole thing though, and I will likely think twice before participating in any short hackathons in the future. I think it was a good experience for sure, just a very exhausting one.

[See the GitHub repo](https://github.com/ICS491-Fall2021/meteor-hackathon) 
||
[See the deployed application](https://proxamie.meteorapp.com/)

