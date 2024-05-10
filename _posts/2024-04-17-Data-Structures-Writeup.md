---
toc: True
comments: True
layout: post
title: Data Structures Writeup
courses: {'compsci': {'week': 31}}
type: hacks
---

### **_Project Description_**
The purpose of our project is to diagnose cancer based on the properties of the cell such as its area, perimeter, smoothness, concavity, etc. Numerical values are entered in these criteria and the probability of having cancer is determined with all the appropriate data entered. We integrated some of our Tri 2 CPT project features to create "Your Game Universe", which is a game site with a bunch of simple and fun games, to relieve stress and cope if the person has cancer, based on the diagnosis. Some of our games include Tic-Tac-Toe, 2048, Drawing, Ping Pong, etc.

### **_Collections_**
_Blog Python Model code and SQLite Database._

- **From VSCode using SQLite3 Editor, show your unique collection/table in database, display rows and columns in the table of the SQLite database.**
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/90d3b94c-1b55-4c83-ade8-50335e3c6196)
This is my unique collection/table in the database and there are 6 rows (6 different users) and 8 columns. This is the database that data is being fetched from in our login page.

- **From VSCode model, show your unique code that was created to initialize table and create test data.**
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/42527fe3-1761-42b2-b3f4-2afda10fb650)
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/b1cfb8c5-f15c-499f-95a3-d2a0513f7cd8)
This is the code that is used to define the Users and their corresponding personal data. This is where all the login page usernames and passwords can be found.

### **_Lists and Dictionaries_**
_Blog Python API code and use of List and Dictionaries._

- **In VSCode using Debugger, show a list as extracted from database as Python objects.**

![image](https://github.com/AdityaSamavedam/student2/assets/114468365/b927ef4e-7fed-4acf-ae5c-ea99a7d971ed)

This is the list "users" which is the list of all the users extracted from the database.

- **In VSCode use Debugger and list, show two distinct example examples of dictionaries, show Keys/Values using debugger.**

![image](https://github.com/AdityaSamavedam/student2/assets/114468365/879425f7-f43a-4ac3-9399-519416702d78)

The argument "hashmap" when creating a user is an example of a dictionary because it has the keys "job" and "Company" and also has its values such as "football player" and "Seattle Seahawks".

![image](https://github.com/AdityaSamavedam/student2/assets/114468365/0b6e0def-5d02-450c-9608-276e381090c3)

The return command in the function "read" outputs a dictionary with keys: id, userID, note, image and base64 and its corresponding values.

### **_APIs and JSON_**
_Blog Python API code and use of Postman to request and respond with JSON._

- **In VSCode, show Python API code definition for request and response using GET, POST, UPDATE methods. Discuss algorithmic condition used to direct request to appropriate Python method based on request method.**
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/ccc934cb-304c-4f86-af44-987e4ad3ca86)
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/648cfea6-0725-4a38-912f-b54d8460871b)
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/023ec81e-5b8e-48ba-8991-6ccd1deef093)

In the update function, we check that the number of characters in each name, uid, and password are greater than zero characters in order to update the database.

- **In VSCode, show algorithmic conditions used to validate data on a POST condition.**
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/8751211b-25dd-4a42-bd84-33db2a6b63dd)

The conditions fail if the length of name/uid is less than 2 characters. It correspondingly returns the appropriate error message that it is missing or less than 2 characters.

- **In Postman, show URL request and Body requirements for GET, POST, and UPDATE methods.**
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/cb7c1b4b-b497-4a36-9c90-dbb34f373757)

The URL for GET and UPDATE is http://127.0.0.1:8088/api/users/
<br>
The URL for POST is the same thing but with an authenticate added at the end: http://127.0.0.1:8088/api/users/authenticate
<br>
The body requires a correct uid and password for it to work.

- **In Postman, show the JSON response data for 200 success conditions on GET, POST, and UPDATE methods.**
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/90df04f2-efd8-40e7-b3c2-24340d3a44bd)

The success condition displays the info about all the users from the database initially shown. It is formatted into JSON data.

- **In Postman, show the JSON response for error for 400 when missing body on a POST request.**
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/0b150bfa-507a-41a6-9267-622f94da0947)

If the body provided is missing on the POST request, a message "Something went wrong" is displayed. The error shows "400" and the data shows "null" meaning that no body was provided.

- **In Postman, show the JSON response for error for 404 when providing an unknown user ID to a UPDATE request.**
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/39122fbc-a3e3-4bd2-b975-6a2cbbda00ad)

Here, when I type the username "gdis" the message "Invalid user id or password" is outputted because the username is wrong. It should be "adis" instead of "gdis".

### **_Frontend_**
_Blog JavaScript API fetch code and formatting code to display JSON._

- **In Chrome inspect, show response of JSON objects from fetch of GET, POST, and UPDATE methods.**
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/e9c2fbeb-6419-4e27-9da0-8f1491eae731)

In the inspect code, the body can be seen, which matches what exactly I entered in the UID and Password fields prior to hitting the breakpoint.

- **In the Chrome browser, show a demo (GET) of obtaining an Array of JSON objects that are formatted into the browsers screen.**
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/23efae81-0c9c-43ab-b9d0-c6651151d4d5)

This uses a GET method to get the JSON data from the database, which is exactly what happened when I ran the GET method in Postman with the 200 success. We then used JavaScript to format the data into a simple table as shown above.

- **In JavaScript code, describe fetch and method that obtained the Array of JSON objects.**

