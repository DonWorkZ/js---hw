<!-- Then copy your code from part one (just your code, not the tests!) and paste it into inheritance.js in the new repository.
 
Recall how to use inheritance/delegation to extend a class object, creating a new variation on the original class. Here's an example:
 
function Dog (name, breed, isGoodBoy) {
    this.name = name;
    this.breed = breed;
    this.isGoodBoy = isGoodBoy;
}
Dog.prototype = {
    constructor: Dog,
    sit: function () {
        // sitting code here
    }
}
function GuardDog (name, breed, isGoodBoy, attackWord) {
    Dog.call(this, name, breed, isGoodBoy);
    this.attackWord = attackWord;
}
GuardDog.prototype = Object.create(Dog.prototype);
GuardDog.prototype.constructor = GuardDog;
GuardDog.prototype.bark = function () {
    // barking code here
}
 
For this assessment, you will extend your Oregon Trail code to use inheritance to create two new types of traveler: Doctor and Hunter. They will have all of the features of any other Traveler, but with these differences:
 
A Doctor is a Traveler with one additional method:
 
Doctor.prototype.heal(traveler)
Pass another Traveler as a parameter to the .heal() method, and their isHealthy property is changed to true.
 
 
A Hunter is a Traveler that is better at finding food, but requires more food to eat. They should start out with 2 food instead of just 1 like other travelers do. They can also give food to other travelers:
 
Hunter.prototype.hunt()
Increase the hunter's food by 5. (A normal traveler gains only 2.)
 
Hunter.prototype.eat()
Consumes 2 units of the hunter's food. If the hunter doesn't have 2 food when they are instructed to eat, they eat as much as they can (0 or 1 unit), but the hunter is no longer healthy. (A normal traveler eats only 1 unit of food.)
 
Hunter.prototype.giveFood(traveler, numOfFoodUnits)
Transfers numOfFoodUnits from the hunter to a different traveler. If the hunter has less food than they are being asked to give, then no food should be transferred.
 
Testing
At the bottom of the file, there are tests to help you verify that your code is working.  
Run the test code and make sure those are working as you would expect.
 
 Notice these tests are different from the test in part one!  Make sure you don’t overwrite the new tests when pasting your old code in. -->

 RUBRIC FOR ME THAT I HAVE TO FOLLOW
 Use .call() inside your child class' constructor to inherit the behavior of your parent class' constructor.

Use Object.create() to make your child class' prototype inherit your parent class' prototype.

Set the ChildClass.prototype.constructor property to your ChildClass constructor.

Testing code from the assessment description is present and unmodified

The testing code's 10 console.log statements are present and print out the expected values