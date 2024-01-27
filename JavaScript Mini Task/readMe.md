JavaScript Documentation
Basics
Printing to Console
// Using the println() function will print the text and create a line break 
// Example of using println()
println("Hello");
println("world.");
// Result:
// Hello
// world.

// Using the print() statement does NOT create a line break
// Example of using print()
print("Hello world. ");
print("How are you?");
// Result:
// Hello world. How are you?

// You can also print to the console using console.log() (includes line break)
// Example:
console.log("Hello world!");
Variables
// Declare a variable
var myVarName;

// Initialize a variable
var myVarName = 5;

// Assign to an existing variable
myVarName = 10;

// Print a variable
println(myVarName);
println("The value is: " + myValue);

// Variables can also be declared and initialized using the keyword 'let'
let myVarName;
let myVarname = 5;

// If a variable isn't going to change its value, it is best to use the keyword 'const'
/*
 * Variables defined with const cannot be redeclared
 * Variables defined with const cannot be reassigned
 * Variables defined with const must be assigned a value when they are declared
 */
// Example:
const PI = 3.141592653589793;
PI = 5;      // This will give an error
User Input
// Read a string
// Strings are a series of characters - ex: Hello World
var str = readLine(prompt);

// Read an integer
// Integers are numbers without a decimal point - ex: 3
var num = readInt(prompt);

// Read a float
// Float are numbers with a decimal point - ex: 3.14
var cost = readFloat(prompt);

// Read a boolean
// Boolean are true/false
var bool = readBoolean(prompt);

// You should replace the word prompt with
// the question you'd like to ask. For example:
var name = readLine("What is your name? ");
var age = readInt("What is your age? ");
var finishedWork = readBoolean("Is your work done? ");
Asynchronous User Input

/* In addition to the blocking input methods that receive input via 
popup, there are additional asynchronous input methods. readLineAsync, 
readIntAsync, readFloatAsync, and readBooleanAsync are non-blocking 
functions that can be used in combination with the `await` keyword to 
receive input asynchronously.
*/

let name = await readLineAsync("What's your name? ");
console.log("Nice to meet you, " + name);
        
To read more about asynchronous user input, see this tutorial.
Math
// Operators:
+	Addition
-	Subtraction
*	Multiplication
/	Division
**  Exponentiation
%	Modulus (Remainder)
()	Parentheses (For order of operations)

// Examples
var z = x + y;
var w = x * y;

// Increment (add one)
x++

// Decrement (subtract one)
x--

// Shortcuts
x = x + y;		x += y;
x = x - y;		x -= y;
x = x * y;		x *= y;
x = x / y;		x /= y;

// Exponentiation
var squared = 5 ** 2;
println(squared);   // prints out 25

// Modulus
var z = 10 % 4             // 2 * 4 = 8; 10 - 8 = 2
println(z)                 // prints out: 2

// Absolute value
var abs = Math.abs(x);

// Square root
var sqrt = Math.sqrt(x);

// Rounding
// Math.round() can be used to round numbers
var pi = 3.14;
var roundedPi = Math.round(pi);
println(roundedPi);				// prints out: 3

var goldenRatio = 1.618;
var roundedGoldenRatio = Math.round(goldenRatio);
println(roundedGoldenRatio);		// prints out: 2

// Floor Division
// Math.floor() can be used to perform floor
// division. With floor division, only the
// integer portion of the quotient is returned.

// For example, 5/2 is 2.5, but with floor division,
// the result is 2 and the .5 is discarded.
var result = Math.floor(5/2);
println(result);					// prints out: 2

// Geometry
// Note input is in radians, not degrees

Math.sin(radians); // Returns value between -1 and 1
Math.cos(radians); // Returns value between -1 and 1
Math.tan(radians); // Returns value

Random Numbers
// Random integer between low and high
Randomizer.nextInt(low, high);
Randomizer.nextBoolean();
Randomizer.nextFloat(low, high);
Randomizer.nextColor();

var roll = Randomizer.nextInt(1,6);

var color = Randomizer.nextColor();
Strings
// str.length
// returns the length of a string

// Example
var str = "hello";
var len = str.length; // equals 5

// str.indexOf(search)
//  returns the first index of the search
// or -1  if not found. It is case sensitive.

