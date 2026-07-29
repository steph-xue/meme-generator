<h1 align="center">
  Meme Generator
</h1>

<h4 align="center">
  An interactive web application for creating custom memes using <br>
  randomly selected images with personalized top and bottom text captions.
</h4>

<p align="center">
  <img src="docs/screenshots/meme-generator.png?raw=true" alt="Meme Generator" width="500">
</p>

<p align="center">
  <a href="https://meme-generator-sx.netlify.app">View Live Demo</a>
</p>

<br>

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [How It Works](#how-it-works)
- [Future Improvements](#future-improvements)
- [Getting Started](#getting-started)

<br>

## Overview

This project allows users to create custom memes by generating randomized image templates and adding personalized top and bottom text captions. It is built with React, JavaScript, HTML, and CSS, uses Vite as the build tool, and is deployed on Netlify for cloud hosting. The interface manages meme data and user input through React state, retrieving a collection of meme templates from the Imgflip API and storing them so new images can be displayed instantly without additional requests. Controlled text inputs update the captions directly on the meme in real time as the user types.

<br>

## Features

### Random Meme Image and Custom Text
Clicking "Get a new meme image" selects a random template from the list fetched from the Imgflip API and displays it immediately, with a default meme image shown before the button has been clicked. Users can then type their own text into the "Top text" and "Bottom text" input fields, and the meme image updates in real time to display whatever has been entered, letting users caption any meme template with their own text.

<p align="center"><img src="docs/screenshots/meme-generator.png?raw=true" alt="Meme Generator" width="700"></p>

<br>

## Tech Stack
 
| Layer | Technologies |
|---|---|
| Frontend | React, JavaScript, HTML, CSS |
| APIs | Imgflip API (supplies a collection of meme images) |
| Build Tool | Vite |
| Deployment | Netlify |

<br>

## How It Works

The interface is built from two components, a header and a meme component, rendered from a single root component. When the meme component first mounts, it fetches the full list of available meme templates from the Imgflip API and stores the result in state, so the list only needs to be requested once per visit. Clicking the button to get a new image picks a random entry from that stored list and updates the displayed image accordingly. The top and bottom text inputs are controlled components, meaning each keystroke updates the component's state and the meme image re-renders immediately to reflect the current text. Vite provides the local development server and bundles the application’s files for deployment via Netlify.

<br>

## Future Improvements
Several enhancements are planned to extend the functionality of the application:
- The ability to search for a specific meme template by name
- Downloading or sharing the finished meme image directly from the page
- Adjustable text size, color, and position on the meme image

<br>

## Getting Started

Follow the steps below to set up and run the application on your own machine.

<br>

**Prerequisites**

Make sure Node.js and npm are installed before you begin. You can check both by running the commands below, which should each print a version number.
```bash
node --version
npm --version
```

<br>

**1. Clone the Repository**

This downloads a copy of the project to your computer and moves you into the project folder.
```bash
git clone https://github.com/steph-xue/meme-generator.git
cd meme-generator
```

**2. Install the Dependencies**

This installs all dependencies the project needs to run.
```bash
npm install
```

**3. Start the Development Server**

This runs the application locally with Vite.
```bash
npm run dev
```

Once the server is running, open the local URL shown in the terminal to start using the application.
