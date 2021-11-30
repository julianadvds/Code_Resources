## Python_Resources

List
my_list = []
index

Tuple
my_tuple = ()

Dictionary
my_dict = {}
my_dict.append({key1:value1, key2:value2})
in a for loop, to get only the key, use:  for i in my_dict:
.keys()
.values()
.get
.items()

Key Value pairs
for key, value in my_dict.items():
	print(Key, value)

## While statement:
while <condition> :
	<statement>

## For Statement
for item in [item]:
	<statement>

## Creating a Function
def funtion_name():
	block of code

## List Comprehension
new_list = [expression for item in list if conditional]
ex. plt.scatter(x_axis, y_axis, s = [i * 3 for i in y_axis])
https://docs.python.org/3.7/tutorial/datastructures.html#list-comprehensions