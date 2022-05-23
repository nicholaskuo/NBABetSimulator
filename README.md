# Sports Prediction Betting Site for the NBA

Description / Motivation: Everyone loves supporting their favorite team and winning money; therefore, a relatively new sports betting industry has been rapidly growing, offering individuals the ability to place money on a game subject to predetermined payouts. Prior to any sports game, namely the most popular ones, online quant shops, and technology companies provide odds to Las Vegas casinos and betting sites that maximize individuals to spend money betting while ensuring that these brokers make money. Therefore, as large companies like Fanduel and DraftKings (among many others) reach tens of billion-dollar market caps, it begs the question of whether or not betting odds favor the user, casinos, or the odd providers - can the die-hard sports fan or ESPN analyst beat the odds? Naturally, the answer is the casinos or else they would not be in business, but our project uses game outcomes in conjunction with their odds to understand how money moves in the sports betting industry. Our application allows users to sign up, log in, and have their own account where they can save queries and access previously saved queries. For each query, the user can pick the betting strategy, wage strategy, teams to bet on, auxiliary forms (if applicable), and date range. Once the query is run, they can see their total winnings, the breakdown of each game, as well as a graph.


Directories: 
* Frontend: files involving the frontend of our application
* Backend: files involving the backend of the application

# How to Run

On the backend - cd into the backend folder. Run npm install. This will install all the node packages. Then, to serve the backend, type in the command node app.js. 

On the frontend - cd into Frontend/nba-front. Run npm install. This will install all the node packages. Then, to serve the front end, type in npm run start.

Now to see the app in action, navigate to http://localhost:8000

# Technologies

A variety of technologies were utilized to build the application. To house the dataset from Kaggle with the Odds, Player, and Game data a MySQL Database was created on AWS. To store the user signups on the website as well as the queries that they save, a NoSQL database was utilized (DynamoDB), again on AWS. To support backend development, Node.js along with Express was used to make routes and save user state. For frontend development, React.js was utilized to make a professional website that is catered for friendly user behavior. For UI/UX design, we used TailwindCSS and Chart.JS to lay out the content and streamline colors and designs.

# Performance Evaluation

In order to evaluate the performance of our queries, we ran each query five times and took the average. Optimizing our queries led to notably faster runtimes since by pushing up selections and pushing down projections, we were able to decrease the number of rows and columns that we were working with. Furthermore, by adding indices on attributes that we joined on or selected for, we were able to increase the speed of looking up or finding a range within these attributes. We also implemented caching on the query that displays static team names, since this meant that the database would be queried once for all team names when the user first viewed the “New Query”, but never redundantly for the same information. 

