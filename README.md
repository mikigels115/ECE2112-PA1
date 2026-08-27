# ECE-2112-PA-1

**Made by: Mike Angelo P. Atienza | Section: 2ECE-B**

The content of this repository contains the Programming Assignment 1 for our course "Advanced Computer Programming and Algorithms" this S.Y. 2026-2027. This project contains three python programming problems 

# 1. Word Rotation Problem
Create a function named rotate word() that accepts a non-empty string. Move the first character of the string to the end while keeping all remaining characters in their original order. Preserve the
capitalization of every character.

**Functions and methods that were used here:**
* **(`def` / `return`):** It defines the function rotate_word(text) to input a string variable inside the function and return the rotated word string to the output.
* **(`text[0]`):** It gets the very first character of the string at index 0.
* **(`text[1:]`):** It slices all the remaining characters starting from index 1 up until the end of the string.
* **String Concatenation (`+`):** It combines the sliced characters and the first character together to move the first letter to the end.

```python
def rotate_word(text):    
    return text[1:] + text[0]
```
    
    print(rotate_word("python"))
    print(rotate_word("logic"))
    print(rotate_word("Code"))
    print(rotate_word("A"))
    print(rotate_word("eMik"))

# 2. Username Builder Problem
Create a function named make username() that accepts two strings: first name and last name. The
function must:
1. convert all letters to lowercase;
2. remove all spaces from the first name;
3. remove all spaces from the last name; and
4. join the processed first and last names using one period (.).

**Functions and methods that were used here:**
* **(`def` / `return`):** It defines the function `make_username(first_name, last_name)` to input two separate name variables inside the function and return a username string to the output.
* **(`.lower()`):** It converts from all uppercase to lowercase letters in both the `first_name` and `last_name`.
* **(`.replace(" ", "")`):** It removes all space characters in the output (ex. "Ana Maria" or "De Leon").
* **(`+`):** It combines the cleaned first name, a literal period (`"."`), and the cleaned last name into a unified username string.

```python
def make_username(first_name, last_name):
    comprs_first = first_name.lower().replace(" ", "") 
    comprs_last = last_name.lower().replace(" ", "")
    user_builder = comprs_first + "." + comprs_last
    return user_builder
```
    
    print(make_username("Ada", "Lovelace"))
    print(make_username("Alan", "Turing"))
    print(make_username("Ana Maria", "De Leon"))
    print(make_username("Dhabi", "Gonzaga"))

# 3. Bookend Swap Problem
Create a function named swap bookends() that accepts a list containing at least two elements. Unpack
the list into three variables:
• first – the first element;
• middle – a list containing everything between the first and last elements; and
• last – the last element.
Using these variables, return a new list in which the first and last elements have exchanged positions.
The elements in middle must remain in their original order. Do not modify the input list.

**Functions and methods that were used here:**
* **(`def` / `return`):** It defines the function swap_bookends(items) to input a list inside the function and return a new swapped list to the output.
* **(`first, *middle, last = items`):** It unpacks the list so the first element goes to first, the last element goes to last, and all the middle elements go into middle using the asterisk (*).
* **(`[last, *middle, first]`):** It combines and creates the new list with last in front, the middle elements in the center, and first at the very end.

```python
def swap_bookends(items):
    first, *middle, last = items
    return [last, *middle, first]
```
    
    print(swap_bookends([1, 2, 3, 4, 5, 6]))
    print(swap_bookends(["red", "green", "blue"]))
    print(swap_bookends([8, 3])) 
    print(swap_bookends(["mlbb", "cod", "pubg"]))


# README File Version History

August 26, 2026: Initial README file output uploaded.
    
