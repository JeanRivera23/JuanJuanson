# Jeanette Rivera - Juan Juanson Notes

---

**Directions:**

1 - Anytime you see code, follow along in terminal.

2 - Create a cheatsheet from Lesson Objectives and submit github link of file to slack when done.

3 - Notify Liza via slack when done so you can get the lab.

---

**Lesson Objectives:**

- Explain the relationship between `.new()` and `def initialize()`.

  - `.new()` is used to instantiate (create) a new instance of a class.

  - `def initialize()` (the initialize method), is a method that is carried out (runs) automatically when a new instance of a class is instantiated (`.new()` is used).


- Define class, subclass, instance, and self.

  - **class** is like an object blueprint. It holds all the default attributes (traits) and methods (things it does) of an object (the structure/layout).

  - **sub class** a class that inherits all attributes and methods from the parent class (use < to denote inheritance).

  - **instance** is an instance of a class (a customized duplicate of a class)

  - **self** an instance's way of referring to itself.


- Properly define `instance` and `class` variables.

  - `instance variables` are denoted by the @ symbol, only available within the instance you created. They store instance traits.

  - `class variables` are denoted by the @@ symbols, every instance of a class will have the same class variable value. It can't be accessed with the `attr_accessor`.


- Properly define `instance` and `class` methods.
  - `instance methods` are methods called on the instance.

  - `class methods` are methods called on the class, named with the class name or `self.` followed by the function name.

- Distinguish whether a piece of data is best suited to being stored in a local, instance, or class variable.

  - **local variables** are good to use for cases when you don't need to access the value of a variable outside of the method or instance in which it was created.

  - **instance variables** are good to use for cases when you need to access the value of a variable outside of the method and inside the entire instance in which it was created.

  - **class variables** are good to use for cases when you want to access the value of variables in each instance of a class.


- Describe the relationship of `attr_` and "getter" and "setter" methods.

  - **"setter"** the purpose of the setter is to take whatever argument is passed into an instance and assign it as the new value of the instance variable. So this will also allow for changes in instance variable values.

  - **"getter"** the purpose of the getter method is to retrieve/return the instance variable.

  - `attr_writer` shortcut for setter methods, only creates a setter method.

  - `attr_reader` shortcut for getter methods, only creates a getter method.

  - `attr_accessor` shortcut for `attr_writer` and `attr_reader`, limits repeated code even more. Creates both a getter and setter method all at once.


- Distinguish whether a piece of data is best suited to having its accessibility defined by attr_reader, attr_writer, attr_accessor or none of the above.

  - If you want the ability to read and overwrite (set) the value of an instance variable than it's more efficient to use the `attr_accessor`.

  - If you only want to read an instance variable and not be able to overwrite (set) a new value to initial argument, then using the `attr_reader` is best.

  - If you have several instance variables and you want to be able to read all and overwrite (set) some of those, then you can use both the `attr_reader` on all instance variables and the `attr_writer` just on the instance variables you'd like to be able to overwrite (set).
