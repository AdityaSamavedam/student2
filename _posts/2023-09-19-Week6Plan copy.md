---
toc: true
comments: false
layout: post
title: Wk 6 Plan
description: random monke program
courses: { compsci: {week: 6} }
type: tangibles
---

<html>
<head>
    <title>Button Message Example</title>
</head>
<body>
    <button id="myButton">Click Me</button>
    <p id="message"></p>
    
    <script>
    var button = document.getElementById("myButton");
    
    var messageElement = document.getElementById("message");
    
    button.addEventListener("click", function() {
        var message = "Hello, World!";
        
        messageElement.innerText = message;
    });
</script>

</body>
</html>