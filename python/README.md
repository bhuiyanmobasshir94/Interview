1. [41 Python Interview Questions [+ Answer Guide]](https://www.springboard.com/blog/data-science/python-interview-questions/)

```
## Problemset 1

watches = [
    {"id": "1", "label": "GC0003", "color": "COL_RED"},
    {"id": "2", "label": "GC0004", "color": "COL_BLACK"},
    {"id": "3", "label": "GC0006", "color": "COL_RED"},
]
watch_colors = [
    {"id": "COL_BLACK", "label": "Black"},
    {"id": "COL_RED", "label": "Red"},
]

# Output
# GC0003 Red
# GC0004 Black
# GC0006 Red

## Problemset 1 solution

for watch in watches:
    for color in watch_colors:
        if watch["color"] == color["id"]:
            print(watch["label"], color["label"])

## Problemset 1 end

## Problemset 2

student_grades = {}
grades = [
    ("elliot", 91),
    ("neelam", 98),
    ("bianca", 81),
    ("elliot", 88),
]

## Output
# {'elliot': [91, 88], 'neelam': [98], 'bianca': [81]}

## Problemset 2 solution

from collections import defaultdict

student_grades = defaultdict(list)
for name, grade in grades:
    student_grades[name].append(grade)

print(dict(student_grades))

## Problemset 2 end

## Problemset 3

# Sum upto 1 million

## Bad approach
sum([i * i for i in range(1, 1001)])

## Good approach
sum((i * i for i in range(1, 1001)))

## Problemset 3 end

## Problemset 4

# Sort this array based on age

animals = [
    {"type": "penguin", "name": "Stephanie", "age": 8},
    {"type": "elephant", "name": "Devon", "age": 3},
    {"type": "puma", "name": "Moe", "age": 5},
]

## Output

# [
#     {'type': 'elephant', 'name': 'Devon', 'age': 3},
#     {'type': 'puma', 'name': 'Moe', 'age': 5},
#     {'type': 'penguin', 'name': 'Stephanie, 'age': 8},
# ]

## Problemset 4 solution

sorted(animals, key=lambda animal: animal["age"])

## Problemset 4 end

## Problemset 5

numbers = [4, 2, 1, 6, 9, 7]

# make a list squares for this array of numbers


def square(x):
    return x * x


## Output
# [16, 4, 1, 36, 81, 49]

## Good approach
list(map(square, numbers))

## Best appraoch
[square(x) for x in numbers]

# make a list filtering out odds for this array of numbers


def is_odd(x):
    return bool(x % 2)


## Output
# [1, 9, 7]

## Good approach
list(filter(is_odd, numbers))

## Best appraoch
[x for x in numbers if is_odd(x)]

## Problemset 5 end

## Problemset 6

courses = ["Data Science", "Machine Learning", "Deep Learning", "Computer Vision"]

def find_index(to_search, keyword):
  for index, value in enumerate(to_search):
    if keyword == value:
      return index
  return -1

print(find_index(courses, "Deep Learning"))
print(find_index(courses, "Natural Language Processing"))

## Problemset 6 end

## Problemset 7

def add_employee(emp, emp_list = []):
    emp_list.append(emp)
    print(emp_list)
    
add_employee('Jane')
add_employee('Corey')

## Problemset 7 end

## Problemset 8

GROUPS = {
    1: {"name": "Super Admin"},
    2: {"name": "Admin"},
    3: {"name": "Archivist"},
    4: {"name": "Reviewer"},
    5: {"name": "Authorizer"},
}

ACCESS_PERMISSION_BY_MODULE = {
    "GROUP": {"read": [GROUPS[2]], "read_write": [GROUPS[1]],},
    "USER": {"read": [GROUPS[2]], "read_write": [GROUPS[1]],},
    "DASHBOARD": {"read": [GROUPS[1], GROUPS[2]], "read_write": [],},
    "ARCHIVE": {
        "read": [],
        "read_write": [GROUPS[1], GROUPS[2], GROUPS[3], GROUPS[4], GROUPS[5]],
    },
}

## Output
[{'name': 'Admin'}, {'name': 'Super Admin'}]

## Solution
groups = [
    value
    for value_list in ACCESS_PERMISSION_BY_MODULE["GROUP"].values()
    for value in value_list
]

## Problemset 8 end

## Problemset 9 

i = 0
while True:
    if i == 5:
        continue
    if i == 10: 
        break
    print(i)
    i += 1

why this runs infinitely

## Problemset 9 end

## Probleset 10

Input: nums = [1,2,3,1]
Output: true

def containsDuplicate(nums: List[int]) -> bool:
    from collections import Counter
    for item, count in Counter(nums).items():
        if count > 1:
            return True
    return False
    
## Probleset 10 end
```

