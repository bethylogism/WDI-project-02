# WDI-project-02
React 1-day hackathon project

# General Assembly Project 1 : Simple front-end game

### Timeframe
2 days

## Technologies used

* JavaScript (ES6)
* HTML5
* CSS3
* React


## Installation

1. Clone or download the repo
2. Run yarn in Terminal
3. Run webpack dev server with yarn run serve

## Eventify: Events, now.

We were tasked with creating a React app in a day, with an evening for planning. We decided to create an events app which, unlike most messy apps in the genre, simply told you what's going on right now, within a 5 mile radius. 

This was a highly achievable, fun, and useable technology to create in such a short timeframe. 



## Process
After the initial ideation moved onto breaking down the MVP into smaller steps. One of the first steps was checking out public APIs and ensuring that we could find solid APIs to combine. Fortunately we came acrosss Skiddle, a highly usable events API, and Mapbox-GL. 

We tested the Skiddle data in Insomnia to check that it was complete and usable, and could then plan how to get the appropriate props to pass to the map component. 


Our initial design board:
![image](https://user-images.githubusercontent.com/44749113/55501952-75c2a980-5643-11e9-8412-d1c56f3e64dc.png)

We used Trello heavily for planning and broke down the tasks: https://trello.com/b/1aAeJeFY/eventify-api-mashup

We aimed to get the map on the page, followed by user location. Once this was set up we made sure that we could send a user's coordinates to the Skiddle API. 

The next step was properly linking up the event data with the map. We made an Axios request using the user's location parameters in the request url. We set state with the response and handed this down to the map component (the main component). We then mapped over the latitude and logitude data from the events in that region and used these to create mapbox popup markers. We also used the imagery and short descriptions from Skiddle to make the popups more useable. We added the user's location to create a Google Maps route link inside each popup that. 

Finally we styled the map, using SCSS variable to tag the event map markers on the page and a key to make it clear what each event is. We also created a loading screen as there is a lengthy wait for the geo-location data to load, which is required for the axios request. We also had time to make it mobile-friendly!

![image](https://user-images.githubusercontent.com/44749113/55503348-5f6a1d00-5646-11e9-8851-a2f3b01bcc3b.png)




### Challenges
The biggest difficulty was finding a good API. Even when we found Skiddle, which yielded high-quality results, we couldn't create a deeply personal or local experience because the radius had to be at least 5 miles for there to be more than a small handful of events displaying on the map. 

### Wins
One of the biggest wins was working effectively in a pair, and picking up features to smash out independently as well as tricky areas for pair-coding. 


## Future features
The app would really benefit from the ability to filter events by type. 


