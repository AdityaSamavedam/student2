---
toc: True
comments: True
layout: post
title: CPT Project Final Review
courses: {'compsci': {'week': 24}}
type: hacks
---

<style>
    * {
        color: white
    }
</style>

# Project Overview


<p>Our project is called "Your Game Universe", where you can play simple games (some are free and for others you have to log-in), explore the eyedropper, do some HTML coding, manage your tasks if you want to feel productive, and even design your own game with our own GUI editor! We have a Login page, as well as a sign-up page if you would like to sign up and get access to all games.</p>
---

# My Feature

The features I worked on are:
- GUI Editor:
    - JavaScript Runner: write JavaScript code, and the output will be shown when you open the Browser Inspect tool
    - Delete Boxes feature: can despawn a box with the click of a button 
    - Secondary color: switch primary and secondary color, which comes in handy when you don't want to constantly change colors and in turn forget which values of RGB you used.
- HTML Runner: runs html code and displays output
- Eyedropper Color Picker: allows user to select any pixel on the screen and returns the color along with its hex value.
- Task List Manager: allows user to enter tasks to complete, mark as done, and delete.

# Component A: Program Code

| Collegeboard Requirements | My Project|
|------------------|------------------|
| Instructions for input from one of the following: the user, a device, an online datas stream, a file.  | <img src="/student2/images/CPTFinal/sliders.png"> <img src="/student2/images/CPTFinal/pixel.png"> <img src="/student2/images/CPTFinal/console.png"> <br><br> My features take user input through sliders, pixel selection, text input, and button input.|
| Use of at least one list (or other collection type) to represent a collection of data that is stored and used to manage program complexity and help fulfill the users purpose.  | <img src='/student2/images/CPTFinal/listinit.png'> This is the initialization of the list that is used to store the user's entered tasks. When the user creates or deletes tasks, the list is updated accordingly to the respective result.|
| At least one procedure that contributed to the program's intened purpose where you have defined: the name, return type, one or more parameters:  | <img src='/student2/images/CPTFinal/funccrit.png'> <br><br> This procedure's name is switchColors, the return type is boolean, and the parameters are tileEditorSetColor and secondTileEditorSetColor. The purpose of this was to switch the primary and secondary colors when the "Switch Colors" button was clicked.|
| An algorithm that includes sequencing, selection, and iteration that is in the body of the selected procedure | <img src='/student2/images/CPTFinal/seqseliter.png'> <br><br> Sequencing: The function begins by getting the reference to the task list element (const taskList = document.getElementById('taskList');) and initializing it to an empty string (taskList.innerHTML = '';). This sequence ensures that the task list is cleared before rendering new tasks. <br><br> Iteration: The function iterates through the tasks array using forEach(), creating HTML elements (e.g., <li>, checkbox, label, delete button) for each task to render them on the task list. <br><br> Selection: In the iteration, there's selection logic to style the label based on the task's completion status. If completed, it applies a line-through style; otherwise, no style is applied, determining the task's visual representation.|
| Calls to your student-developed procedure: | <img src='/student2/images/CPTFinal/functioncall.png'> <br><br> When the "Switch Colors" button is being clicked, the switchColors function/procedure gets called. |
| Instructions for output (tactile, audible, visual, or ) based on input and program functionality  | <img src='/student2/images/CPTFinal/updatefunctions.png'><br><img sec='/student2/images/CPTFinal/updatecalls.png'> <br><br> This code has the functions to update the colors in each thumbnail, and also the slider positions. They are called in the switchColors function. |

# Component B: Video

[Link to Video](https://drive.google.com/file/d/1gFN7XoDIJG1DzACinSUGHKODmcCWlQx7/view?usp=sharing)


| Collegboard Requirements | My Video |
|------------------|------------------|
| Input to program  | This was shown in the video where I entered code in the JavaScript and HTML Runners, adjusted sliders to create different colors, selected any pixel on the screen to output its color, and entered tasks in the task list manager. |
| At least one aspect of the functionality of your program | My HTML runner is also capable of correctly displaying the output of our project's index.html which makes it useful for viewing the output when there is also CSS and JavaScript.|
| Output produced by program:  | JavaScript Runner output can be seen in browser inspect console. HTML runner output is produced in the box on the right side. When sliders for color are altered, the output can be seen in the tile editor. |
| My video does not contain: | Any distinguishing information about myself or voice narration.  |
| My video is | .mp4, exactly 1 minute in length, and less than 30MB in file size.|

<script src="https://utteranc.es/client.js"
        repo="adityasamavedam/student2"
        issue-term="pathname"
        theme="github-dark"
        crossorigin="anonymous"
        async>
</script>