//Examples
var str = "hello";
var pos1 = str.indexOf("l"); // returns 2

var pos2 = str.indexOf("H"); // returns -1

// str.substring(start);
// returns a substring including the
// character at start to the end of the
// string

//Examples
var str = "hello";
var sub1 = str.substring(1); // equals "ello"
var sub2 = str.substring(3); // equals "lo"

// str.substring(start, end);
// returns a substring including the
// character at start, but not including
// the character at end

//Examples
var str = "hello";
var sub1 = str.substring(0,2); // equals "he"
var sub2 = str.substring(1,4); // equals "ell"

Functions
// Functions can take in values, called parameters.
// The function below takes in a parameter called
// 'input' and prints it.
function printText(input) {
    println(input);
}

// Functions can also return a value.
// The function below takes in a value,
// adds two to it, and returns it.
function addTwo(number) {
	return number + 2;
}
Graphics
CodeHS Library
Check out our full documentation for the CodeHS Graphics Library!
Canvas
// returns the width of the canvas
getWidth();

// returns the height of the canvas
getHeight();

// Example returns the y coordinate of the
// center of the canvas
var CENTER_Y = getHeight() / 2;

// Example returns the x coordinate of the
// center of the canvas
var CENTER_X = getWidth() / 2;

// Removes all objects from the canvas
removeAll();
Circles
// To make a circle
var circle = new Circle(radius);

// To set the location of the center of the circle
circle.setPosition(x, y);

// Example, red circle with 50px radius with center at (100, 200)
var circle = new Circle(50);
circle.setPosition(100, 200);
circle.setColor(Color.red);

// Get the radius
circle.getRadius();					// returns 50
var curRadius = circle.getRadius();	// store in variable

// Change the radius
circle.setRadius(100);

// Get the position of the center of the circle
var x = circle.getX();  // x is 100
var y = circle.getY();  // y is 200

// Change the location of the circle
var x = getWidth() / 2;
var y = getHeight() / 2;
circle.setPosition(x, y);   // circle center is in the center of the screen

// Adding to and removing from screen
add(circle); // Add to screen
remove(circle); // Remove from screen

// Move the circle dx horizontally and dy vertically
circle.move(dx, dy);
Rectangles
// To make a rectangle
var rect = new Rectangle(width, height);

// To set location of the upper left corner of rectangle
rect.setPosition(x, y);

// Example, 200x50 blue rectangle with upper left corner at (100, 200)
var rect = new Rectangle(200, 50);
rect.setPosition(100, 200);
rect.setColor(Color.blue);

// Get location of the upper left corner of the rectangle
var x = rect.getX(); // x is 100
var y = rect.getY(); // y is 200

// Change location of the rectangle
var x = getWidth() / 2;
var y = getHeight() / 2;
rect.setPosition(x, y)  // upper left corner is at center of screen

// Adding to and removing from screen
add(rect); // Add rectangle
remove(rect); // Remove rectangle

// Move the rect dx horizontally and dy vertically
rect.move(dx, dy);
Arcs
// To make an arc
var myArc = new Arc(radius, start, end, unit);

// More specifically, the parameters are:
//    1. radius of the arc
//    2. starting angle of the arc
//    3. ending angle of the arc
//    4. angle unit (0 for degrees, 1 for radians)

// To set the position of the center of the arc
myArc.setPosition(x, y);

// Example, a 90-degree arc with
// radius of 50 and color of red:
var myArc = new Arc(50, 0, 90, 0);
myArc.setPosition(100, 200);
myArc.setColor(Color.red);

// Get the location of the center of the arc
var x = myArc.getX();   // x is 100
var y = myArc.getY();   // y is 200

// Change the location of the center of the arc
var x = getWidth() / 2;
var y = getHeight() / 2;
myArc.setPosition(x, y);    // arc center is at center of screen

// Adding to and removing from screen
add(myArc); // Add arc
remove(myArc); // Remove arc
Lines
// To draw a line from (x1, y1) to (x2, y2)
var line = new Line(x1, y1, x2, y2);

// Set the line color to green
line.setColor(Color.green);

// Set the line width to 10 pixels
line.setLineWidth(10);

// Adding to and removing from screen
add(line);
remove(line);

// Move the line dx horizontally and dy vertically
line.move(dx, dy);

