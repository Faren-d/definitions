# Placeholder

Placeholder in Python is like a temporary spot or marker in your code where you plan to put some specific information later. It's a way to say "I'll fill in this part with actual data when I need to."

In other words, Placeholders are part of a broader concept called string formatting. They allow for dynamic string creation and manipulation.

## 
- What does a placeholder look like?
In Python, placeholders are often written with curly braces {} inside a string.

- When do we use placeholders?
We use them when we want to create a string that will have some parts filled in later with specific values.

```bash
name = "Bob"
age = 30
message = f"My name is {name} and I am {age} years old."
print(message)
```

# Objects

An object is like a container that holds data and functions related to that data. Almost everything in Python is an object.
Example:

```bash
my_car = "Toyota"  # my_car is a string object
my_numbers = [1, 2, 3]  # my_numbers is a list object
```

# Arguments
Arguments are pieces of information that you pass into a function when you call it. They're like inputs for the function to work with.
Example:
```bash
def greet(name, time_of_day):
    print(f"Good {time_of_day}, {name}!")

greet("Alice", "morning")  # Outputs: Good morning, Alice!
```
# Parameteres

- Parameters are variables listed in the definition of a function or method.

- They act as placeholders for the values that will be passed into the function when it's called.

- Parameters have a scope limited to the function they're defined in.

# Attributes

- Attributes are pieces of information attached to an object. They're like characteristics or properties of the object.

- Attributes are variables that belong to an object.

- They store data that is associated with that object.

- Attributes have a lifespan as long as the object exists and can be accessed from various methods within the class.


```bash
class Car:
    def __init__(self, make, model, year):
        self.make = make    # attribute
        self.model = model  # attribute
        self.year = year    # attribute
        self.mileage = 0    # attribute (not from a parameter)
        self.running = False  # attribute (not from a parameter)

    def start_engine(self):
        self.running = True
        print(f"The {self.year} {self.make} {self.model}'s engine is now running.")

    def drive(self, distance):
        if self.running:
            self.mileage += distance
            print(f"Drove {distance} miles. Total mileage is now {self.mileage}.")
        else:
            print("You need to start the engine first!")

# Creating an instance (object) of the Car class
my_car = Car("Toyota", "Corolla", 2020)

# Using the object
my_car.start_engine()
my_car.drive(50)
```


