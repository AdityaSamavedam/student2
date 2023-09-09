---
toc: True
comments: True
layout: post
title: Task List Maker
description: Task List Maker made in Javascript
courses: {'compsci': {'week': 3}}
type: tangibles
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Task List Maker</title>
</head>
<body>
    <div id="output"></div>
    <input type="text" id="input" placeholder="Enter the number">
    <button onclick="processInput()">Submit</button>

<script>
    let condition = true;
    let tasksQueue = [];
    var button = document.getElementById("Submit")
    function printMessage(message) {
        document.getElementById('output').innerHTML += message + '<br>';
    }

    function processInput() {
        let taskNum = parseInt(document.getElementById('input').value);

        if (taskNum === 1) {
            let newTask = prompt("Enter your task:");
            tasksQueue.push(newTask);
            printMessage(`Task ${newTask} added!`);
        } else if (taskNum === 2) {
            if (tasksQueue.length === 0) {
                printMessage("No tasks in the list.");
            } else {
                printMessage(`Your first task is ${tasksQueue[0]}.`);
            }
        } else if (taskNum === 3) {
            if (tasksQueue.length === 0) {
                printMessage("No tasks in the list.");
            } else {
                printMessage(`You completed/removed the task ${tasksQueue[0]}.`);
                tasksQueue.shift();
            }
        } else if (taskNum === 4) {
            tasksQueue.length = 0;
            printMessage("All tasks are cleared!");
        } else if (taskNum === 5) {
            printMessage("Goodbye!");
            button.style.display = "none";
            condition = false;
        } else {
            printMessage("Invalid number entered. Please try again.");
        }
    }
</script>
</body>
</html>