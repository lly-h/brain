Inheritance is all about allowing child classes to inherit behavior and data from their parent classes. This is one of the most crucial topics in *object oriented programming* but is usually only found in class-based languages like Python, Java, and Ruby.

## <u>Example 1</u> <sub><sup><sub><sup>in Python</sub></sup></sub></sup>

```py
class Human: # this is the parent class
	def __init__(self, name, health, stamina):
		self.name = name
		self.health = health
		self.stamina = stamina

class Baby(Human): # this is the child class
	def __init__(self, name, health, stamina, fragile):
		super().__init__(name, health, stamina) # gets attributes from parent
		self.fragile = fragile
```