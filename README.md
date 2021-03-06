# RentRabbit - React App

### Description

RentRabbit is a website where people can rent and/or buy tools from other users. The webapp was built using `React-js` front-end, `express` back-end, and a `mysql` database. This project contributed a lot in the journey to learn about each of the individual stacks and how they are connected in the web.

### Requirements
- `npm` and `node` installed in your system
- `mysql workbench` or a cloud instance of `mysql`

### Setup
- Clone repo using `git clone https://github.com/Aadhieaswar/RentRabbit.git`
- Import the schema and data from `data.sql` in the home directory of the repo into your `mysql workbench` or cloud instance
- `cd` into the cloned repo and run `npm install` in both `Server` and `WebApp` directories of the cloned repo
- After npm completes installing packages in both the directories, open two terminals
  - In one of the terminals `cd` into the `WebApp` directory and run `npm start`
  - In the other terminal `cd` into the `Server` directory and run the following command:
    ``` bash
      # environment variable values for the mysql db connection configuration
      # provide appropriate values for each of the environment variables to connect to your mysql database
      $ HOST=<db-host> USER=<db-user> PWD=<db-password>  DB=<db-name> node server.js
      ```
  - You can choose to directly add the configurations to the file in `Server/db/connection.js` instead of setting the environment variables and run `npm start` in the `Server` directory to start the server
- The react app should then open in your default browser

### Files and Directories
- The crucial files in the repo home directory are:
  - `data.sql`: dump file with all the database schema and data used for the `mysql` database
  - `Server`: folder that consists of all the files required to run the `express` server
    - `db`: consists of files that are required to create the database connection and the async queries to get data
    - `server.js`: file that contains all the code to run the `express` server
    - `package.json`: consists of all the dependencies and the run script for the app
  - `WebApp`: folder that consists of all the files required to run the `react` app
    - `src`: consists of all the files for the react app
      - `index.js`: the entry point of the react app
      - `index.css`: consists of styles for the react component in `index.js` file
      - `App.js`: the main file to view the app
      - `App.css`: consists of styles for the react component in `App.js` file
      - `Axios`: consists of the file with the axios requests
      - `Header`, `Login`, `Profile`, `Tools`, `Transactions`, `User`, `insertTools`, and `popRenters` each consist the files used to create the respective react components needed for the app
      - `package.json`: consists of all the dependencies and the run script for the app

### Credits
- Implemented by __Aadhieaswar Senthil Kumar__
    - Contact me at: <aadhieaswar@gmail.com>
