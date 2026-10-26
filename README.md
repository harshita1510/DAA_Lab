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


