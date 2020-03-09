# Object Oriented Programming


## Class

Class adalah salah satu fitur baru yang di perkenalkan di javascript versi 2015 atau ES6. Fitur class menyediakan syntax yang lebih sederhana dan rapi untuk membuat blueprint sebuah objek. Perlu di catat bahwa di javascript, class sebenarnya adalah sebuah function namun dengan sintax yang berbedah.

```
class Car {
  
  constructor(type, color) {
    this.type =  type
    this.color = color
    this.engineStatus = 'off'
  }
  
  engineStart () {
    
    this.engineStatus = 'on'
    console.log('engine start')
  }
  
  engingeStop () {
    this.engineStatus = 'off'
    console.log('engine start')
  }
  
  static isEngineOn (car) {
    if (car.engineStatus === 'on') {
      console.log('Engine On')
    } else {
      console.log('Engine off')
    }
  }    
  
}
```

## Static Method

Adalah method yang sama seperti class method, tetapi untuk menjalankannya tidak perlu meng instance class, cukup menggunakan NamaClass.namaMehod()tersebut.

```
class ClassWithStaticMethod {
  static staticMethod() {
    return 'static method has been called.';
  }
}

console.log(ClassWithStaticMethod.staticMethod());
// expected output: "static method has been called."
```

## Method Chaining

Memanggil sebuah method secara berantai yang mempunyai return value yang sama

```
var recipeObj = new Recipe();

recipeObj
.addIngredient('salt')
.addIngredient('pepper')
.getIngredients();

```

## Encapsulation

Sebuah metode untuk membunĀkus properti atau method di dalam class aĀar method
dan property di dalam class tersebut tidak disalahĀunakan

```
function Person()
{
  //properties/fields
  var name = "Rob Gravelle";
  var height = 68;
  var weight = 170;
  var socialInsuranceNumber = "555 555 555";

  //methods/actions
  this.setHeight = function(newHeight) {height=newHeight;}
  this.getHeight = function() { return height; }
  this.setWeight = function(newWeight) {weight = newWeight;}
  this.getWeight = function() { return weight; }
  this.setName   = function(newName) {name=newName;}
  this.getName   = function() { return name; }
  this.setSocialInsuranceNumber  = function(newSocialInsuranceNumber) { socialInsuranceNumber=newSocialInsuranceNumber; }

  return this;
}
//instanciate the Person class
var aPerson = new Person();
var myName = aPerson.name;  //this no longer works
var myName = aPerson.getName();  //this does

```

## inheritance

Inheritance dalam OOP adalah sebuah proses dimana sebuah class mewariskan property dan methodnya ke class lain atau childnya.

```
function Person(first, last, age, gender, interests) {
  this.name = {
    first,
    last
  };
  this.age = age;
  this.gender = gender;
  this.interests = interests;
};


Person.prototype.greeting = function() {
  alert('Hi! I\'m ' + this.name.first + '.');
};
```

## Polymorphism

Mengubah sebuah method dari suatu subclass yang berbeda dengan superclass.

```
const Auto = function(make, model, year) {
    this.make = make;
    this.model = model;
    this.year = year;
};
Auto.prototype.map = function() {
    console.log('Vroom Vroom!');
}
```
