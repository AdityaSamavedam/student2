---
toc: True
comments: False
layout: post
title: Login Page Backup
description: Spot Check Individual Login Page
courses: {'compsci': {'week': 20}}
type: tangibles
---

<h1>Login</h1>

<style>
    form {
        max-width: 300px; 
        margin: 0 auto;
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.1); 
        padding: 20px;
        border-radius: 8px;
    }

    input {
        width: 100%;
        padding: 10px;
        margin-bottom: 15px;
        box-shadow: inset 0 0 5px rgba(0, 0, 0, 0.1); 
        border: 1px solid #ccc;
        border-radius: 4px;
        transition: box-shadow 0.3s ease; 
    }

    input:focus {
        outline: none;
        box-shadow: 0 0 10px rgba(0, 0, 255, 0.5);
    }

    button {
        background-color: #4CAF50;
        color: white;
        padding: 10px 15px;
        border: none;
        border-radius: 4px;
        cursor: pointer;
        box-shadow: 0 0 10px rgba(0, 128, 0, 0.5); 
        transition: box-shadow 0.3s ease; 
    }

    button:hover {
        box-shadow: 0 0 15px rgba(0, 128, 0, 1);
    }
</style>

<form action="javascript:login_user()">
    <!-- ... -->
</form>

<script type="module">
</script>

<form action="javascript:login_user()">
    <p><label>
        User ID:
        <input type="text" name="uid" id="uid" required="" />
    </label></p>
    <p><label>
        Password:
        <input type="password" name="password" id="password" required="" />
    </label></p>
    <p>
        <button>Login</button>
    </p>
    <p id="loginStatus" name="loginStatus">null</p>
</form>


<script type="module">

    function login_user(){
        const url ='http://127.0.0.1:8086/api/users/authenticate';

        const body = {
            uid: document.getElementById("uid").value,
            password: document.getElementById("password").value,
        };

        const authOptions = {
            mode: 'cors', 
            credentials: 'include', 
            headers: {
                'Content-Type': 'application/json',
            },
            method: 'POST',
            cache: 'no-cache',
            body: JSON.stringify(body)
        };

        fetch(url, authOptions)
        .then(response => {
            if (!response.ok) {
                const errorMsg = 'Login error: ' + response.status;
                console.log(errorMsg);
                if (response.status == 500) {
                    document.getElementById("loginStatus").innerHTML = "incorrect username or password";
                    return;
                }
            }

          
            window.location.href = "http://127.0.0.1:4200/student2/2024/02/06/DataTable.html"
            ;
        })
       
        .catch(err => {
            window.location.href = "http://127.0.0.1:4200/student/2024/01/31/401error.html"
            console.error(err);
        });
    }

   
    window.login_user = login_user;
</script>