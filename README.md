# Text Editor Web Application

## Overview

This repository contains the source code for a text editor web application built with modern web technologies. The application has a robust client-server architecture, utilizes webpack for bundling JavaScript files, employs IndexedDB for local storage, and implements service workers for offline capabilities. Additionally, the project includes deployment scripts for Heroku.

## Features

- **Client-Server Architecture:** The application follows a structured folder setup for the client and server components.

- **npm Scripts:**
  - Running `npm run start` from the root directory starts the backend and serves the client.
  - Executing webpack plugins generates HTML files, a service worker, and a manifest file.

- **Webpack Integration:** JavaScript files are bundled using webpack, allowing for efficient module management.

- **Next-gen JavaScript Support:** The text editor seamlessly functions in the browser even when utilizing next-gen JavaScript features.

- **IndexedDB Integration:**
  - Upon opening the text editor, IndexedDB immediately creates a database storage.
  - Content entered is saved to IndexedDB when clicking off the DOM window, ensuring persistent storage.

- **Content Retrieval:** Closing and reopening the text editor retrieves content from IndexedDB, providing a seamless user experience.

- **Desktop Icon Download:**
  - Clicking the "Install" button allows users to download the web application as an icon on their desktop.

- **Service Worker Registration:** Loading the web application registers a service worker using Workbox.

- **Offline Support:**
  - Service workers pre-cache static assets upon loading, ensuring a smooth offline experience.
  - Subsequent pages and static assets are also pre-cached, enhancing performance.

- **Heroku Deployment:**
  - Proper build scripts are included for deploying the webpack application to Heroku.

## Getting Started

1. Clone the repository:

   `git clone https://github.com/your-username/text-editor-web-app.git`
   `cd text-editor-web-app`

2. Install dependencies:

   `npm install`

3. Start the application:

   `npm run start`

4. Access the text editor at [http://localhost:3000](http://localhost:3000).

## Deployment to Heroku

To deploy the application to Heroku, follow these steps:

1. Create a Heroku account if you don't have one.

2. Install the Heroku CLI.

3. Login to Heroku in your terminal:

   `heroku login`

4. Create a new Heroku app:

   `heroku create your-app-name`

5. Deploy the application:

   `git push heroku master`

6. Open your deployed application:

   `heroku open`

## License

This project is licensed under the [MIT License](LICENSE)