// Change the starting point of the line to (x1, y1)
line.setPosition(x1, y1);

// Change the end point of the line to (x2, y2)
line.setEndpoint(x2, y2);

//Get the starting point of the line
var x = line.getX();    // x has same value as x1
var y = line.getY();    // y has same value as y1
Ovals
// To make an Oval
var oval = new Oval(width, height);

// To set location of the center of the oval
oval.setPosition(x, y);

// Example, 200x50 blue oval with center at (100, 200)
var oval = new Oval(200, 50);
oval.setPosition(100, 200);
oval.setColor(Color.blue);

// Get location of the center of the oval
var x = oval.getX(); // x is 100
var y = oval.getY(); // y is 200

// Change location of the oval
var x = getWidth() / 2;
var y = getHeight() / 2;
oval.setPosition(x, y)  // oval's center is at center of screen

// Adding to and removing from screen
add(oval); // Add oval
remove(oval); // Remove oval

// Move the oval dx horizontally and dy vertically
oval.move(dx, dy);
Polygons
// To make a polygon
var polygon = new Polygon();

// To add points to the polygon
polygon.addPoint(x, y);

// Example, 4-sided green polygon
// NOTE: The order in which you add the points determines how the polygon is drawn
var polygon = new Polygon();
polygon.addPoint(20, 20);
polygon.addPoint(10, 50);
polygon.addPoint(100, 80);
polygon.addPoint(60, 10);
polygon.setColor(Color.green);

// Check if polygon contains a point
polygon.containsPoint(x, y); // returns boolean

// Adding to and removing from screen
add(polygon); // Add polygon
remove(polygon); // Remove polygon

// Move the polygon dx horizontally and dy vertically
polygon.move(dx, dy);
Text
// To make a graphical text object
var txt = new Text(label, font);

// To set the position of the lower left corner of the text
txt.setPosition(x, y);

// Example
var txt = new Text("Hello, world!", "30pt Arial");
txt.setPosition(100, 200);
txt.setColor(Color.blue);

// Change what the text says
txt.setText("Goodbye!");

// Get the location of the lower left corner of text
var x = txt.getX(); // x is 100
var y = txt.getY(); // y is 200

// Change the location of the text
var x = getWidth() / 2;
var y = getHeight() / 2;
txt.setPosition(x, y)   // text's lower left corner is
						// in the center of the screen

// Adding to and removing from screen
add(txt); // Add text
remove(txt); // Remove text

// Move the text dx horizontally and dy vertically
txt.move(dx, dy);
Images
// A web image can be added to the graphics canvas
// as a WebImage. WebImages are created, sized,
// and positioned much like other graphics objects.

// To create a new WebImage, use a URL that links
// directly to the image on the Internet.
// Use the Upload Tab in the editor to upload and create
// a valid URL for your own image.

var copter = new WebImage("https://upload.wikimedia.org/" +
						  "wikipedia/commons/4/41/" +
						  "Bell_206L3_%28D-HASA%29.jpg");
copter.setSize(300, 150);
copter.setPosition(getWidth()/4, getHeight()/2);
add(copter); // Adding copter to screen
remove(copter); // Removing copter from screen

// Note that the URL to the image must be directly
// to the image file itself. It should generally end with
// something like .png, .jpg, or another image file type.

Images Hosted on CodeHS
https://static.codehs.com/img/library/characters/penguin.png
https://static.codehs.com/img/library/characters/monkey.jpg
https://static.codehs.com/img/library/characters/leopard.jpg
https://static.codehs.com/img/library/characters/chameleon.jpg
https://static.codehs.com/img/library/characters/lizard.jpg
https://static.codehs.com/img/library/characters/butterfly.jpg
https://static.codehs.com/img/library/objects/icicle.png
https://static.codehs.com/img/library/objects/helicopter.png
https://static.codehs.com/img/library/objects/asteroid.png
https://static.codehs.com/img/library/objects/soccerBall.png
https://static.codehs.com/img/library/landscapes/flowers.jpg
Color
You can visit the W3Schools CSS Colors page for a list of colors.
// You can use the setColor() method to give your objects a color.
// like this:
obj.setColor(color);

// You can pass in to setColor() any css color name as a string.
// Refer to the link above for a list of possible color names

