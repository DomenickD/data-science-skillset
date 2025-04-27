# Lesson 2: Python Intermediate

### Objectives

- Understand and write functions

- Work with lists, dictionaries, and sets

- Apply error handling and input validation

- Enhance chatbot logic with reusable functions

### Prerequisites

- Completion of Lesson 1

### Topics Covered

- Defining and calling functions

- Function parameters and return values

- Data structures: `list`, `dict`, `set`, `tuple`

- List comprehensions and dictionary comprehensions

- Raise and catch exceptions

### In-Class Exercise: Chatbot Functions

```python 
# chatbot_v2.py
def respond(message: str) -> str:
    msg = message.lower()
    if 'help' in msg:
        return "Bot: Sure, how can I assist?"
    elif 'time' in msg:
        return "Bot: I can't tell time yet."
    return "Bot: Sorry, I didn't get that."

while True:
    user_input = input("You: ")
    if user_input.lower() in ['exit', 'quit']:
        print("Bot: Bye!")
        break
    print(respond(user_input))
```

### Homework

- Create a function for keyword matching

- Add a list of fallback responses and randomly select one

- Update the chatbot to log each conversation turn to a Python list