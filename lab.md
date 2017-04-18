1- Explain the relationship between .new and def initialize.

  - `.new()` is used to instantiate a new instance of a class and `def initialize()` is a method that runs automatically when a new instance of a class is instantiated.

2- What is the difference between instance and class methods? Give an example from the lesson.

  - `instance methods` are methods called on the instance and `class methods` are methods called on the class, named with the class name or `self.` followed by the function name.

  - Example:
    ```ruby
    class User

      attr_accessor :firstname, :lastname
      @@all = 0

      #instance method
      def initialize(firstname, lastname)
        @firstname = firstname
        @lastname = lastname
        @@all += 1
      end

      #class method
      def User.count
        return @@all
      end

    end
    ```

3- Given this class, rewrite the getter & setter methods the shorter way (attr_):

```ruby
class Robot

  attr_reader :name, :model_num
  attr_writer :name, :model_num

  def initialize(name, model_num)
    @name = name
    @model_num = model_num
  end

  def change_my_name(new_name)
    @name = new_name
  end

end
```

4- Create a Vehicle class

Initialize method:
Enable the class to be initialized with a type, a color & fuel_level (which has a default of 0).
You don’t have to use the options hash. We can assume you will type the arguments in properly.
Some options for types could be: truck, car, motorcycle, etc.
When initialized, the instance “speaks” its type, color & fuel_level. This can be one method or three.
Make it so that you can get and set all 3 of the above variables.
Create the following methods:
These two methods take a parameter speed:
accelerate - increments fuel_level
decelerate - decrements fuel_level
honk - Makes the car beep.
Each take a car part as a parameter:
something_broke: when called, says which car part is broken
car_shop: when called, says what car part is being fixed.
The end.

```ruby
class Vehicle

  attr_accessor :type, :color, :fuel_level

  def initialize(type = "airplane", color = "red", fuel_level = 100)
    @type = type
    @color = color
    @fuel_level = fuel_level

  end

  def speak
    return "This #{@type} is #{@color} and has a fuel level of #{@fuel_level}."
  end

  def accelerate(speed)
    @fuel_level = @fuel_level + speed
    return "The fuel leve is #{@fuel_level}."
  end

  def decelerate(speed)
    @fuel_level = @fuel_level - speed
    return "The fuel leve is #{@fuel_level}."
  end

  def honk
    return "Beep!"
  end

  def something_broke(car_part)
    return "The #{car_part} is broken."
  end

  def car_shop(car_part)
    return "The #{car_part} is being fixed."
  end

end

truck = Vehicle.new("car", "green", 250)
truck.speak
truck.honk
truck.accelerate(20)
truck.decelerate(30)
truck.something_broke("brake")
truck.car_shop("brake")

```
