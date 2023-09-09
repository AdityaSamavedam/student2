---
toc: True
comments: True
layout: post
title: Task Manager
description: Task Manager made in Javascript
courses: {'compsci': {'week': 3}}
type: tangibles
---

condition = True
print("Welcome to a queue task list maker!")
tasks_queue = []
while condition:
  print('''What would you like to do?
  1: add a task
  2: look at the first task
  3: complete (remove) the first task
  4: clear the tasks
  5: exit''')
  task_num = int(input("Enter the number: "))

  if task_num == 1:
    new_task = input("Enter your task:\n")
    tasks_queue.append(new_task)
    print(f"Task {new_task} added!")

  elif task_num == 2:
    if len(tasks_queue) == 0:
      print("No tasks in the list.")
    else:
      print(f"Your first task is {tasks_queue[0]}.")

  elif task_num == 3:
    if len(tasks_queue) == 0:
      print("No tasks in the list.")
    else:
      print(f"You completed/removed the task {tasks_queue[0]}.")
      del tasks_queue[0]

  elif task_num == 4:
    tasks_queue.clear()
    print("All tasks are cleared!")

  elif task_num == 5:
    print("Goodbye!")
    condition = False

  else:
    print("Invalid number entered. Please try again.")
    continue
