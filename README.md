# Slider Puzzle
Completing this assignment depends on knowing:

- jQuery!

## GitHub Repository
https://github.com/htc-ccis2591/slider-puzzle

You’ll want to begin each assignment by forking the repository and cloning it locally.  When you are done, you’ll push to GitHub and submit a pull request.

## Intro
In this assignment we will make an image slider puzzle using jQuery.  To begin, you will want to download the PuzzlePage starter project from D2L.  Open the HTML file in a browser and you’ll see the puzzle, but it doesn’t do anything yet.

Add a new puzzle.js file to the project and set it up using the module pattern.

Add a function called sliderPuzzle.tileClick().  This method should be called each time one of the cells (td) in the puzzleGrid is clicked on.

The sliderPuzzle.tileClick() method should:
Popup an alert if the user clicked on the “empty” image tile.  Because you will often need to check if a cell is the empty cell, this would make a good function.

if the user did not click on an empty cell, we need to determine which cell next to the image cell is the empty cell so we can swap the tiles.  (Is it above, below, right or left?)

Note: To help with this, the cell ids are numbered to be coordinates.  The first row is numbered cell11, cell12, etc. The second row is numbered cell21, cell22, etc.  Use this pattern to determine the id of the cell you want to check.

When you have identified the location of the empty tile, swap the images between the two cells.  The logic to swap the tiles also makes a good function.  To swap the tiles, you move the image from one cell into the other.

The last thing you’ll need to do is determine if this solves the puzzle.  The following code should help.  It uses the image names (which are the numbers of the pieces) to make a string, then compares that “hash”, against the value for the solution.

function isPuzzleComplete() {
   var hash = "";
   var tiles = $("#puzzleGrid").find("img").each(
       function (index, element) {
           var num = element.src.substr(-6, 2);
           hash += num;
       });
   if (hash == "ty020304050607080910111213141516")
       return true;
   return false;
}


If the puzzle is solved you should change the background image to have the Green border instead of the brown one.

Additional Features
One additional feature is required to get an A.  The others will earn you 5 extra points each applied to your Homework grade.  If you’ve missed assignments or not done as well as you’d like, here is your chance to make some of that back up.  

I have not worked through all of these extras, only imagined them.  I think the first is easiest, and the last the most difficult, but you may feel differently.  
Reset
Add a button to the page so that the puzzle will reset back to the original layout.  There are a few different ways you might do this, and it is up to you to think up some options and decide what works best.  The button should look nice on the page, so this will require a little HTML/CSS too.

Help
Add a help button to the page that will show/hide numbers over the images.  The image number is found in the alt text for the image.  Do NOT show anything for the empty image.  Again, the button should look nice on the page, so this will require a little HTML/CSS too.

Transitions
Use animations to slide the pieces more gracefully from cell to cell.

Extraordinary Win
Do something extra special when the puzzle is solved.  Something more than a “You win” message or flashing colors.  I’m thinking like floating balloons, applause, rainbows or confetti.  We haven’t really talked about these things, so you’ll have to do some research for this one.  

Of course I’ve not provided any extra resources, and you should make sure that anything you add you have rights to use freely.  If any attributions are required, you should add those to a footer in the HTML.  Otherwise, please add a comment to indicate where any additional resources are from.
