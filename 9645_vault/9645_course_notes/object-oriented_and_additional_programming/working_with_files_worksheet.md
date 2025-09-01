
*NOTE: Code Emitter does not support I/O Operations (and these tend to cause Obsidian to crash) so for this worksheet, please test your code outside of Obsidian and paste in your answers once complete.*

---

# Serial Files

---

A text file is an example of a **serial file**.

This is because:

* data can only be appended (unless the entire file is rewritten)
* the file can only be read line-by-line, in sequence.

---

## TASK 1

Explain three different modes for opening text files in Python.

Show a sensible example of each mode in practice, and demonstrate some of the methods associated with that mode.

---

**A:**

---

## TASK 2

```python

file = open("example.txt", "w")
file.write("1\n2\n3")
file.close()

with open("example.txt") as file:
	while file:
		print(file.read())
```

Explain the output of the above program, making reference to how the `.read()` method is used and why it returns a different result each time it is called inside the `while` loop.

---

**A:**

---

## TASK 3

The file is opened and closed twice in the above program, but each time using different syntax.

State the name of the technique that is being used the second time the file is opened, and explain why this is the preferred way of opening files in Python.

---

**A:**

---

# Random Access File

A random access file stores data at a certain starting byte, and can directly read data found at that byte. All bytes in the file can also be read in sequence.

To work with random access files in Python, files must be opened in one of the binary modes:

```python
"rb" # read bytes
"wb" # write bytes
"rwb+" # ?
"rb+" # ?
```

## TASK 4

