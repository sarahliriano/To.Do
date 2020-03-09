## List of things I rather do app.

**Part One**
Final Project Proposal: A personal diary app where you input daily observations and activities with the date and some hashtags. Kind of like a daily blog of your life and it's displayed in chronological order.

**Part Two**
For this week we were supposed to do something similar to what we did in class but add a client side to it. Some of the things we did in class weren't clear to me but at this point I'm starting to figure out that clarity will come with practice and the more I do it the better I'll understand it. I've been feeling like now I have a better grasp of the things we learned at the beginning of the semester. It's kind of frustrating because I feel like I'm always behind everyone else in terms of learning but I'm just going to have to deal with it.

So for my homework I decided to do a simple To Do List app like what we did in class but with a client side view. I chose this because it seemed simple enough in order for me to practice what we learned and try to better grasp the concepts. I modified the content. My inspiration came from my birthday, which I spent doing this homework.

I tried following the workbook again but the non-linear way of explaining is really confusing for me. There's an assumption that we already know all the syntax and functions to use and we need to branch for each solution to the problem when we don't. So I decided to do the same thing as before and look for a straightforward tutorial and try to understand the concepts as best I could. I ended up learning some interesting things that were very new to me and a different process for this which seemed clearer.

The tutorial I followed is in this article which has two chapters by Diogo Pinheiro:
- Chapter 1: https://medium.com/@diogo.fg.pinheiro/simple-to-do-list-app-with-node-js-and-mongodb-chapter-1-c645c7a27583
- Chapter 2: https://medium.com/@diogo.fg.pinheiro/simple-to-do-list-app-with-node-js-and-mongodb-chapter-2-3780a1c5b039

The tutorial starts by explaining basic concepts, some of which I already knew but it was a nice refresher and I learned what REST is.

Then we created our directory using the terminal, something I'm pretty confident in doing at this point (mkdir).

Something new I learned is that VS Code also has a terminal in which you can execute commands. This particular tutorial has us execute "npm init" within that terminal. I was a little unsure if this would cause an issue later on but I wanted to follow the tutorial to the letter and just focus on cementing the concepts for future use.

We proceeded by installing Express, mongoose, ejs and dotenv and nodemon.

With this I learned that:
Dotenv is a zero-dependency module that loads environment variables from a .env file into process.env. In this file we ended up storing our MongoDB url to connect to our cluster.

EJS (Embedded Javascript Templating) is a templating engine used by Node.js that helps create an HTML template with minimal code. Also, it can inject data into HTML template at the client side and produce the final HTML. EJS is a simple templating language which is used to generate HTML markup with plain JavaScript. It also helps to embed JavaScript to HTML pages.

The next part of the process was similar to what we've done before initializing the server, using npm start and asigning a port number (listening at local host 3000) and logging a message if it's running properly.

**GET METHOD**
After that what follows is testing the "GET" method where every time there's a request we send a response of a "Hello World" message.

Setting the "view engine" was kind of different but from what I understand it is basically telling it to "display" the .ejs templates like it would display a regular html file?

What followed was filling up the .ejs with html markup which was very recognizable for me and creating a .css file for my styles. To access the css (middleware) file we used the app.use function and give it a path to our file.

**POST METHOD**

the first line of code here means that I'm accessing the express library and extracting the data so I can store it and console log it. We easily tested this and it worked when I saw the results in my console.

**CHAPTER TWO**

The first part of this chapter deals with Mongo DB and creating a new cluster. I didn't know I could only have the one cluster in the free option so I had to delete the previous one and work with this new one. It made em a little nervous to delete the old one though.

After all that was set up we connected by first requiring the dotenv library and adding our Mongo DB url to the .env file.

We called the mongoose library and connected to the db.

The next step was very blurry for me in class so I'm glad it was repeated here and then explained by a classmate. We created a schema or data model next so that the db knows how I want to store my information and so I can see it in that format. I exported the model so I could pass it to a variable and use it in my server.js file.

The next step was to modify the POST method we had created before in order to start adding the tasks to the db.

We then modified our GET method to be able to see our data on the client side constantly. Essentially we told it to search the TodoTask file and find the data  for tasks then render the todo.ejs file with the tasks that have been created in our database (I think?).

What followed was something else that was new to me where we're adding JS code to the .ejs file in order to create new instances of things. I didn't know you could do that.

**UPDATE**
This part of the tutorial got a little confusing but I think I understood most of it. Essentially we're giving it a route to the thing that we want to edit, then we're asking that it pre-fills the form with the information from that task then find the data for the tasks and render the file for the edits which has the confirm and cancel buttons and the new input box.

Once the changes are done we post to that same id and replacing the content and asking to return an error if there is one.

**DELETE**