// For example, here is how we set a circle to be teal:
circle.setColor("teal");

// You can also make your own color by giving a red, green,
// and blue component like
var color = new Color(r, g, b);

// The values are between 0-255 for each component. After making
// a new color, you can use it to set the color of an object.

// For example, to set an existing rectangle called
// rect to be brown:
var brown = new Color(139, 69, 19);
rect.setColor(brown);

// Another way to set the color of an object is to use a
// string with the hexadecimal color value with setColor.
// For example, to set a rect object to be pink:
rect.setColor("#FF66CC");

// There are also many color constants. You can set an objects
// color like
obj.setColor(Color.RED);

// List of available colors:
Color.RED
Color.GREEN
Color.BLUE
Color.YELLOW
Color.CYAN
Color.ORANGE
Color.WHITE
Color.BLACK
Color.GRAY
Color.PURPLE

// Other fun functions
// Return a random color
var color = Color.randomRed();
var color = Color.randomGreen();
var color = Color.randomBlue();

// Get a random color from the randomizer
var color = Randomizer.nextColor();
Rotation
/**
* The following graphic objects can be rotated:
* - Rectangle
* - Arc
* - Line
* - Oval
* - Text
* - WebImage
*/

// Set the rotation of the rectangle with these parameters:
//    1. angle to rotate
//    2. angle unit (0 for degrees, 1 for radians)
//       This will default to degrees.

// Sets rotation of the rectangle to 45 degrees
rect.setRotation(45, 0);           
rect.setRotation(45);       // Does the same thing.

// Sets rotation of the rectangle to Math.PI/2 radians
rect.setRotation(Math.PI / 2, 1);  

// Add rotation with these parameters:
//    1. angle to rotate
//    2. angle unit (0 for degrees, 1 for radians)
//       This will default to degrees.

// Rotates the rectangle by 45 degrees
rect.rotate(45, 0);     
rect.rotate(45);        // Does the same thing.

// Rotates the rectangle by Math.PI/2 radians
rect.rotate(Math.PI / 2, 1);
Graphics Type and Layers

// To get the type of the object:
var type = obj.getType();

// could return: 'Circle', 'Rectangle', 'Text', 'Line', or 'WebImage'


/* You can change the order of your graphics by
 * using the layer property. Setting the layer
 * to 0 sends the graphic to the very back of the canvas.
 * The graphic with a higher layer number will be
 * drawn on top of objects with a lower layer number.
 * The default layer of a graphic is 1.
 */

obj.layer = 1; // moves the graphic forward to 1 layer
obj2.layer = 5; // will be drawn on top of layers 0 - 4

Debug Mode and Anchors

/* 
 * The debug method can be used to see where 
 * an object's anchor point is located
 * By default, a circle's anchor point is 
 * at its center and a rectangle's anchor point
 * is located at its top-left corner.
 * The debug method evaluates a boolean and can
 * be set to 'true' for any object
 */ 

// The debug method is set to 'false' by default
// Here's how you can turn it on for a circle object:
var circle = new Circle(50);
circle.debug = true;

/*
 * You can also change an object's anchor point
 * by using setAnchor()
    * An anchor of 0, 0 will cause the shape to 
      draw with its position at its top left corner
    * An anchor of 0.5, 0.5 will cause the shape
      to draw with its position at its center
    * An anchor of 1, 1 will cause the shape to
      draw with its position at its bottom right corner
 */
 
// Here's how you can change the anchor point of
// a rectangle to be at the bottom right corner:
var rect = new Rectangle(50, 25);
rect.setAnchor({vertical: 1, horizontal: 1});
 
// Note: it is best to change the anchor point while debug mode is on
Control Structures
Booleans
// A boolean is either true or false
var myBoolean = true;

var anotherBoolean = false;

var result = readBoolean("Question? ");

// Not Operator
var x = !y; 	// x gets the opposite of y

// And Operator
var andExp = x && y;

// Or Operator
var orExp = x || y;

// You can combine many booleans!
var boolExp = x && (y || z);
If Statements, If/Else, If/Else If/Else
if(BOOLEAN_EXPRESSION){
	// code to execute if true
}

if(BOOLEAN_EXPRESSION){
	// code if true
} else {
	// code if false
}