"fetch(url, authOptions)" gets the url from the backend server (http://127.0.0.1:8088) followed by the suffix "/api/users/authenticate". This is first done to authenticate the user, before they gain access to the array of JSON objects that are formatted into the browser's screen. When the login is successful, the page is redirected to the Database of users that was formatted in the browser.  Next, the url is passed as "http://127.0.0.1:8088/api/users/" since we want to obtain the actual JSON data of the users in the database.  Another fetch is done with the url and when the data is fetched, HTML formats all of it into a table, to make it resemble the SQLite database.

- **In JavaScript code, show code that performs iteration and formatting of data into HTML.**

![image](https://github.com/AdityaSamavedam/student2/assets/114468365/40f5e276-db6d-4c14-9a6c-c50336aaf5f1)

`const headerRow = document.createElement("tr")` creates a header row for the column names

`const th = document.createElement("th");` creates a header for each attribute of the user

`const tr = document.createElement("tr");` creates a row for each of the users

`const td = document.createElement("td");` formats the data into the corresponding cells of the table
 
- **In the Chrome browser, show a demo (POST or UPDATE) gathering and sending input and receiving a response that show update. Repeat this demo showing both success and failure.**

![image](https://github.com/AdityaSamavedam/student2/assets/114468365/df927acd-8b89-48ea-99d9-9ba84708ae8b)
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/508657cd-d714-4a4b-9708-7cbb2c49e7dd)

This is the result for 200 success when the UID and password provided in the login are correct and match the UID and password from the database. It redirects the user to the database table that was formatted into the browser screen.

![image](https://github.com/AdityaSamavedam/student2/assets/114468365/a6e1c78f-965d-4cef-8ff6-35a114e06b52)
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/b94a031d-78a5-4c22-8cda-83bb64f5d752)

As you can see, I've entered `"adiw"` instead of `"adis"`, which is incorrect. Hence it takes the user to the 401 Unauthorized page in order to prevent them from seeing the data.

- **In JavaScript code, show and describe code that handles success. Describe how code shows success to the user in the Chrome Browser screen.**

![image](https://github.com/AdityaSamavedam/student2/assets/114468365/aaadf735-e31a-4f9b-9b05-90eb961316fe)

If the user's username and password match correctly, the user will be redirected to the formatted HTML database table.
Redirecting the user is done with `window.location.href = "http://127.0.0.1:5500/_posts/2024-02-06-DataBase.html"`

- **In JavaScript code, show and describe code that handles failure. Describe how the code shows failure to the user in the Chrome Browser screen.**

![image](https://github.com/AdityaSamavedam/student2/assets/114468365/b6e9cccb-2ff0-48d0-81f6-130ffa949982)

If the user's username or password do not match correctly, or if an error is caught, then the user will not be able to access the database table, which redirects them to the 401 page, saying that they are "Unauthorized". The console logs that there was an error. Again, redirecting is done with `window.location.href = "http://127.0.0.1:5500/_posts/2024-02-07-401error.html"`but with the 401 error page instead of the Database page.

### **_Optional/Extra, Algorithm Analysis_**
_In the ML projects, there is a great deal of algorithm analysis. Think about preparing data and predictions._

- **Show algorithms and preparation of data for analysis. This includes cleaning, encoding, and one-hot encoding.**
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/82dba5d9-4192-4f94-981b-2e74f64a40ac)

Over here, I am cleaning the data by dropping an unnecessary column"diagnosis_cat". I don't really need it because I already have a column called "diagnosis" that outputs 0 or 1 based on whether the cell is malignant or benign.

![image](https://github.com/AdityaSamavedam/student2/assets/114468365/aaf6005d-fc6c-40d5-84db-ed17794fc1d5)

One-hot encoding is shown in the line `self.encoder = OneHotEncoder(handle_unknown='ignore')`

- **Show algorithms and preparation for predictions.**
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/2b3110ec-f111-45c7-a685-fd11ffa39929)

The data is being prepared by splitting the data into features (X variables) and target (y variable). It performs the train, test, and split in `self.model = LogisticRegression(max_iter=1000)`. It actually trains the data in the line `self.model.fit(X,y)` which fits the model and passes the X and y values.

![image](https://github.com/AdityaSamavedam/student2/assets/114468365/2b906d61-ae24-44bf-b0b0-083859e9548b)

- **Discuss concepts and understanding of Linear Regression algorithms.**

Linear regression involves the relationship between two variables (x and y). Given a large dataset (pandas dataframe) of x and y values, the linear regression algorithm will try to find a correlation in the scatterplot and plot the line of best fit. Usually, 80% of the data is the training data, and the rest 20% is the test data. This is done so that the maximum possible accuracy is achieved. After the model is trained, it is tested with the test data. Given test x values, we get our y prediction values based on the line of best fit that was calculated during training. Linear regression is an example of supervised learning because the machine trains off of data that is labeled.

Our project is similar to Linear Regression, but it does not exactly use it. It uses Logistic Regression because there are multiple x-variables being provided and there is only one y-variable.

Here is a comparison of the two:
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/01b4a92d-0008-4027-af29-474cd5999b6e)
Logistic Regression aims to output discrete values like 0 or 1, unlike Linear Regression which just finds a correlation between x and y/

- **Discuss concepts and understanding of Decision Tree analysis algorithms.**
![image](https://github.com/AdityaSamavedam/student2/assets/114468365/9fde4858-829a-400e-b76e-f30f52f82a4e)

Decision Trees are used mainly for classification and regression (usually logistic regression) purposes. We start at the root node (or the first node), which contains the entire dataset. Then, the algorithm splits the data based on certain criteria and new nodes are created accordingly. Then, the data is partitioned into more subsets based on the possible values of that feature.  This is done repeatedly until we reach a stopping condition, and the leaf nodes (last nodes) are formed. The leaf nodes show our output as a result of the decision tree.

The picture above is an example of a decision tree being used for logistic regression, on deciding whether a person should go outside or not, based on the weather conditions.
- We start with the root node "Outlook" which means that we are looking at the weather and starting the decision tree. Next, we are provided with three categories: "Sunny", "Overcast" and "Rain".
    - If the weather is sunny, a new node "Humidity" is created.
        - If the Humidity is high, then we shouldn't go outside. If the Humidity is low, then we can go outside. The decision tree stops as either "Yes" or "No" and they become the leaf nodes or our output. 
    - If the weather is overcast, then the leaf node "Yes" is immediately created and we can go outside.
    - If the weather is rainy, then a new node "Wind" is created. 
        - A strong wind means that we shouldn't go outside. Similarly, a weak wind means that we can go outside. Again, the decision tree ends at the leaf nodes "Yes" or "No"

Our project used a decision tree classifier for our model, as shown in the code lines:
<br>

 `self.dt = DecisionTreeClassifier`
 <br>

 `self.dt.fit(X,y)`

<script src="https://utteranc.es/client.js"
        repo="adityasamavedam/student2"
        issue-term="pathname"
        theme="github-dark"
        crossorigin="anonymous"
        async>
</script>