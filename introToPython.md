# Chapter 1 Python Basics

To **add comments** to your Python script, you can use the **# tag**. 

Python is perfectly suited to do basic calculations. It can do addition, subtraction, multiplication and division, and there is also support for more advanced operations such as:
- Exponentiation: **. This operator raises the number to its left to the power of the number to its right. For example 3**4 is 3 to the power of 4 and will give 81.
- Modulo: %. This operator returns the remainder of the division of the number to the left by the number on its right. For example 18 % 7 equals 4 because 7 fits into 18 twice (7 x 2 = 14), leaving you with a remainder of 4 (18 - 14 = 4).
- Remember, **= in Python means assignment**, it doesn't test equality!

**Types**:
- To see the type of our bmi value, simply write type and then bmi inside parentheses: **type(bmi)**;
- **float**, which is python's way of representing a real number, so a number which can have both an integer part and a fractional part: 2.598;
- Python also has a type for **integers**: int, like this example 8;
- A **string** is Python's way to represent text. You can use both double and single quotes to build a string, as you can see from these examples;
-  The **Boolean** is a type that can either be True or False. You can think of it as 'Yes' and 'No' in everyday language. Booleans will be very useful in the future, to perform filtering operations on your data for example.
- o do this, you'll need to explicitly convert the types of your variables so that they are all strings. More specifically, you'll need str(), to convert a value into a string. str(savings), for example, will convert the integer savings to a string.
- Similar functions such as int(), float() and bool() will help you convert Python values into any type.

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Chapter 2 Python Lists

**Lists**:
- a list is a **compound data type** so you can group values together;
- name of the collection of values;
- contain any type;
- content differnt types;
- contain lists as well;
- e.g.[1.23, 5.65, 8.99];
- fam = [["liz", 1.86], 
    ["mom", 1.65],
    ["dad", 1.95]]
- type(fam) = list !!

# Subsetting Lists

Subsetting Lists:
- zero-indexing;
- slicing [start:end](inclusive; exclusive)
-fam =  ['liz', 1.73, 'emma', 1.68, 'mom', 1.71, 'dad', 1.89]; fam[0]
- fam[-1] => the last element
- fam[:4] => inclusive
- Selecting single values from a list is just one part of the story. It's also possible to slice your list, which means selecting multiple elements from your list. Use the following syntax:
-my_list[start:end]    !The start index will be included, while the end index is not.
- However, it's also possible not to specify these indexes. If you don't specify the begin index, Python figures out that you want to start your slice at the beginning of your list. If you don't specify the end index, the slice will go all the way to the last element of your list. To experiment with this, try the following commands in the IPython Shell;
- fam_ext = fam + ["me", 1.79]del(fam[2])fam['lisa', 1.74, 1.68, 'mom', 1.71, 'dad', 1.86]
- Replacing list elements is pretty easy. Simply subset the list and assign new values to the subset. You can select single elements or you can change entire list slices at once.
- If you can change elements in a list, you sure want to be able to add elements to it, right? You can use the + operator:
- The ; sign is used to place commands on the same line. The following two code chunks are equivalent:
- Same line: command1; command2
- If you want to prevent changes in areas_copy from also taking effect in areas, you'll have to do a more explicit copy of the areas list. You can do this with list() or by using [:].
- **Create list areas**
    - areas = [11.25, 18.0, 20.0, 10.75, 9.50]
-  **Create areas_copy**
    - areas_copy = list(areas[:])
- **Change areas_copy**
    - areas_copy[0] = 5.0
- **Print areas**
    print(areas)

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Chapter 3 Functions and packages

**Functions**:
- Nothing new!
- type()
- Piece of reusable code
- Solves particular task
- Call function instead of writing code yourself
- max()
- round(number, percision ~ ndigits)
- help(round) => get description
- In IPython specifically, you can also use ? before the function name.
- print()
- str(), int(), float(), bool()
- The general recipe for **calling functions** and saving the result to a variable is thus: output = function_name(input)
- len() => get the length of the list
- pow(x, y, z): x	A number, the base; y	A number, the exponent; z	Optional. A number, the modulus;
- You'll see that **sorted()** takes three arguments: iterable, key, and reverse
    - iterable	Required. The sequence to sort, list, dictionary, tuple etc.
    - key	Optional. A Function to execute to decide the order. Default is None
    - reverse	Optional. A Boolean. False will sort ascending, True will sort descending. Default is False.

**Methods**:
- string, float, list **are objects**
- **Methods** - functions that belong to python objects
- fam['liz', 1.73, 'emma', 1.68, 'mom', 1.71, 'dad', 1.89]
    - fam.index("mom") # "Call method index() on fam" => 4
    - fam.count(1.73) - how many time 1.73 occurs in the list => 1
    - sister 'liz' 
    - sister.capitalize()'Liz'
    - sister.replace("z", "sa") =>'lisa'
    - fam.append("me") => fam['liz', 1.73, 'emma', 1.68, 'mom', 1.71, 'dad', 1.89, 'me']
    - fam.append(1.79) => fam['liz', 1.73, 'emma', 1.68, 'mom', 1.71, 'dad', 1.89, 'me', 1.79]
-  upper() method does not change the object(str) it is called on. 
- Most **list methods will change the list** they're called on. Examples are:
    - append(), that adds an element to the list it is called on,
    - remove(), that removes the first element of a list that matches the input, and
    - reverse(), that reverses the order of the elements in the list it is called on.

**Packages**:
- Directory of Python Scripts
- Each script = module
- Specify functions, methods,types
- Thousands of packages available 
    - NumPy
    - Matplotlib
    - scikit-learn

**Install packagehttp**:
- //pip.readthedocs.org/en/stable/installing/
- Download get-pip.py
- Terminal:python3 get-pip.py
- pip3 install numpy
- import numpy as np; np.array([1, 2, 3])
- from numpy import array; array([1, 2, 3])
- pi => math.pi

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------

# Chapter 4 NumPy

**NumPy**:
- Numeric Python 
- Alternative to Python List: NumPy Array
- Calculations over entire arrays
- Easy and Fast
- InstallationIn the terminal: pip3 install numpy
- bmi => array([21.85171573, 20.97505669, 21.75028214, 24.7473475 , 21.44127836])
    - bmi[1] 20.975
    - bmi > 23 => array([False, False, False,  True, False])
    - bmi[bmi > 23] => array([24.7473475])
- First of all, numpy arrays cannot contain elements with different types. If you try to build such a list, some of the elements' types are changed to end up with a homogeneous list. This is known as type coercion.

**2D NumPy Arrays**:
- np_2d = np.array([[1.73, 1.68, 1.71, 1.89, 1.79],[65.4, 59.2, 63.6, 88.4, 68.7]])
    - np_2darray([[ 1.73,  1.68,  1.71,  1.89,  1.79],       [65.4 , 59.2 , 63.6 , 88.4 , 68.7 ]])
    - np_2d.shape => (2, 5) # 2 rows, 5 columns
    - .shape is atribute not a method ! it doesn't have ()
    - np_2d[0][2] => 1.71

**Basic Statistics**:
- np.mean()
- np.median()
- np.std()
- np.corrcoef()
- sum()
- sort()

**Generate data**:
- Generate data
    - Arguments for np.random.normal():
        - distribution mean
        - distribution standard deviation
        - number of samples
        - height = np.round(np.random.normal(1.75, 0.20, 5000), 2) 
        - weight = np.round(np.random.normal(60.32, 15, 5000), 2) 
        - np_city = np.column_stack((height, weight))