if(x < 0){
	println("x is negative.");
}

if(color == "red" || color == "blue" || color == "yellow"){
	println("Primary color.");
} else {
	println("Not a primary color.");
}

// You can use else if if you have multiple
// conditions, but only one should happen.
if(condition_1){

} else if(condition_2) {

} else if(condition_3) {

} else {

}


// You can always write these using nested
// if/else. For example:
if(condition_1){
	// code here runs if condition 1 is true
} else {
	if(condition_2){
		// if condition 2 is true
	} else {
		// and here if condition 2 is false
	}
}
For Loops
var COUNT = 5;

for(var i = 0; i < COUNT; i++){
	/* Repeat code betweeen the brackets 5 times,
	 * as the COUNT variable is 5. */
}

// Print numbers 0-9
for(var i = 0; i < 10; i++){
	println(i);
}
While Loops
while(boolean expression){
	/* Repeat code betweeen brackets while
	 * 'boolean expression' is true */
}

// Countdown from from 15 to 10
var i = 15;
while(i > 9){
	println(i);
	i--;
}
// This is a loop and a half format
while(true){
	// code
	if(condition){
		break;
	}
}
Animation
Timers
setTimer(fn, delay); // Create a timer
stopTimer(fn); 		 // Stop a timer

// Example: call moveBall every 40 milliseconds
function start() {
	setTimer(moveBall, 40);
}

function moveBall() {
	ball.move(x, y);
}

Mouse Events
// Mouse events are used to create programs
// that respond to users' mouse clicks, drags,
// and movements.

// When the mouse event occurs, the function
// registered with the event will be called. Note
// that you leave out the parentheses () when
// passing the name of the function.

// Here is a list of mouse events that can be used:
mouseMoveMethod(functionToCall);	// on mouse movement
mouseClickMethod(functionToCall);	// on mouse clicks
mouseDragMethod(functionToCall);	// on mouse drags
mouseDownMethod(functionToCall);	// mouse button depressed
mouseUpMethod(functionToCall);		// mouse button released

// Sample program using mouse events
function start() {
	// Set up mouse callbacks
	mouseMoveMethod(onMouseMove);
	mouseClickMethod(addBall);
	mouseDragMethod(updateLine);
}

function onMouseMove(e) {
	println("Mouse is at (" +
			e.getX() + ", " +
			e.getY() + ").");
}

function addBall(e) {
	var ball = new Circle(20);
	ball.setPosition(e.getX(), e.getY());
	add(ball);
}

function updateLine(e) {
	line.setEndpoint(e.getX(), e.getY());
}

// The function getElementAt(x, y) can be used to grab
// an object, if one exists, at the coordinates
// (x, y). If none present, returns null

// Example
function start() {
    mouseClickMethod(turnRed);
}

// If you click on an object, turn it red.
function turnRed(e) {
    var elem = getElementAt(e.getX(), e.getY());
    if (elem != null) {
        elem.setColor("red");
    }
}

Keyboard Events
function start() {
	// Set up keyboard callbacks
	keyDownMethod(keyDown);
	keyUpMethod(keyUp);
}

function keyDown(e) {
	if (e.keyCode == Keyboard.LEFT) {
		ball.move(-5, 0);
	}
	if(e.keyCode == Keyboard.letter('K')){
		println("You pressed K");
	}
}

function keyUp(e) {
	println("You lifted up a key");
}
Audio Files
// To add a sound file to a program, first create a variable
// to store the sound you want. Be sure to use a link
// directly to the audio file itself (for example,
// if it's an mp3, the link should end with .mp3).
// The link must be a full URL to a sound file that
// is available on the internet.
var mySong = new Audio("link_to_sound_file.mp3");

// To play the file, use .play()
mySong.play();

// To pause a file, use .pause()
mySong.pause();

// To loop a file, first play the file,
// then set .loop to true:
mySong.play()
mySong.loop = true;
Sound
/*
 * Create your own sound waves!
 */

// Construct a new Sound with a given note and sound wave type
var sound = new Sound("C4", "square");
var sound2 = new Sound("C1", "sawtooth");

// Set the tone to either a frequency value or a note value
sound.setFrequency(440);   // 440 Hz
sound.setFrequency("C4");  // Middle C note
sound.setFrequency("A2");  // Low A note
sound.setFrequency("A#8");  // High A sharp note

