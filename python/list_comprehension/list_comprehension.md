
# 2-D List 

```python
matrix = [[1, 2, 3], [4, 5], [6, 7, 8, 9]] 
Expected Output: flatten_matrix = [1, 2, 3, 4, 5, 6, 7, 8, 9]  

flatten_matrix = [] 
  
for sublist in matrix: 
    for val in sublist: 
        flatten_matrix.append(val) 

flatten_matrix = [val for sublist in matrix for val in sublist]
```
같은 결과 보임 

```python
flatten_matrix = [val
                  for sublist in matrix
                  for val in sublist]
```
로 이해하면 쉬움

```python
# 2-D List of planets 
planets = [['Mercury', 'Venus', 'Earth'], ['Mars', 'Jupiter', 'Saturn'], ['Uranus', 'Neptune', 'Pluto']] 
  
# Nested List comprehension with an if condition 
flatten_planets = [planet for sublist in planets for planet in sublist if len (planet) < 6] 
          
print(flatten_planets) 
```

```python
flatten_planets = [planet 
                   for sublist in planets 
                   for planet in sublist 
                   if len(planet) < 6] 
```

헷갈릴땐 항상 줄을 바꿔서 보자!

if 를 앞에 붙이면 else도 해야하지만 뒤에 넣으면 else 안해도 된다!

reference : https://www.geeksforgeeks.org/nested-list-comprehensions-in-python/
