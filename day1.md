Day 1: Name Cleaning Task

# Task
Write a function to clean up a list of names by:
- Stripping extra spaces
- Lowercasing all names
- Removing digits and special characters

---

# python Code

def clean_name(names):
    clean=[]
    for i in names:
        name=i.strip().lower()
        for p in "!@#$%^&*()_+=-1234567890":
            name=name.replace(p,'')
        clean.append(name)
    return clean

name = ["  Alice  ", "BOB", "   charlie", "dave!", "Eve123"]
print(clean_name(name))

# output

['alice', 'bob', 'charlie', 'dave', 'eve']

---

# Explanation of code

This function loops through each name:
- first it strips unwanted spaces and convert to lowercase
- then it checks it checks for unwanted characters and removes them one by one
- clean names are collected in a new list
- final result is returned and printed

# What I Learned

- How to remove extra characters like spaces and symbols from names
- How to use .strip(), .lower(), and .replace() in a loop
- How to clean a list of names and return the result
