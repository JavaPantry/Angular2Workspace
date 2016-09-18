- Read Appendix B install typescript '__npm install -g typescript__'
	-- typescript@1.8.10
- confirm version and availability
	C:\Users\ptitchkin>tsc --version
	Version 1.8.10
- transpile ts file with source map
	tsc --sourcemap main.ts

- Step 1: from book p#335 
>In the command line change to the server directory and run __npm install__ to get all
required dependencies for the server’s portion of the application.
To use the local compiler run the command __npm run tsc__, which will transpile the
server’s code and will create auction.js and model.js (and their source maps) in the
directory build as configured in tsconfig.json. This is the code for the Auction’s server.
Start the server by running the command __npm run startServer__  (_missing 'run' in original_). It’ll print the message
"Listening on 127.0.0.1:8000" on the console.

    C:\webStormWS\Angular2Workspace\auction\server>npm run tsc
    > ng2-webpack-starter@ tsc C:\webStormWS\Angular2Workspace\auction\server
    > tsc
    C:\webStormWS\Angular2Workspace\auction\server>

- Step 2: from book p#336
>Before starting the client portion of the auction you need to open a separate command
 window, change to the client directory, and run the command __npm install__.
 Then start the Auction app in the development mode by running __npm run startWebpackDevServer__. The webpack-dev-server will bundle your Angular app
 and will start listening for browser’s requests on port 8080. Enter http://localhost:8080 in your browser and you’ll see the familiar UI of the Auction app.
 
- if terminate node server started in Step 1 and refresh auction page products will appear

- Step 3: from book p#337 
>Now stop the webpack-dev-server by pressing Ctrl-C in the command window where
 you started the _client_ from. , Start the production build by running the command __npm run deploy__. This command will prepare the optimized build and will copy its files into the
 directory ../server/build/public, which is where all the static content of our Node server belongs.
 There is no need to restart the Node server since we only deployed the static code
 there. But now to see the production version of the auction you need to use the port 8000, where our Node server runs.
 Open your browser at the URL http://localhost:8000. You’ll see the Auction
 application served by the Node server. Open the Chrome Developer Tools panel in the
 Network tab and refresh the application. You’ll see that the size of the optimized application is drastically smaller.
 
- error because I shouldn't __npm run deploy__ in server folder, but in client

- restart __npm run startServer__ in server folder
- restart __npm run deploy__ in client folder
- error in karma chrome not installed on my inspiron
- TMP Fix take out `"test": "karma start karma.conf.js",` from Angular2Workspace\auction\client\package.json
- mark it with prefix 'deleteTask_'> "deleteTask_test": "karma start karma.conf.js",