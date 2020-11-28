# Progressive-Budget

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)



## DESCRIPTION
A budget tracking web application that utilizes PWA (Progressive Web Application) frameworks to successfully store and track financial transactions during offline and online scenarios.



## TABLE OF CONTENTS
* [Installation](#installation)
* [Usage](#usage)
* [Tests](#tests)
* [License](#license)
* [Contributing](#contributing)
* [Retrospective](#retrospective)

## INSTALLATION
- No installation is required, as the user can simply visit the deployed application link: 
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
- To run the application online, please visit the deployed link: []()
- Application functionality is identical whether you are running the server locally or visiting the deployed link:
    - After arriving at the landing page, users will see the following:
        - A ledger of previous transactions (recalled from a Mongo database)
        - A graph documenting the trend/progression of these previous transactions
    - Users can then enter additional transactions – adding or subtracting funds – which are posted to the database
    - In the event that online connectivity is interrupted, users can still proceed to enter transactions
    - During offline status, the transactions are stored with IndexedDB, a "low-level API for client-side storage of significant amounts of structured data"
    - Once online status is returned, any offline transactions are posted to the database and cleared from IndexedDB, and normal online functionality resumes



## LICENSE
License: MIT License<br>
[https://opensource.org/licenses/MIT](https://opensource.org/licenses/MIT)

https://agile-reaches-33212.herokuapp.com/






