---
title: Hi, My Name is Jake Savage
layout: default
show_downloads: false
---

# Welcome to My Portfolio...

  Here's a list of my most recent projects hosted on Github!

## Remote Controlled Lighting:
***

  This project was a way for me to experiement with various web technologies including React, Redux, WebSockets, Redis and working with microcontrollers. Building this project I became very comfortable with asynchronous programming and promises in TypeScript and JavaScript as every step of communication required asynchronous calls.

  Through a web interface you can interact with microcontrollers that control the LED light bars directly. You can do things like:
  - Change a segments lighting effect
  - Split an existing segment
  - Merge existing segments back together
  - Adjust segment boundaries changing their size

### Project Components:
  - **Web Interface**: The web interface is primarily built using React with Redux to display the data pulled from the server. It uses the Socket.io WebSocket client to communicate with the server. ([Repo Link](https://github.com/jxsavage/remote-lights-web))
  - **Microcontroller**: The microcontroller and associated code controls the actual LEDs, stores its default settings and waits for an incoming bluetooth connection from a client.
  ([Repo Link](https://github.com/jxsavage/remote-lights-micro-socket-client))
  - **Lighting Client**: The lighting client scans for microcontrollers and connects to them via bluetooth, once it connects to one it sends that information on to the server. ([Repo Link](https://github.com/jxsavage/remote-lights-micro-socket-client))
  - **Server**: The lighting server stores information from all the lighting clients and stores it in a Redis database. It also provides that information to the React web interface. ([Repo Link](https://github.com/jxsavage/remote-lights-micro-socket-client))
  - **Shared Library**: There were several TypeScript types and functions that needed to be shared amongst all components. This repository is for any code that needs to be shared by several components. ([Repo Link](https://github.com/jxsavage/remote-lights-shared))
  
### Repositories:
- [Remote Lights Server](https://github.com/jxsavage/remote-lights-pi)
- [WebSocket Client](https://github.com/jxsavage/remote-lights-micro-socket-client)
- [React based Web Interface](https://github.com/jxsavage/remote-lights-web)
- [Shared Types and Functions](https://github.com/jxsavage/remote-lights-shared)
- [Microcontroller](https://github.com/jxsavage/remote-lights-micro)

## SELENIUM AUTOMATION TESTING:
***
### Repository:

