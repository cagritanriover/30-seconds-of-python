---
title: find_closest
tags: utility
expertise: intermediate
firstSeen: 2021-06-13T05:00:00-04:00
---

Finds the closest smaller element in `an_array` to `target_value` and returns its position and value. 

- Use numpy.asarray() to convert `an_array` into a numpy array first
- Calculate the `absolute_distances` between each `numpy_array` element and `target_value` 
- Identify the array position (i.e., `index`) of the minimum distance
- Return `index` and the closest `numpy_array`

```py
import numpy as np

def find_closest(an_array, target_value):
    numpy_array = np.asarray(an_array)
	absolute_distances = np.abs(array - target_value)
    index = absolute_distances.argmin()
    return index, numpy_array[index]
```

```py
an_array = [-1.2, -1.0, 0.0, 1.0, 2.3, 2.7, 3.0]
target_value = 0.5

index, value = find_closest(an_array, target_value)
# Result: index = 2 value = 0.0
```