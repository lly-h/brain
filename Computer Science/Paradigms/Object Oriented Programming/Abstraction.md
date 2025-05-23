Abstraction is all about *creating a simple interface for complex behavior*. If focuses on what's exposed (public).

A good example of this would be using the `random` library to generate a random number in Python:

```py
import random

attack_damage = random.randrange(5) # whenever attack_damage is referenced, it will give random value between 0-5
```

## <u>Why is this useful?</u>

Taking the example above, generating random numbers is a *really hard* problem. Thankfully, someone else has already done the heavy lifting for us so we don't have to. Instead of having to solve the problem ourselves or understanding what's happening behind the scenes, we simply just apply what's in the `random` library to problems we want to solve.

## <u>Another way to see it</u>

Take these examples if you're having trouble grasping the concept of abstraction:
- People who create vehicles need to know mechanical engineering, but not everyone who works on vehicles needs to
- Plumbers don't need to know how to weld the pipes or how physics work, they just need to know the layout and how to use their tools
- A barista doesn't need to know how to grow coffee beans, only how to make a good cup

## <u>How can we apply this in our code?</u>

### Python:

```py
from abc import ABC, abstractmethod
from math import pi

class Shape(ABC):
	@abstractmethod
	def area(self):
		pass

	@abstractmethod
	def perimeter(self):
		pass

class Circle(Shape):
	def __init__(self, radius):
		self.radius = radius

	def area(self):
		return pi * self.radius ** 2

	def perimeter(self):
		return 2 * pi * self.radius
```

Let's break down the above example:
1. From the `abc` library, import `ABC` (class) and `abstractmethod` (decorator)
2. Define a class called `Shape` that inherits from `ABC`
3. Create 2 methods with `@abstractmethod` to be used by subclasses - this ties into [[Polymorphism]]!
4. Define a class called `Circle` that inherits from `Shape`
5. Modify the 2 passed methods to make them specific to `Circle`

## <u>What's the difference between this and [[Encapsulation]]?</u>
Great question. Who cares? Kind of. You'll notice they are really similar. What it really boils down to: <u>abstraction</u> emphasizes *exposing the right features* and <u>encapsulation</u> emphasizes *bundling data and methods, and restricting access to inner workings*