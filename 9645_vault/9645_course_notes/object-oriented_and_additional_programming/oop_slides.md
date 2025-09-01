
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
* Pubic
* Modifier


---

## Keywords Lesson 2

* Parent / Superclass
* Child / Subclass
* `super()`
* Inheritance
* Composition
* Aggregation
* Overriding

---
# 'Do Now's Lesson 1

_With your partner, discuss each code snippet. What will be output, and why?_

---

```python
class A:
	def __init__(self, thing):
		A.name = thing
		
class B:
	def __init__(self, thing):
		self.name = thing
		
		
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
	

		
test = Y()
print(f"I like {test.__x}s and I like {test.__y}s!")
```

---