This React project was created with [Coding Zeal's React Generator](https://github.com/CodingZeal/generator-react-zeal). See the documentation at that site for in depth documentation with regard to creation of React Components and theming, but here's some documentation to get you started.

Environment Variables
==========================

This application uses [dotenv](https://www.npmjs.com/package/dotenv) and reads environmental variables from `.env`, `.env.development`.

If you are using this template as part of a server side application, like Rails or Phoenix, it's important you do **NOT** use the tools these frameworks provide to read environmental variables from these files. (At best, this may start two servers on the same `PORT`!!!!!)

Application server and port
===========================

You can run your React application using `yarn start` (or `npm start`) and by default the React frontend is served from `localhost:3000`. 


Use in the context of a larger framework
=========================

Overriding the PORT the React app is served from
-------------------------

If you are in the context of a larger framework, there are two environmental variables to modify to start on the desired port:

  1. `APP_PORT`: updates the port number displayed to the user as part of the startup routine
  2. `PORT`: updates the actual port the server listens to. (it does not update the startup documentation!)


Overriding default graphql endpoint
-------------------------

By default, React Apollo sends GraphQL requests to `/graphql`, aka *expects this endpoint to be served off the same host and port as the React application itself*.

When using this application in the context of a larger framework, this may not be true.

To set the GraphQL host and port to something different, modify `client/base/apolloClient.js` as appropriate to the version of Apollo Client currently used (1.x uses a `networkInterface` key, 2.x uses `link`, per the [Apollo Client Upgrade Guide](https://github.com/apollographql/apollo-client/blob/master/Upgrade.md))

App Specific Instructions
=========================

(Delete me and add your own!!!)
