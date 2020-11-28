# Progressive-Budget

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)



## DESCRIPTION
A budget tracking web application that utilizes PWA (Progressive Web Application) frameworks to successfully store and track financial transactions during offline and online scenarios.

## SCREENSHOTS
### Screenshot of the landing page, showing the ledger of previous transactions
![Screenshot of Landing Page](./public/img/1-LandingPage.png)
### Screenshot of the graph, documenting the trend/progression of these previous transactions
![Screenshot of Graph](./public/img/2-Graph.png)

## TABLE OF CONTENTS
* [Installation](#installation)
* [Usage](#usage)
* [Tests](#tests)
* [License](#license)
* [Contributing](#contributing)
* [Retrospective](#retrospective)

## INSTALLATION
- No installation is required, as the user can simply visit the deployed application link: [https://pwa-budget-2020.herokuapp.com/](https://pwa-budget-2020.herokuapp.com/)
- However, if the user wishes to investigate the code locally, the following steps should be performed:
    - Clone the repo for use on your local machine
    - Use the command line to locate the cloned repo and make it your current directory
    - Type `npm install` in the command line
    - This will install the necessary node module packages and dependencies
    - Under the assumption that the user has MongoDB previously installed and/or running, no further installation is required

## USAGE
- To run the application locally...
    - Use the command line to locate the cloned repo and make it your current directory
    - Simply type `node server.js` in the command line
    - Executed correctly, the command line should respond with `Server listening on http://localhost:####`
    - Open your preferred browswer and visit `http://localhost:####/`
    - In both instances above, replace `####` with the corresponding PORT number as noted in the server.js file
    - To end the server instance, simply type "ctrl" + "c"
- To run the application online, please visit the deployed link: [https://pwa-budget-2020.herokuapp.com/](https://pwa-budget-2020.herokuapp.com/)
- Application functionality is identical whether you are running the server locally or visiting the deployed link:
    - After arriving at the landing page, users will see the following:
        - A ledger of previous transactions (recalled from a Mongo database)
        - A graph documenting the trend/progression of these previous transactions
    - Users can then enter additional transactions – adding or subtracting funds – which are posted to the database
    - In the event that online connectivity is interrupted, users can still proceed to enter transactions
    - During offline status, the transactions are stored with IndexedDB, a "low-level API for client-side storage of significant amounts of structured data"
    - Once online status is returned, any offline transactions are posted to the database and cleared from IndexedDB, and normal online functionality resumes

## TESTS
To test offline functionality – and ensure that data collected, stored in IndexedDB, and then subsequently posted when online functionality returns – please take the following steps:
- Take the application offline (e.g. utilize Service Workers)
![Taking the application offline](./public/img/3-ServiceOffline.png)
- Post an offline transaction (e.g. add or subtract funds)
![Making an offline transaction](./public/img/4-OfflineTransaction.png)
![Posting an offline transaction](./public/img/5-OfflinePosted.png)
- Confirm that the data has been stored in IndexedDB
![Storing the data in IndexedDB](./public/img/6-IndexedDB.png)
- Take the application back online and post an online transaction (e.g. add or subtract funds)
![Taking the application online and posting a transaction](./public/img/7-OnlineTransaction.png)
- Confirm that the offline AND online transactions have been posted in your MongoDB
![Confirmation of MongoDB data](./public/img/8-Database.png)

## LICENSE
License: MIT License<br>
[https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT)

## CONTRIBUTING
[https://github.com/JPBrickhouse](https://github.com/JPBrickhouse)

## RETROSPECTIVE
This was an informative homework assignment, that afforded many opportunites for learning and growth. While the majority of the initial code was provided – allowing for consistent online functionality – I was required to create and write code for the following files to implement the PWA offline functionality:
- `public/db.js`
- `public/manifest.webmanifest`
- `public/service-worker.js`

Beyond that, the following files also required additional modifications:
- `public/index.html`
- `public/index.js`
- `server.js`

With everything in place, I "connected the dots," ensuring that the budget tracker worked accurately during offline and online scenarios.