/*
 * Set the oscillator type for the sound wave. Options are:
 *
 * Basic waves: "square", "sine", "triangle", or "sawtooth"
 * Fat waves: "fatsquare", "fatsine", "fattriangle", or "fatsawtooth"
 * AM waves: "amsquare", "amsine", "amtriangle", or "amsawtooth"
 * FM waves: "fmsquare", "fmsine", "fmtriangle", or "fmsawtooth"
 * Special waves: "pwm", or "pulse"
 * Drum sound: "drum"
 * Cymbal sound: "metal"
 */
sound.setOscillatorType("sine");
sound.setOscillatorType("square");

// Set the volume (in decibels)
sound.setVolume(2);

/*
 * Get information about the sound
 */

var currentVolume = sound.getVolume();
var currentNote = sound.getFrequency();
var currentOscillatorType = sound.getOscillatorType();


/*
 * Adding effects to the sound
 * Options are: "distortion", "reverb",
 * "tremolo", "vibrato", or "chebyshev"
 */

// Add a distortion effect at full capacity
sound.setEffect("distortion", 1);

// Add a tremolo effect at half capacity
sound.setEffect("tremolo", 0.5);

// Add a vibrato effect at 0 capacity
sound.setEffect("vibrato", 0);

/*
 * Starting and stopping the sound
 */

// Play the sound continuously
sound.play();

// Play the sound for 3 seconds
sound.playFor(3);

// Stop playing the sound immediately
sound.stop();

Misc
function start() {
	mouseClickMethod(turnRed);
}

// If you click on an object, turn it red.
function turnRed(e) {
	var elem = getElementAt(e.getX(), e.getY());
	if (elem != null) {
		elem.setColor(Color.red);
	}
}
Data Structures
Arrays
// Create an empty array
var arr = [];

// Create an array with values
var arr = [1, 2, 4];

// An array can have any type
var arr = [4, "hello", x];

// Access an element in an array
var elem = arr[i];

var firstElem = arr[0];

// Set an element in an array
arr[4] = 9;

// Looping over an array
for(var i = 0; i < arr.length; i++){
	var cur = arr[i];
	// process cur
}

// length of an array
var length = arr.length;

// Add to an array
arr.push(elem);

// Remove last element from array
var last = arr.pop();

// Finding the index of an element in a list
var index = arr.indexOf(5);

// Remove an element from a list at index i
arr.remove(i)
Maps/Objects
// Object literal
var obj = {
	name: "Jeremy",
	color: "blue"
};

// Objects/Maps have a collection of key, value pairs

// Set a value
obj["Jeremy"] = "123-4567";

// Get a value for a key
var phone = obj["Jeremy"];

// Loop over an object
for(var key in obj){
	var val = obj[key];
	// process key and val
}
Sets
// Make a new set named "newSet"
var newSet = new Set();

// Add to a set
newSet.add(5);

// Does a set contain a value
newSet.contains(5); // returns a boolean

// Number of elements in the set
var count = newSet.size; // returns an integer

// Make a new set named "setA"
var setA = new Set();
// Add 2 numbers to the set
    setA.add(1);
    setA.add(2);
// Make a new set named "setB"
var setB = new Set();
// Add 2 numbers to the set
    setB.add(2);
    setB.add(3);

// Call the intersect function on "setA" and pass in "setB", store the resulting
// set in a new variable named "mutualSet"
var mutualSet = setA.intersect(setB);
Grids
// Create a grid named "newGrid"
var newGrid = new Grid(rows, cols);

// Get a value in a grid
var elem = newGrid.get(row, col);

// Set a value in a grid
newGrid.set(row, col, val);

// Getting dimensions
var rows = newGrid.numRows();
var cols = newGrid.numCols();

// Is a row, col pair inbounds
newGrid.inBounds(row, col);

// Set all values in grid to initial value
newGrid.init(0); // sets all grid values to 0

// Initialze a grid from an array
newGrid.initFromArray([
	[6, 3, 2],	// 0th row
	[2, 5, 1],	// 1st row
	[4, 3, 9],	// 2nd row
	[1, 5, 1]	// 3rd row
]);
Want more? 
