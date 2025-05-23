Encapsulation is the practice of hiding complexity inside a "black box" so that it's easier to focus on the problem at hand. The simplest example of encapsulation is a function. The caller of a function doesn't need to worry too much about what happens inside, they just need to understand the inputs and outputs.

A good example would be the difference between public and private properties of a class. By default, they are all *public*, meaning that you can access them with the `.` operator:
```py
wall.height = 10
print(wall.height)
# 10
```

*Private* data members are a way to <u>encapsulate</u> logic and data *within a class definition*. For instance, in **Python**, to make a property or method private, you prefix it with with two underscores (`__`):
```py
class Wall:
	def __init__(self, armor, magic_resistance):
		self.__armor = armor
		self.__magic_resistance = magic_resistance
	
	def get_defense(self):
	return self.__armor + self.__magic_resistance

front_wall = Wall(10, 20)

print(front_wall.__armor) # results in an error

print(front_wall.get_defense()) # this works
# 30
```

Python is a bit different since it doesn't *truly* make the property private, it just performs something called [name mangling](https://www.geeksforgeeks.org/name-mangling-in-python/). In the above example, trying to do `print(front_wall.__armor)` gives us an error, but we can easily get around that by doing `print(front_wall._Wall__armor)`

***In Python, since there is no true way to make a property private, anything prefixed with one or two underscores is really just a strong suggestion.***

Other languages, like Go, have true encapsulation.