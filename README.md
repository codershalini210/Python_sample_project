Command-Line Task Manager
A simple Python command-line application for managing daily tasks. Users can add tasks, display all tasks, mark tasks as completed, and view a task summary.

Features
Add a new task
Display all tasks
Mark a task as completed
View total, completed, and pending task counts
Exit the application from the menu
Requirements
Python 3.x
No external libraries are required
Installation
Clone or download this repository, then navigate to the project directory:

bash


git clone <repository-url>
cd <repository-directory>
Usage
Run the Python file from your terminal:

bash


python task_manager.py
The following menu will appear:

text


Press:
1: Add task
2: Show Task
3: Complete Task
4: Summary
exit: Exit
Menu Options
1. Add Task
Enter 1, then provide the name of the task.

text


Enter task: Complete assignment
Task Added Successfully
New tasks are initially marked as incomplete.

2. Show Tasks
Enter 2 to display all tasks and their completion status.

text


[{'Complete assignment': False}, {'Read a book': True}]
False means the task is pending.
True means the task is completed.
3. Complete Task
Enter 3, then provide the exact name of the task you want to complete.

text


Enter task to mark as complete: Complete assignment
Task Complete assignment is completed
If the task does not exist or has already been completed, the program displays:

text


item not present
4. View Summary
Enter 4 to view the number of total, completed, and pending tasks.

text


Total Task: 2
Completed task: 1, pending: 1
Exit
Enter exit to close the application.

How It Works
Tasks are stored in a list of dictionaries:

python


taskList = [
    {"Complete assignment": False},
    {"Read a book": True}
]
Each dictionary contains:

A task name as its key
A Boolean completion status as its value
False for a pending task
True for a completed task
Limitations
Tasks are stored only in memory and are lost when the application closes.
Task names must match exactly when marking them as completed.
Duplicate task names are allowed.
Tasks cannot currently be edited or deleted.
Completed tasks cannot be marked as pending again.
Possible Improvements
Save tasks to a JSON or text file
Display tasks in a numbered, readable format
Add options to edit and delete tasks
Prevent duplicate task names
Make task searches case-insensitive
Validate empty task names and invalid menu input
Allow completed tasks to be reopened
License
This project is available for educational and personal use.