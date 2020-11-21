---
layout: post
title:      "Notes from the Blunderground"
date:       2020-11-21 01:10:28 +0000
permalink:  notes_from_the_blunderground
---


Currently I am working on a react front end / rail back end record keeping system with the plan of further developing the app for daily goal tracking and monitoring. The main functionality I’m trying for is to maintain flexibility across users for goal definitions. This way one user could use the same menu for tracking say, daily reading and savings contributions, while another could track daily exercise and caloric intake. To this end I’ve implemented allowing the user to name the goal and then configure the data associated to it with up to three data entry fields. So far progress has been steady, but as with any project there were some unforeseen developments and lessons learned along the way. Here are a few of the issues and notes for my own progress tracking. 

To start with, I should reconfigure the database schema on my API back end. While on paper it seemed logical to separate the Field_name, and Field_type entries to the field table because these are the models that they were describing, in practice it would be more sensible to have these on the Goal table. The reason for this is that while I do want them configurable by field, they should be consistent across all entries of data for that field in the future. Otherwise I will be forced to repeat their assignment every time a user adds a new entry. 

A separate task to focus on during a future code audit: enforce consistency. In variable names, there are a few which jump around (“goal_data” vs “goaldata”) which just introduces bugs when connecting components together, but also choosing a consistent data format for delivery to actions and reducers will prevent many headaches going forward with the project. Also, some time re-assessing the current connection structures of my app now that basic functionality is present would be worthwhile. There are several places where the desire to get the app up and running may have superseded intelligent design. It wasn’t until about halfway through the current implementation that while investigating how to implement some functionality that I was reminded of the Redux connect() function’s parameters each had other parameters of their own such as mapStateToProps ownProps, which was key in several spots. This allowed me to utilize the props of the parent container in selecting the relevant stored state values I needed to pass along to children containers.
