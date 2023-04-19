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


