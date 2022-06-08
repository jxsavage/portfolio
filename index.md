---
title: Hi, My Name is Jake Savage...
layout: default
show_downloads: false
---

# Welcome to My Portfolio

>Here's a list of my most recent projects hosted on Github!

## Remote Controlled Lighting:
***

![Venue Lighting](https://user-images.githubusercontent.com/2956515/172713433-ae3a46c5-d56d-4d29-8e2c-176798a51b02.png)

***
  This project was a way for me to experiement with various web technologies including React, Redux, WebSockets, Redis and working with microcontrollers. Building this project I became very comfortable with asynchronous programming and promises in TypeScript and JavaScript as every step of communication required asynchronous calls.

  Through a web interface you can interact with microcontrollers that control the LED light bars directly. You can do things like:
  - Change a segments lighting effect
  - Split an existing segment
  - Merge existing segments back together
  - Adjust segment boundaries changing their size as well as adjusting the adjacent segments size appropriately

### Project Components:
  - **Web Interface**: The web interface is primarily built using React with Redux to display the data pulled from the server. It uses the Socket.io WebSocket client to communicate with the server. ([Repo Link](https://github.com/jxsavage/remote-lights-web))
  - **Microcontroller**: The microcontroller and associated code controls the actual LEDs, stores its default settings and waits for an incoming bluetooth connection from a client.
  ([Repo Link](https://github.com/jxsavage/remote-lights-micro-socket-client))
  - **Lighting Client**: The lighting client scans for microcontrollers and connects to them via bluetooth, once it connects to one it sends that information on to the server. ([Repo Link](https://github.com/jxsavage/remote-lights-micro-socket-client))
  - **Server**: The lighting server stores information from all the lighting clients and stores it in a Redis database. It also provides that information to the React web interface. ([Repo Link](https://github.com/jxsavage/remote-lights-micro-socket-client))
  - **Shared Library**: There were several TypeScript types and functions that needed to be shared amongst all components. This repository is for any code that needs to be shared by several components. ([Repo Link](https://github.com/jxsavage/remote-lights-shared))

### Testing:
As the code base grew there were several areas I noticed where bugs tended to pop up that were difficult to notice and/or determine the source. It was difficult to tell if the data I was getting from Redis was exactly the same as what I put in without going through and inspecting it myself. I had the same problem with ensuring that data and commands going into the microcontroller were having the proper result. Because of these problems I took the following steps using the Jest test framework:

- Created test data that had both the input as well as the expected output.
- Unit tested the functions that modified the data in the Shared Library of the project.
- After the unit tests were working I moved onto testing the Redis database functions.
- I also tested that the commands I sent to ensure the micrcontrollers were changing the state of the microcontroller the way that I expected.

### Features and Improvments to Add...

- **Grouping Segments:** I'd like to be able to group segments together so I can control the effects for multiple segments at the same time.
- **Save Multiple Presets:** The ability to save multiple setting configuations and choose between them with a user interface.
- **Improve Handling of Bluetooth Connections:** I've tested up to 3 Bluetooth devices and 7 is the hard limit, but in order to expand passed those limitations I would need to make a way for a client to claim certain bluetooth devices so others don't attempt to connect which disconnects the original device. An alternate solution could be to move to using WiFi instead eliminating the need to manage that.
- **Change the LED Library on the microcontroller:** The current library I use requires the pins to control the LEDs as well as the LED stip length to be known at compile time. This means I cannot change them at run time. There is another library I found where this would be possible.

### Project Photos
![Venue Lighting](https://user-images.githubusercontent.com/2956515/172713484-da150b46-246e-4ef6-9dee-3ea5bacfc143.png)
  
### Repositories:
- [Remote Lights Server](https://github.com/jxsavage/remote-lights-pi)
- [WebSocket Lighting Client](https://github.com/jxsavage/remote-lights-micro-socket-client)
- [React based Web Interface](https://github.com/jxsavage/remote-lights-web)
- [Shared Types and Functions](https://github.com/jxsavage/remote-lights-shared)
- [Microcontroller](https://github.com/jxsavage/remote-lights-micro)

## SELENIUM AUTOMATION TESTING:
***

I've recently started playing around with Selenium and really like it. I found a site that permits you to run automation tools against a test site they built so I began writing tests for that site. I noticed myself repeating a lot of the same functionality test to test so I began breaking certain things I repeated into their own fuctions so I could re-use them efficiently.
### Repository: [Link](https://github.com/jxsavage/selenium-demo)

