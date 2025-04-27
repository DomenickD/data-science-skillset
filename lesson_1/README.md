# Lesson 1: Python Basics

### Objectives
- Learn Python syntax, variables, data types  
- Write basic control flow (if/else, loops)  
- Implement a simple hardcoded chatbot input loop  

### Prerequisites
- No prior programming experience needed  
- Python 3.8+ installed  

### Topics Covered
- Variables & types (`int`, `float`, `str`, `bool`)  
- `print()` and `input()` functions  
- `if`/`else` statements  
- `for` and `while` loops  
- Basic error handling with `try`/`except`  

### In-Class Exercise: Hardcoded Chatbot
```python
# chatbot.py
while True:
    user_input = input("You: ")
    if user_input.lower() in ['exit', 'quit']:
        print("Bot: Goodbye!")
        break
    elif 'hello' in user_input.lower():
        print("Bot: Hi there!")
    else:
        print("Bot: I'm still learning...")
```

### Homework

- Extend the chatbot to recognize at least three different keywords

- Add error handling if the input is empty

- Commit your code and push to GitHub