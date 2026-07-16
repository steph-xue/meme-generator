# Meme Generator

An interactive web application that lets users generate a random meme and overlay their own custom top and bottom text on it. Meme images are pulled from the Imgflip API, and as the user types into the text fields, the caption on the meme updates right along with it.

**[View Live Demo](https://meme-generator-sx.netlify.app)**

<br>

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [How It Works](#how-it-works)
- [Getting Started](#getting-started)
- [Future Improvements](#future-improvements)

<br>

## Overview

This project is a small, interactive web application built to practice working with external APIs and managing form state in React. It is built with React, JavaScript, HTML, and CSS, and bundled with Vite. When the page loads, the application fetches a list of meme templates from the Imgflip API and stores them in state, so a new template can be selected instantly at any time without a repeat network request. Text entered into the top and bottom fields updates the meme image live as the user types, since both are controlled inputs tied directly to the component's state.

<br>

## Features

### Random Meme Image and Custom Text
Clicking "Get a new meme image" selects a random template from the list fetched from the Imgflip API and displays it immediately, with a default meme image shown before the button has been clicked. Users can then type their own text into the "Top text" and "Bottom text" input fields, and the meme image updates in real time to display whatever has been entered, letting users caption any meme template with their own text.

<p align="center"><img src="./images/meme-generator.png?raw=true" alt="Meme Generator" width="700"></p>

<br>

## Tech Stack
 
| Layer | Technologies |
|---|---|
| Frontend | React, JavaScript, HTML, CSS |
| APIs | Imgflip API (supplies the list of meme templates to choose from) |
| Build Tool | Vite |

<br>

## How It Works

The interface is built from two components, a header and a meme component, rendered from a single root component. When the meme component first mounts, it fetches the full list of available meme templates from the Imgflip API and stores the result in state, so the list only needs to be requested once per visit. Clicking the button to get a new image picks a random entry from that stored list and updates the displayed image accordingly. The top and bottom text inputs are controlled components, meaning each keystroke updates the component's state and the meme image re-renders immediately to reflect the current text. Vite handles the local development server and production build, compiling the React components into files that can be deployed anywhere.

<br>

## Getting Started

Follow the steps below to set up and run the application on your own machine.

**Prerequisites**

Make sure Node.js and npm are installed before you begin. You can check both by running the commands below, which should each print a version number.
```bash
node --version
npm --version
```

**1. Clone the repository**

This downloads a copy of the project to your computer and moves you into the project folder.
```bash
git clone https://github.com/steph-xue/meme-generator.git
cd meme-generator
```

**2. Install the dependencies**

This installs React and everything else the project needs to run.
```bash
npm install
```

**3. Start the development server**

This runs the application locally with Vite.
```bash
npm run dev
```

Once the server is running, open the local URL shown in the terminal to start using the application.

<br>

## Future Improvements
Several enhancements are planned to extend the functionality of the application:
- The ability to search for a specific meme template by name
- Downloading or sharing the finished meme image directly from the page
- Adjustable text size, color, and position on the meme image
