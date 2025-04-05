# What is Angular?

- Angular is a frontend JavaScript framework used to build user interfaces (UI) for web applications. It enables the creation of interactive, modern web UIs.
- It provides a collection of tools and features to build web applications ranging from simple to complex.
- Angular simplifies the development process by providing structured rules, features, and concepts that streamline the building of complex web applications.

# Why Use a Framework?

- **Declarative Code**: Unlike vanilla JavaScript, which requires step-by-step explicit instructions, Angular allows developers to write declarative code. This means defining the desired state or states, and Angular manages the details to reach those states.

  - **Vanilla JavaScript**: Requires explicit, step-by-step instructions.
  - **Declarative JavaScript**: Used by Angular to define target states with special instructions, simplifying the development process.

- **Component-Based Architecture**: Angular uses components, which are custom HTML templates, to build the overall interface. This approach breaks the application into simpler, reusable blocks, making both UI development and logic management easier and more modular.

- **Object-Oriented Principles**: Angular embraces certain object-oriented programming (OOP) principles and concepts, which can help in organizing and maintaining code.

- **TypeScript Integration**: Angular uses TypeScript instead of JavaScript. TypeScript is a superset of JavaScript that includes strict and strong typing, making it easier to catch errors during development and improving code maintainability.

# Creating an Angular Project

- [text](https://angular.dev/tools/cli)
- [text](https://nodejs.org/en)

- npm install
- npm start

# JavaScript Refresher: Classes, Properties & More

Angular makes heavy use of classes - a feature that's supported by vanilla JavaScript and TypeScript (though TypeScript "extends" it and adds some extra features as you'll see).

A class is essentially a blueprint for objects. Any properties and methods defined in the class will exist on all objects that are created based on the class.

For example, if you had this class (in vanilla JavaScript):

class Person {
constructor(name, age) {
this.name = name;
this.age = age;
}

greet() {
console.log('Hi, I am ' + this.name);
}
}
You could instantiate it (and create objects) like this:

const person1 = new Person('Max', 35);
const person2 = new Person('Anna', 32);
And you could then access the properties and methods defined by the class:

console.log(person1.age);
person2.greet();
When using Angular, you'll often define classes which are NEVER instantiated by you!

For example, components are created as classes - i.e., you create blueprints for custom HTML elements. But it's Angular that actually instantiates the classes in the end. You never call new SomeComponent() anywhere in your code.

In addition, Angular uses TypeScript - therefore, you often use TS-supported "enhancements" to classes.

For example decorators:

@Component({})
class SomeComponent {}
Decorators like @Component are used by Angular to add metadata & configuration to classes (and other things, as you'll see throughout the course).

In addition, TypeScript gives you more control over how properties are defined in classes.

You can, for example, mark properties (and methods) as private, public (the default) and protected to control which parts of your code can access which property (or method). You can learn more about these keywords here.

And, in general, you can learn more about TypeScript's support for classes here.

That being said, you don't have to study classes in-depth right now. You'll see most of those important features in action throughout this course.

For the moment, it's just important to understand that this classes feature exists, what it does (= create blueprints for objects) and how to work with classes.

# Generating Components in Angular 18

In Angular, components are the building blocks of the application UI. The Angular CLI provides powerful commands to generate components, reducing the need for manual setup.

ng generate component

The primary command to generate a new component in Angular 18 is:

ng generate component component-name

or its shorthand:

ng g c component-name

What This Command Does:

Creates a new folder with the component name inside the current working directory.

Generates four files:

component-name.component.ts (TypeScript file for logic)

component-name.component.html (Template file for UI)

component-name.component.css/scss/less (Styles file based on project configuration)

component-name.component.spec.ts (Test file for unit testing)

Automatically declares the component in the nearest Angular module (if applicable).
