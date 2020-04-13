# week-12 was a very interesting week.


# Method-function-kill was a home work assigned to us to exercise our  objects skills. We learned how to create objects that had functions. 

const newPerson = function(firstName = 'Anonymous', lastName = 'Person', age, married = false){
  
  const newPerson = {
    firstName: firstName,
    lastName: lastName,
    age: age,
    married: married,

    goingOn: function(){
      age  = this.age
    return age + 1
    },

    ageUp: function(){
    this.age = this.age + 1
    },
    getFullName: function(){
      return  this.firstName + this.lastName
    },
    marry: function(person2){
      this.married = true
      person2.married = true
      
    },

    divorce: function(person2){
      this.married = false
      delete this.spouseName
      person2.married = false
      delete person2.spouseName
    }
  };
return newPerson;
};






/*********************************
 * OUR CODE BELOW; DO NOT TOUCH! *
 *********************************/

if (typeof newPerson === 'undefined') {
  newPerson = undefined;
}


module.exports = {
  newPerson,
}


## we learned about how to use methods


const makeDino = function(name, isCarnivore) {
  const newObj = {
    name: name,
    isCarnivore: isCarnivore,
    humansEaten: 0,

    sayHi: function() {
      const diet = this.isCarnivore ? 'carnivorous' : 'herbivorous';
      return `Rawr! I'm a ${diet} ${this.name}!`;
    },

    switchDiet: function() {
      if (this.isCarnivore === true) {
       this.isCarnivore = false;
      } else {
        this.isCarnivore = true;
      }
    },

    eatMeal: function() {
      if (this.isCarnivore) {
        this.humansEaten += 2;
      }
    },

    eatMeals: function(mealsToEat) {
      let mealsEaten = 0;
      while (mealsEaten < mealsToEat) {
        this.eatMeal();
        mealsEaten++;
      }
    },
  };

  return newObj;
}
