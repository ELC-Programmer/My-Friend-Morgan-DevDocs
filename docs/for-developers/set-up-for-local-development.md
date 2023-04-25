# My Friend Morgan
# **Set up for local development**

## Required
- Node.js v14 or later
- npm (should be included with Node)

## Set up
1. Clone the repository from GitHub
2. Run ```npm install``` in the frontend directory
3. Run ```npm install``` in the server directory
4. Go to frontend/src/util/serverInfo.js and change the ```serverURL_dev``` variable if necessary
5. To start the server: Switch to the server directory and run ```npm start``` or ```npm run dev``` 
   1. ```npm start``` starts the server normally
   2. ```npm run dev``` starts the server and restarts it any time changes are made to the server files
6. To start the frontend: Switch to the frontend directory and run ```npm start```
   1. The default url for the app is localhost:3000