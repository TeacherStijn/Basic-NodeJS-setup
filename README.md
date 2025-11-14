# Basic NodeJS server with small front-end

## Starting off with a basic NodeJS project;
Create a projectfolder and navigate in it
> mkdir yourDirectory
>
> cd yourDirectory
>
> npm init -y

Create basic serverfile
> 

Extend basic serverfile with content by opening in notepad/editor and fill with:

> import express from "express";
>
> const app = express();

> app.get("/", (req, res) => {
>
>   res.send("Hello world");
>
> });
>
> app.listen(3000);

Install the basic dependencies
> npm install express openai --save

Testrun
> node index.js

> check browser @ http://localhost:3000

> close the instance by pressing <ctrl><c> and confirm with <y>

## Add basic front-end
create folder 'public' and navigate in it
> mkdir public
>
> cd public

Create basic HTML file:
> type nul > index.html

Open index.html in an editor and add the following lines of HTML:
> <!DOCTYPE html>
> <html>
> <body>
> Hello there!
> </body>
> </html>

## Statically provide the front-end to the NodeJS back-end
Add the following line on line 3 to include a local directory:
> app.use(express.static("public"));

Change the res.send() line with the following so the index.html file is sent back:
> res.send("index.html");

Start the server again 
> node index.js

Test the result in the browser by refreshing the page
> F5
