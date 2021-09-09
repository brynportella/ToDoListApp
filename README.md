# ToDoListApp
Instructions for the make-up project for SPARK candidates. 

## Project Overview
Your goal is to create a console based application that allows a user to create and manage their to-do lists. 

## Requirements 

1. A user should be able to add a task to their to-do list. 
2. A user should be able to remove any of the tasks from their to-do list. 
3. A user should be able to view all the tasks on their to-do list.
4. A user should be able to create different types of tasks including a reminder task and a shopping task. 
5. A reminder task should include a title, a description, and a deadline. 
6. A shopping task should include a title, a description, and a list of items to purchase. 
7. For shopping tasks, a user should be able to add and remove items from the shopping list. 
8. A user should be able to continuously perform operations on their to-do list until they choose to quit. 

### Optional Features
* A user can create multiple to-do lists. 
* In addition to adding and removing tasks, a user can mark a task complete. 
* A user can create a task that has sub tasks, i.e. a series of parts that need to be complete for the whole task to be complete. 

## Suggested Project Structure
- Two packages
    - `model`
    Classes in `model`
        - `Task`
        - `ReminderTask`
        - `ShoppingTask`
        - `ToDoList`
    - `main`
    Classes in `main`
        - `User`
        - `Driver`

### `Task`
- Parent class of `ReminderTask` and `ShoppingTask`.
Should include the fields:
`String title`
`String description`

- The class should also include the getter and setter methods for those fields.

- You may choose to include additional methods/fields that you deem useful. 

### `ReminderTask`
- In addition to what was inherited from `Task`, `ReminderTask` should include a field for a deadline. (As we have not discussed any date datatypes, simply use a String to capture this information.)
`String deadline`

- The class should also include the getter and setter methods for deadline. As well as any constructors needed. 

- You may choose to include additional methods/fields that you deem useful. For instance, overriding toString would be recommended. 

### `ShoppingTask`
- In addition to inheriting fields from `Task`, `ShoppingTask` should include a field for a list of items. This could either be an array of Strings or you could use some type of Collection, for example your datatype could be `List<String>`. 
The simplest version of the field would be:
`String[] items`

- The class should also include the getter and setter methods for items. As well as methods to add an item to the list of items. Make sure that you also include any constructors needed. 

- You may choose to include additional methods/fields that you deem useful. For instance, overriding toString would be recommended. 

### `ToDoList`
- This class should have a single field that is a list or array of Task objects. It might look like either 
`List<Task> tasks`
or 
`Task[] tasks`

- The class should also include the getter and setter methods for the list of tasks. As well as methods to add a Task to the list of tasks and to remove one. Make sure that you also include any constructors needed. 

- You may choose to include additional methods/fields that you deem useful. For instance, overriding toString would be recommended. 

### `User`
- This class should keep track of the user's personal to-do list. If you choose to implement the additional features, then it should keep track of all the to-do lists that a user has. 

- In its simplest version the `User` class should have the single field. 
`ToDoList toDoList`
- If you choose to implement the optional requirements you could replace the earlier field with something like the following:
`Map<String, ToDoList> toDoLists`
or
`List<ToDoList> toDoLists`

- The class should also include the getter and setter methods for the to-do list. Make sure that you also include any constructors needed. 

- You may choose to include additional methods/fields that you deem useful. 

### `Driver`
- This class should contain the main method.
- In the Main method:
    - The class should set up the initial User object. 
    - The main loop of the application should allow the user to keep performing operations on the User object's to-do list. 
    - Should use the Scanner to read in user input. 

It's suggested to divide the logic into smaller methods in the Main class that will be called from within the main method. 