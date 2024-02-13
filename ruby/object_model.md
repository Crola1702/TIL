# Ruby object model

> From [Deep dive into ruby's object model](https://blog.devops.dev/a-deep-dive-into-rubys-object-model-pt-1-6dcddfba37b4)

Everything in ruby is an object. This is the base of Ruby's metaprogramming capabilites (metaprogramming understood as modify code behavior in the run).

The `Class` keyword is helpful to create blueprints for objects. An object is an instance of a specific class.

Instance variables are associated to objects. Instance methods are actually inherited from classes.


Classes are also ruby objects. But ruby objects come from classes. How does it work?

A Class is a specialization of an Object for which the methods `:new, :allocate, :supperclass` are created.

`:new` method is used to create instances of the class. Also, `:supperclass` is a method to check what's the parent class of an object. Here is an interesting fact about `Class` class superclass and `Object` class superclass:

```ruby
class MyClass; end
MyClass.class           # Out: Class
MyClass.superclass      # Out: Object

Class.superclass        # Out: Module
Module.superclass       # Out: Object
Object.superclass       # Out: BasicObject
BasicObject.superclass  # Out: nil

Class.class             # Out: Class
Module.class            # Out: Class
Object.class            # Out: Class
BasicObject.class       # Out: Class

MyClass.new.class       # Out: MyClass
MyClass.new.superclass  # ERROR: (Instances don't have superclasses)
```

So every `Class` instance contains a superclass. The superclass of a new defined Class is an Object, and the Class of an Object is `Class`.


Also, the `Class` object is a specialization of a Module, which is a special type of Object. And an Object is a special type of BasicObject.






