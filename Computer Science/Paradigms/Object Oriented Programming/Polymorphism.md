While [[Inheritance]] is the most *unique* trait of object-oriented languages, polymorphism is probably the most powerful. <u>It is also *not* particularly unique to class-based languages.</u> Polymorphism is the ability of a variable, function, or object to take on multiple forms. Polymorphism literally means *many forms*:
- "poly" = "many"
- "morph" = "form"

For a good example of this, go check out the [[Abstraction]] note where we create a class called `Shape` and a class called `Circle` - we define two methods in the `Shape` class to be used by any subclasses. This is achieved by ensuring the subclass methods have the same signatures as the superclass methods.

## What is a function signature?

A function signature (or method signature) includes the name, inputs, and outputs of a function or method. For example, `hit_by_fire` in the `Human` and `Archer` classes have identical signatures:
```py
class Human:
	def hit_by_fire(self):
		self.health -= 5
		return self.health

class Archer:
	def hit_by_fire(self):
		self.health -= 10
		return self.health
```
These classes would <u>**NOT**</u> have identical method signatures if they were written like this instead:
```py
class Human:
	def hit_by_fire(self):
		self.health -= 5
		return self.health

class Archer:
	def hit_by_fire(self, dmg):
		self.health -= dmg
		return self.health
```
The reason they are not identical is because in the `Archer` class, the `hit_by_fire` method, unlike the `Human` class, asks for another argument, `dmg`.

The difference between the above examples, and the example found in [[Abstraction]], is that using `abstractmethod` from the `abc` library says the subclass <u>**MUST**</u> use any methods decorated with `@abstractmethod` from the superclass, or else you get a `TypeError`. This is where function signatures become really important!