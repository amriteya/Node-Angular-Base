# Node-Angular-Base

Steps to setup the project.

   - Clone the project.
   - Run `npm install --save`
   - Run `npm start`
   
The server will be running on localhost at port 3000.


This is a node application built using express framework. The `npm start` looks for scripts in [package.json](package.json#L6).

The first command sets up the node server and makes it available on localhost on port 3000.

The basic resource routing is defined in [app.js](app.js#L25-L26). <br />
For eg. <br />
`localhost:3000/` is defined at [app.js](app.js#L25) which points to [imported file](app.js#L8) under [routes](routes/index.js) directory. <br />
`localhost:3000/users` is defined at [app.js](app.js#L26) which points to [imported file](app.js#L9) under [routes](routes/users.js) directory.


By default express app uses jade templating and the templates could be found in [views](views/) directory and the configuration for using same can be found in [app.js](app.js#14-15).

In this particular application we [change the rendering strategy](routes/index.js#L6-L9) of `/` route. Instead of rendering the jade template, we render an HTML file which is using Angular.js


In order to provide dynamic data to angular controller, we create another route `/data` in [index.js](routes/index.js#L11-L22) which return json data which is then rendered by the angular controller.
