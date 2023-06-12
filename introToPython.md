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