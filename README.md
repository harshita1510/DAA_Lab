<div align="center">

# MODY UNIVERSITY OF SCIENCE AND TECHNOLOGY

## School of Engineering and Technology

<br>

<img width="154" height="157" alt="Mody_University_logo" src="https://github.com/user-attachments/assets/11e32514-7869-4f2d-afc9-b45171b58488" />


<br>

# PYTHON PROGRAMMING LAB

### LAB RECORD

<br><br>

**Student Name:** Harshita Garg
**Enrollment Number:** 240042

<br>

**Faculty Name:** Dr. P. K. Bishnoi

<br><br>

**Mody University of Science and Technology**
**School of Engineering and Technology**
Lakshmangarh, Rajasthan

</div>

---

<div style="page-break-after: always;"></div>


# INDEX

<table style="width:100%; border-collapse:collapse;">
  <tr>
    <th style="width:10%;">S. No.</th>
    <th style="width:65%;">Program</th>
    <th style="width:25%;">Link</th>
  </tr>

  <tr>
    <td>1</td>
    <td>Finding Execution Time</td>
    <td><a href="#program-1-finding-execution-time">Program 1</a></td>
  </tr>
  <tr>
    <td>2</td>
    <td>Finding Memory Used</td>
    <td><a href="#program-2-finding-memory-used">Program 2</a></td>
  </tr>
  <tr>
    <td>3</td>
    <td>Creating Graph</td>
    <td><a href="#program-3-creating-graph">Program 3</a></td>
  </tr>
  <tr>
    <td>4</td>
    <td>Multiple Graph</td>
    <td><a href="#program-4-multiple-graph">Program 4</a></td>
  </tr>
   <tr>
    <td>5</td>
    <td>Illustrate Undirected Graph</td>
    <td><a href="#program-5-illustrate-undirected-graph">Program 5</a></td>
  </tr>
   <tr>
    <td>6</td>
    <td>Illustrate Directed Graph</td>
    <td><a href="#program-6-illustrate-directed-graph">Program 6</a></td>
  </tr>
  <tr>
    <td>7</td>
    <td>Illustrate Undirected Weighted Graph</td>
    <td><a href="#program-7-illustrate-undirected-weighted-graph">Program 7</a></td>
  </tr>
  <tr>
    <td>8</td>
    <td>Illustrate Directed Weighted Graph</td>
    <td><a href="#program-8-illustrate-directed-weighted-graph">Program 8</a></td>
  </tr>
  
</table>


---

<div style="page-break-after: always;"></div>

# Program 1: Finding Execution Time

## Aim

To write a Python program to find the time of execution.
## Program

```python
import time

start = time.time()

# Program
for i in range(1000000):
    pass

end = time.time()

print("Execution Time:", end - start, "seconds")
```

## Sample Output

<img width="442" height="173" alt="image" src="https://github.com/user-attachments/assets/7b2ba5f4-c0cc-44b2-9d1b-fe6f34b55b50" />


