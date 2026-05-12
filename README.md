# Events and Debugging Assessment

Time to assess how well you have learned to use the debugging tools in Chrome Dev Tools, and writing click event listeners. This application is to show kids with illnesses and the memories the would like to make. Celebrities sign up to help kids make memories.

> 🧨 Make sure you answer the vocabulary and understanding questions at the end of this document before notifying your coaches that you are done with the project

## Event Listeners to Create

1. When the kid name is clicked, it should display their wish.
1. When the celebrity name is clicked, it should display their sport.
1. The pairings list should should contain the pairing in the following format.
   ```html
   {child name} will be making memories with {celebrity name}, a {celebrity
   sport} star, by {child wish}
   ```

Below is an animation showing how the application should look when complete and how the event listeners should work.

<img src="./images/debugging-events-assessment.gif" width="700px">

## Setup

Your instruction team will provide a link for you to create your assessment repository. Once your repo is created, clone it to your machine.

1. Make sure you are in your `workspace` directory.
1. `git clone {github repo SSH string}`.
1. `cd` into the directory it creates.
1. `code .` to open the project code.
1. Use the `serve` command to start the web server.
1. Open the URL provided in Chrome.

Make sure your Developer Tools are open at all times while working on this project. Use the messages provided in the Console to determine what code needs to be fixed or implemented, and use breakpoints in the Sources tab to step through your code as you debug.

## Vocabulary and Understanding

Before you click the "Complete Assessment" button on the Learning Platform, add your answers below each question and make a commit.

1. When a child is clicked on in the browser, which module contains the code that will execute on that event happening? Can you explain the algorithm of that logic?
   > That user action is contained in the Kids.js module. When the user initiates the click event, it grabs our target element. If the element has datatype of "child", it prompts a browser alert with the string of elements containing innerText, which is the name, and the wish value.
2. In the **Pairings** module, why must the `findCelebrityMatch()` function be invoked inside the `for..of` loop that iterates the kids array?
   > To be paired at all, the celebrityId for each child needs to be read first, as it's the only connection between the childId and the celebrity that they picked. In order to achieve that in Pairings.js, we iterate through every child in database.js so that we can read and then interpolate the value of celebrityId into the HTML string. Obviously, we shouldnt print the string until we have all of the necessary values included in the HTML template literal. 
3. In the **CelebrityList** module, can you describe how the name of the sport that the celebrity plays can be displayed in the window alert text?
   > Yes, we stored the sport of the celebrity in data-sport on each of the <li> elements displayed on the DOM. The user clicks on the celebrity and the event listener gets the value from dataset.sport of the element that was clicked, which is then included in the alert. 
4. Can you describe, in detail, the algorithm that is in the `main` module?
   > 1. Importation of all peripheral, single functionality modules; Kids.js, CelebrityList.js and Pairings.js. 2. A template literal, applicationHTML, is assigned to a variable which provides structure to the DOM and interpolates components of the imported functions. 3. innerHTML from the container is assigned the value of the HTML string from step 2 which is rendered onto the DOM. 
