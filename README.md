# python-CDLLwS

Python implementation of a *Circular Doubly Linked List with Sentinel*.

---

The `CDDLwS` module contains the following classes.

##<a id="Nodeclass"></a>`Node` class##
This class generates the items that can be appended to a `CDLLwS` instance. You can extend this class for adding extra properties. The minimum definition is as follows:

###`__init__(self, data)`###

 - **`data`**: The value to associate to this instance.

###`data`###

The value to be stored within that node. It can be anything.

###`next`###

Pointer to the following `Node` instance in the `CDLLwS` object.

###`prev`###

Pointer to the previous `Node` instance in the `CDLLwS` object.



##`CDLLwS` class##
The *Doubly Linked List with Sentinel* class itself.
`CDLLwS` objects must be composed of [`Node`](#Nodeclass) instances.
The defined properties/methods are the followings:

###`__init__(self, nodeClass)`###

 - **`nodeClass`**: The class used for filling this instance.

###`__len__(self)`###
	
Returns the length of the list (omitting the sentinel object).
```python
l = CDDlwS(Node)
length = len(l)
```

###`__iter__(self)`###
	
Transforms this object into an iterator. For example you can do:
```python
l = CDDlwS(Node)
for x in l:
	pass
```

###`__getitem__(self)`###

Allows you to positionally retrieve a node, e.g.:
```python
l = CDDlwS(Node)
item = l[27]
```

###`__str__(self)`###

Lets you print the `CDLLwS` instance like a normal `list`, e.g.:
```python
l = CDDlwS(Node)
print l
```

###`insert(self, i, x)`###

Lets you insert a `Node` object (`x`) to any position `i` (*&lt;int&gt;*) of the `CDLLwS` instance like a normal `list`, e.g.:
```python
l = CDDlwS(Node)
l.insert(27, Node(...))
```
	
###`append(self, x)`###

Lets you append a `Node` object (`x`) to the `CDLLwS` instance like a normal `list`, e.g.:
```python
l = CDDlwS(Node)
l.append(Node(...))
```

###`pop(self, i=None)`###

Lets you remove an element from the `CDLLwS` instance and return it like a normal `list`. If parameter `i` (*&lt;int&gt;*) is equal to `None` the last item is removed otherwise `i` must be and integer number indicating the position of the item to remove. e.g.:

```python
l = CDDlwS(Node)
x = l.pop(i=27)
```
	
###`find(self, s, propName)`###

Lets you retrieve the first occurence of a `Node` whose property `propName` (*&lt;int&gt;*) is equal to `s`. If no element matches the criterion, `None` is returned instead, e.g.:
```python
l = CDDlwS(Node)
x = l.find("pippo", "firstName")
```

---

##Changelog

###1.0.0

First version