[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 2: Finding Memory Used

## Aim

To write a Python program to find the memory used.
## Program

```python
import tracemalloc

tracemalloc.start()

# Program
a = [i for i in range(100000)]

current, peak = tracemalloc.get_traced_memory()

print("Current Memory:", current, "bytes")
print("Peak Memory:", peak, "bytes")

tracemalloc.stop()
```

## Sample Output

<img width="325" height="166" alt="image" src="https://github.com/user-attachments/assets/dce33956-e66c-461c-833d-67c2ac1ba4b7" />


[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 3: Creating Graph
## Aim

To write a Python program to create a graph.
## Program

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []


class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2):
        node1.neighbors.append(node2)
        node2.neighbors.append(node1)

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")

            for neighbor in node.neighbors:
                print(neighbor.data, end=" ")

            print()


# Create graph
g = Graph()

# Add nodes
n1 = g.add_node(1)
n2 = g.add_node(2)
n3 = g.add_node(3)
n4 = g.add_node(4)

# Add edges
g.add_edge(n1, n2)
g.add_edge(n1, n3)
g.add_edge(n2, n4)
g.add_edge(n3, n4)

# Display graph
g.print_graph()
```

## Sample Output

<img width="213" height="170" alt="image" src="https://github.com/user-attachments/assets/84144f74-0662-4d56-a3dc-b0310f852066" />


[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 4: Multiple Graph

## Aim

To write a Python program to create multiple graph.
## Program

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []


class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2):
        node1.neighbors.append(node2)
        node2.neighbors.append(node1)

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")
            for neighbor in node.neighbors:
                print(neighbor.data, end=" ")
            print()


# First Graph
g1 = Graph()

n1 = g1.add_node(1)
n2 = g1.add_node(2)
n3 = g1.add_node(3)

g1.add_edge(n1, n2)
g1.add_edge(n2, n3)

# Second Graph
g2 = Graph()

n4 = g2.add_node(4)
n5 = g2.add_node(5)
n6 = g2.add_node(6)

g2.add_edge(n4, n5)
g2.add_edge(n4, n6)

# Third Graph
g3 = Graph()

n7 = g3.add_node(7)
n8 = g3.add_node(8)
n9 = g3.add_node(9)

g3.add_edge(n7, n8)
g3.add_edge(n8, n9)
g3.add_edge(n7, n9)


# Print all graphs
print("First Graph:")
g1.print_graph()

print("\nSecond Graph:")
g2.print_graph()

print("\nThird Graph:")
g3.print_graph()
```

## Sample Output

<img width="364" height="385" alt="image" src="https://github.com/user-attachments/assets/561ff081-88de-43bb-808e-61f77ca1d619" />


[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 5: Illustrate Undirected Graph

## Aim

To write a Python program to illustrate undirected graph.
## Program

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []


class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2):
        # Undirected edge: connection in both directions
        node1.neighbors.append(node2)
        node2.neighbors.append(node1)

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")
            for neighbor in node.neighbors:
                print(neighbor.data, end=" ")
            print()


# Create an undirected graph
g = Graph()

# Add vertices
a = g.add_node("A")
b = g.add_node("B")
c = g.add_node("C")
d = g.add_node("D")

# Add undirected edges
g.add_edge(a, b)
g.add_edge(a, c)
g.add_edge(b, d)
g.add_edge(c, d)

# Display the graph
print("Undirected Graph:")
g.print_graph()
```

## Sample Output

<img width="218" height="196" alt="image" src="https://github.com/user-attachments/assets/5ddec05b-38b3-411b-97e4-1f96bfdab2b1" />


[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 6: Illustrate Directed Graph

## Aim

To write a Python program to illustrate directed graph.
## Program

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []


class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2):
        # Directed edge: node1 -> node2
        node1.neighbors.append(node2)

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")
            for neighbor in node.neighbors:
                print(neighbor.data, end=" ")
            print()


# Create a directed graph
g = Graph()

# Add vertices
a = g.add_node("A")
b = g.add_node("B")
c = g.add_node("C")
d = g.add_node("D")

# Add directed edges
g.add_edge(a, b)
g.add_edge(a, c)
g.add_edge(b, d)
g.add_edge(c, d)

# Display the graph
print("Directed Graph:")
g.print_graph()
```

## Sample Output

<img width="200" height="187" alt="image" src="https://github.com/user-attachments/assets/73495d5b-1ad9-4eaf-9dde-39702ea1bd3c" />


[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 7: Illustrate Undirected Weighted Graph

## Aim

To write a Python program to illustrate undirected weighted graph.
## Program

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []


class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2, weight):
        # Undirected weighted edge
        node1.neighbors.append((node2, weight))
        node2.neighbors.append((node1, weight))

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")
            for neighbor, weight in node.neighbors:
                print(f"({neighbor.data}, weight={weight})", end=" ")
            print()


# Create an undirected weighted graph
g = Graph()

# Add vertices
a = g.add_node("A")
b = g.add_node("B")
c = g.add_node("C")
d = g.add_node("D")

# Add edges with weights
g.add_edge(a, b, 10)
g.add_edge(a, c, 20)
g.add_edge(b, d, 30)
g.add_edge(c, d, 40)

# Display the graph
print("Undirected Weighted Graph:")
g.print_graph()
```

## Sample Output

<img width="332" height="207" alt="image" src="https://github.com/user-attachments/assets/7a719581-81a7-49dc-afdb-db02993b7d48" />


[Back to Index](#index)

---
<div style="page-break-after: always;"></div>

# Program 8: Illustrate Directed Weighted Graph

## Aim

To write a Python program to illustrate directed weighted graph.
## Program

```python
class Node:
    def __init__(self, data):
        self.data = data
        self.neighbors = []


class Graph:
    def __init__(self):
        self.nodes = []

    def add_node(self, data):
        node = Node(data)
        self.nodes.append(node)
        return node

    def add_edge(self, node1, node2, weight):
        # Directed weighted edge
        node1.neighbors.append((node2, weight))

    def print_graph(self):
        for node in self.nodes:
            print(node.data, "->", end=" ")
            for neighbor, weight in node.neighbors:
                print(f"({neighbor.data}, weight={weight})", end=" ")
            print()


# Create a directed weighted graph
g = Graph()

# Add vertices
a = g.add_node("A")
b = g.add_node("B")
c = g.add_node("C")
d = g.add_node("D")

# Add directed edges with weights
g.add_edge(a, b, 10)
g.add_edge(a, c, 20)
g.add_edge(b, d, 30)
g.add_edge(c, d, 40)

# Display the graph
print("Directed Weighted Graph:")
g.print_graph()
```

## Sample Output

<img width="327" height="186" alt="image" src="https://github.com/user-attachments/assets/699d936e-8b94-4572-97c6-2bb519d0d508" />


[Back to Index](#index)

---
