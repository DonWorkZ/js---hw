<!-- Recall how to create a class object using a constructor function for instance properties and a prototype method for behavior common to all instances of the class. Here's an example:
 
function Dog (name, breed, isGoodBoy) {
    this.name = name;
    this.breed = breed;
    this.isGoodBoy = isGoodBoy;
}
Dog.prototype = {
    constructor: Dog,
    sit: function () {
        // sitting code here
    },
    fetch: function () {
        // fetching code here
    }
}
 
Following this example, create two different types of classes using constructor functions and prototype methods: a Traveler and a Wagon.
 
A Traveler has a few properties:
a name (string) that must be provided as a parameter to the constructor
an amount of food (number) with an initial value of 1
an isHealthy (boolean) to indicate whether they are sick, with an initial value of true
 
A Wagon has a few properties as well:
a capacity (number) that must be provided as a parameter to the constructor, sets the maximum number of passengers the wagon can hold
a passengers list (array) which is initially empty
Operations
Write the following prototype methods:
 
Traveler.prototype.hunt()
Increase the traveler's food by 2.
 
Traveler.prototype.eat()
Consumes 1 unit of the traveler's food. If the traveler doesn't have any food to eat, the traveler is no longer healthy.
 
Wagon.prototype.getAvailableSeatCount()
Return the number of empty seats, determined by the capacity set when the wagon was created, compared to the number of passengers currently on board.
 
Wagon.prototype.join(traveler)
Add the traveler to the wagon if there is space. If the wagon is already at maximum capacity, don't add them.
 
Wagon.prototype.shouldQuarantine()
Return true if there is at least one unhealthy person in the wagon. Return false if not.
 
Wagon.prototype.totalFood()
Return the total amount of food among all occupants of the wagon.
 
Testing
At the bottom of the file, there are tests to help you verify that your code is working.  
Run the test code and make sure those are working as you would expect.

RUBRIC FOR ME THAT I HAVE TO FOLLOW
Activity

Wagon class has these properties: capacity and passengers (initialized to an empty array)

Wagon prototype has these methods: getAvailableSeatCount, join, shouldQuarantine, and totalFood

Traveler class has these properties: name, food (initialized to 1), and isHealthy (initialized to true)

Traveler prototype has these methods: hunt and eat

Testing code from the assessment description is present and unmodified -->