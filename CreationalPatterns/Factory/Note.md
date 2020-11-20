## Overview
------------------------------------------

* It doesn't require us to use a constructor.
* Instead, a Factory can provide a generic interface for creating objects, where we can specify the type of factory object we wish to be created.
* Imagine that we have a UI factory where we ask to create a type of UI component.
* Rather than creating this component directly using the `new` operator, we ask a Factory object for a new component instead. 
* We inform the Factory what type of object is required (e.g "Button", "Panel") and it instantiates this, returning it to us for use.

## When To Use The Factory Pattern
------------------------------------------

* When our object or component setup involves a high level of complexity
* When we need to easily generate different instances of objects depending on the environment we are in
* When we're working with many small objects or components that share the same properties
* When composing objects with instances of other objects that need only satisfy an API contract (aka, duck typing) to work. This is useful for decoupling.

## When Not To Use The Factory Pattern

* When applied to the wrong type of problem, this pattern can introduce an unnecessarily great deal of complexity to an application.
* Unless providing an interface for object creation is a design goal for the library or framework we are writing, I would suggest sticking to explicit constructors to avoid the unnecessary overhead.
* Due to the fact that the process of object creation is effectively abstracted behind an interface, this can also introduce problems with unit testing depending on just how complex this process might be.

## Abstract Factory
------------------------------------------
* It is also useful to be aware of the Abstract Factory pattern, which aims to encapsulate a group of individual factories with a common goal.
* It separates the details of implementation of a set of objects from their general usage.
* An Abstract Factory should be used where a system must be independent from the way the objects it creates are generated or it needs to work with multiple types of objects.
