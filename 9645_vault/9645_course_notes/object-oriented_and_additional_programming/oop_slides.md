
---
# Your Spec


![height:600px](media/oop_spec_ss_01.png)

---

![height:700px](media/oop_spec_ss_02.png)

---

![height:700px](media/oop_spec_ss_03.png)

---

# Activities

1) Litmus Test - OOP Puzzles
2) Introduction to OOP md worksheet
3) OOP Continued md worksheet
4) Objectifying Your Y10 PPP task
5) Python Challenges XXIVC: My Object Oriented Restaurant
6) *Other Python Challenges tasks as needed*
7) SpaceInvaders Project

---
## Keywords Lesson 1


* Object
* Class
* Instance
* Property / Attribute
* Method
* `self`
* Constructor / `__init__()`
* Getter
* Setter
* Private `__`
* Protected `_`
* Public
* Modifier


---

## Keywords Lesson 2

* Parent / Superclass
* Child / Subclass
* `super()`
* Inheritance
* Association
* Composition
* Aggregation
* Overriding
* Encapsulation

---
# 'Do Now' Code Puzzles Lesson 1

_With your partner, discuss each code snippet. What will be output, and why?_

---

```python
class A:
	def __init__(self, thing):
		A.name = thing
		
class B:
	def __init__(self, thing):
		self.name = thing

if __name__ == "__main__":	
	var1 = A("Tim")
	var2 = A("Tom")
	var3 = B("Tin")
	var4 = B("Ton")
	
	print("var2 is called", var2.name)
	print("var1 is called", var1.name)
	print("var4 is called", var4.name)
	print("var3 is called", var3.name)

```

---


```python

class X:
	def __init__(self):
		self.x = "fish"
		self.y = "cat"
	
	def test(self):
		return self.x == self.y

if __name__ == "__main__":		
	thing = X()
	if thing.test:
		print("Fishcat")
```

---


```python

class Y:
	def __init__(self):
		self.__x = "horsey"
		self.__y = "frogs"
	
if __name__ == "__main__":	
	test = Y()
	print(f"I like {test.__x}s and I like {test.__y}s!")
```

---

# A Class, Constructor, and Instantiation Parameters

`__init__()` - the constructor method, executed when the object is first instantiated.

Commonly used to initialise object properties - according to data passed in via instance parameters, or to some default values.

```python

# note, code block missing full context - not intended to be executed

class Animal:
	def __init__(self, name, species, age, owner_name):
		self.name = name
		self.species = species
		self.age = age
		self.owner_name = owner_name
		self.alive = True
```

---

# Instantiation

```python

# note, code block missing full context - not intended to be executed

fred = Animal("Fred", "Gecko", 3, "Mr. Yates")
billy = Animal("Billy", "Goat", 6, "Mr. Yates")
```

Both `fred` and `billy` now have the data type of: `Animal`

---

# Private, Public, Protected Modifiers

* Private properties / methods - can only be accessed from within the same class.
* Protected properties / methods - within that class and any derivatives (children).
* Public properties / methods - can be accessed freely from outside the class.

```python

# note, code block missing full context - not intended to be executed

class MedicalRecord:
    def __init__(self, animal, diagnosis, treatment_plan, vet_notes):
        self.animal = animal  
        self._diagnosis = diagnosis
        self._treatment_plan = treatment_plan
        self.__vet_notes = vet_notes  # Notes from the veterinarian 


# Example Usage
if __name__ == "__main__":
    
    animal = Animal("Buddy", "Dog", 5, "Alice Johnson")
    record = MedicalRecord(animal, "Arthritis", "Pain management and light exercise", "Monitor progress weekly.")
    print(f"Animal: {record.animal.name}")
    # Access protected attribute (not recommended but possible)
    print(f"Protected Diagnosis: {record._diagnosis}")
    
```

---

# Getters and Setters

To enforce proper **encapsulation**, method interfaces should be used.

**Getters** allow outside access to internal private data.

**Setters** allow internal private properties to be set from outside scopes.

```python

# note, code block missing full context - not intended to be executed

class Animal:
	## ....
	def add_vet_notes(self, new_notes):
			""" Public method to update vet notes via private method. """
			self.__update_vet_notes(new_notes)
			

	def get_vet_notes(self):
		""" Retrieves the private vet notes (for authorised access). """
		return self.__vet_notes
```
    
---

# Technology Current Affairs Task

Recently there has been [news](https://www.theguardian.com/us-news/2025/sep/02/trump-immigration-ice-israeli-spyware) about the US government purchasing a spyware program named "Graphite" from the company Paragon.

Consider the hypothetical OOP design of *Graphite*.

What...

* Objects
* Properties
* Methods

... do you think this programming code for this software contains?

---

# 'Do Now' Code Puzzles Lesson 2

_With your partner, discuss each code snippet. What will be output, and why?_

```python
class A:
	def __init__(self):
		self.x = False
		self.y = True
		
class B:
	def __init__(self):
		self.x = A()
		self.y = A()
		
if __name__ == "__main__":
	a = A()
	b = B()
	
	print(a.x == b.x.y)
	print(type(a.x))
	print(type(b.x.x))
		
```

---

```python
class Y:
	def __init__(self):
		self.a = 9
		self.b = 2
		
class X(Y):
	def __init__(self):
		self.a = 1
		super().__init__()
		self.a += self.b
		
	def get(self):
		return self.a
		
if __name__ == "__main__":		
	x = X().get()
	print(x)
		
```

---

# Inheritance

```python

# note, code block missing full context - not intended to be executed

class Animal:
	pass
	
class Dog(Animal):
	pass
```

If an object *inherits* some of its properties and behaviour from another object, then the two objects have a **"B is a type of A"** relationship.

* *A dog is a type of animal*

What other examples can you think of?

---

# `super()`

The built-in function `super()` allows an object to make reference to its parent. You will likely use this inside your child class' constructor - to make sure the parent object constructor is executed at the same time.

```python

# note, code block missing full context - not intended to be executed

class Animal:
	def __init__(self, age, weight):
		self.__age = age
		self.__weight = weight
	
	
class Dog(Animal):
	def __init__(self, age, weight, obedience):
		super().__init__(age, weight)
		self.__obedience = obedience
```

---

# Overriding

The process of **overriding** is where a child class modifies or extends the existing behaviour of a parent class.

```python

# note, code block missing full context - not intended to be executed

class Animal:
	# ....
	def hear_whistle(self):
		self.__speed = 10
		
class Dog(Animal):
	# ....
	def hear_whistle(self, owner):
		super().hear_whistle()
		self._move_towards(owner.x, owner.y)
```


# CRD Example

Discuss the data design decisions that have been made in this system.

![height:600px](https://cdn-proxy.slickplan.com/wp-content/uploads/2025/08/banking-uml-class-diagram.jpg)

---

# CRD Syntax

* **+** denotes a public attribute
* **-** denotes a private attribute
* \**#** denotes a public method
* -▷ a hollow triangular arrowhead denotes **inheritance**
* --- a line with no arrowhead between classes denotes **association**
* -◇ a hollow a diamond arrowhead denotes **aggregation**
* -◆ an opaque diamond arrowhead denotes **composition**
* The x...y syntax denotes **cardinality** - how many instances of some object associate with how many instances of another object.

