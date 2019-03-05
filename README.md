# Let's practice modules
## Setup
* npm install
* npm start
- If you are on a windows machine, remove the single quotes from package.json in "start": "nodemon --exec 'babel-node src/index'"
* What shows up in the terminal?

## Do
* You should see the text `Cannot find module './modules/multiply'`
Why? What's this telling us? Essentially, we haven't configured everything properly.
Let's find the source of the problem.

* Look in your terminal, a few lines below the `Error:`
What we are looking at is called a Stack Trace and what we are looking for the source of the error. 
You'll notice that the first couple lines below the error reference `internal/modules/cjs/loader.js:581:15`. 
This shows us the file and line number where the error occured. But.. that doesn't look like our file. It doesn't
appear anywhere in our project. That's ok, it's a third party file. So let's keep looking for one of our files. 
`/advanced-module-practice/src/index.js:3:1`. If you go to that file and line number (3) you will see that it 
tries to import a file/module that doesn't exist! That's the problem!

* Add file and implement code for multiply module

* What's in the terminal now?

* Implement code for subtractNumbers module
Create a file called subtractNumbers in the module folder. You should know where to look 
for this already but if you didn't.. it's in the first line of the `Error` message. 
Figure out what to call the function

* What's in the terminal now?
Are you seeing a pattern?? Hopefully.. but it's a different error message now. You're on your own, you know 
how to find these errors now. 

* The divide module is next.. let's tackle it!

* Let's finish the rest of the modules
  * Implement code for addOne in the addNumbers module
  * Import and use addOne in index.js
  * Implement the rest of the code for subtractNumbers module

* Run yarn start

* Make sure there are no errors

