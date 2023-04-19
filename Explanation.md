# Assumptions

1. Every element in the lists has an id (if not there has to be something with roll_no, because everything else such as name and age and extra_info does not have to be unique)
2. Every Element in both the lists have non conflicting data i.e. List does not contain different values for the same key for a given dict with given id (which if exist will be overriden by the later value)
   Example

```python
list_1 = [{'id':1, name:'ravi'}]

list_2 = [{'id':1, name:'siva'}]
```

3. List are unsorted in terms of id (which implies every id element has to have id)
4. Order of Output List does not matter (if required can sort using inbuild sort function)

# Idea

- This can be achieved in two ways
- Using 2 for loops
  - This has O(n^m) time complexity
  - two for loops for two list merge on same id
- Using a dict
  - This has O(m+n) time complexity
  - create a dictionary with id as key and object as value, update dictionary as you get the objects
    going with the second idea
# Sample Test Case

```python
list_1 = [
    {"id": "1", "name": "Shrey", "age": 25},
    {"id": "3", "age": 10, "name": "Hello"},
    {"id": "2", "name": "World", "age": 24},
]

list_2 = [
    {"id": "1", "marks": 100},
    {
        "id": "3",
        "marks": 90,
        "roll_no": 11,
        "extra_info": {
            "hello": "world",
        },
    },
]
list_3 = [
    {
    'id': '1',
    'name': 'Shrey',
    'age': 25,
    'marks': 100
    },
    {
    'id': '3',
    'age': 10,
    'name': 'Hello',
    'marks': 90,
    'roll_no': 11,
    'extra_info': {
        'hello': 'world'
        }
    },
    {
    'id': '2',
    'name': 'World',
    'age': 24
    }
]
```

# How to run

```bash
python -i main.py
> > >  list_3
[{'id': '1', 'name': 'Shrey', 'age': 25, 'marks': 100}, {'id': '3', 'age': 10, 'name': 'Hello', 'marks': 90, 'roll_no': 11, 'extra_info': {'hello': 'world'}}, {'id': '2', 'name': 'World', 'age': 24}]
```
