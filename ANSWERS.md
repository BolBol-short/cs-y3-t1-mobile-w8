# 				W8	Practice

### 			Lists, Pass Functions, Lift States Up

##### EX 1 - Loop when creating widgets ...

Q1 - In what scenarios might one approach **be more advantageous** than another? (in terms of readability, maintainability, performance, etc.)

A1 = In terms of readability, maintainability, performance, beginner friendly, 

| Type               | When to use it                                                                                | Readability                                                                        | Maintainability                                                                             | Performance |
| ------------------ | --------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- | ----------- |
| Loops              | When I need the index, like numbering items, or when each item is one small widget           | Easy to read since loop is short but get messy when the widget inside is big       | Okay for small loops. If build() has many loops, they are hard to find and can't reuse them | O(n)        |
| .map() method      | When I wanted to turn each item in the list into a widget, and don't need the index           | short and clean for simple cases                                                   | The code stays inside build() and has no name, I can't reuse it somewhere else              | O(n)        |
| dedicated function | When the code to build the widgets is long, or I need the same widgets in more than one place | Easiest to read in build(), because the name (function name) tells me what it does | Easiest to maintain, since the logic is in one place, and I can reuse them                  | O(n)        |

Q2 - Coding [done]

##### EX 2 - Switch Screen using a state

Q1 - Reflect in group

- How are you going to manage this?
- Explain your solution using a **component diagram** (WelcomeScreen + TemperatureScreen)

A1 = 

- I am going to manage this by puting the state in the parent, 'TemperatureApp', which is a Stateful widget. I added a `bool` called `_log = false`. In build(), I use a ternary operator to pick between the TemperatureScreen or WelcomeScreen. Since, WelcomeScreen can't change `_log` by itself, so the parent gives it a callback called `isLogged`. When I pressed the button, it will switch to the TemperatureScreen.
- Component Diagram:

![1795231188010](image/ANSWERS/1795231188010.png)

Q2 - Coding [Done]

##### EX 3 - Refactor the code to bind with data

Coding [Starting]

##### EX 4 - Manage a list of jokes

Coding [Starting]

You will need to **re-think** about your **data structure** and **widget interaction** to perform the changes:

| Questions                                                                                                                                   | Answers                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------- |
| - What **type of data** will store the jokes?<br />- What **type of data** will store the favorite joke?                  | - The jokes will be store as<br />- The favorite joke will be stored as                                                              |
| - **Which widgets** should be in charge **of storing the favorite joke?**<br />- Which widget should be **stateful?** | - **Widget** that should be in charge **of storing the favorite joke** is<br />- Widgets that should be stateful are: |
| - How will your widget interact?<br />- Do you need to **pass callback function** between widgets?                                | - The Widgets will interact<br />- Yes/No                                                                                             |

##### Bonus

Coding [Starting]
