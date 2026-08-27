# ECE-2112-PA-1

**Made by: Mike Angelo P. Atienza | Section: 2ECE-B**

The content of this repository contains the Programming Assignment 1 for our course "Advanced Computer Programming and Algorithms" this S.Y. 2026-2027. This project contains three python programming problems 

# 1. Word Rotation Problem
Create a function named rotate word() that accepts a non-empty string. Move the first character of the string to the end while keeping all remaining characters in their original order. Preserve the
capitalization of every character.

**Functions and methods that were used here:**
* **Function Definition (`def` / `return`):** Defines the modular function `rotate_word(text)` that accepts a string and returns the rotated result.
* **String Indexing (`text[0]`):** Isolates the first character of the string at index 0.
* **String Slicing (`text[1:]`):** Extracts all characters starting from index 1 through the end of the string.
* **String Concatenation (`+`):** Glues the sliced substring (`text[1:]`) and the first character (`text[0]`) back together in reverse order.

def rotate_word(text):    
    return text[1:] + text[0]
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
* **Function Definition (`def` / `return`):** Defines `make_username(first_name, last_name)` to accept two separate name inputs and return a formatted username string.
* **Case Conversion (`.lower()`):** Converts all uppercase characters in both `first_name` and `last_name` to lowercase.
* **Character Replacement (`.replace(" ", "")`):** Identifies and strips all space characters from multi-word names (such as "Ana Maria" or "De Leon").
* **String Concatenation (`+`):** Combines the cleaned first name, a literal period (`"."`), and the cleaned last name into a unified username string.

def make_username(first_name, last_name):
    comprs_first = first_name.lower().replace(" ","") 
    comprs_last = last_name.lower().replace(" ","")
    user_builder = comprs_first + "." + comprs_last
    return user_builder 
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
* **Function Definition (`def` / `return`):** Defines `swap_bookends(items)` to accept a list of elements and return a newly constructed list.
* **Extended Sequence Unpacking (`first, *middle, last = items`):** 
  * Captures the very first list element into `first`.
  * Gathers all center elements into a sub-list named `middle` using the asterisk (`*`) iterable unpacking operator.
  * Captures the final list element into `last`.
* **List Construction & Unpacking (`[last, *middle, first]`):** Builds a brand new list placing `last` at index 0, expanding the `middle` elements in place, and appending `first` at the end without mutating the original list.

def swap_bookends(items):
    first, *middle, last = items
    return [last, *middle, first]
    print(swap_bookends([1, 2, 3, 4, 5, 6]))
    print(swap_bookends(["red", "green", "blue"]))
    print(swap_bookends([8, 3])) 
    print(swap_bookends(["mlbb", "cod", "pubg"]))
    
