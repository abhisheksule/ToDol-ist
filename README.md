
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List</title>
  <style>
    body {
      font-family: Arial, sans-serif;
    }
    ul {
      list-style-type: none;
      padding: 0;
    }
    li {
      margin-bottom: 8px;
    }
  </style>
</head>
<body>

  <h1>To-Do List</h1>
  
  <input type="text" id="taskInput" placeholder="Add a new task">
  <button onclick="addTask()">Add Task</button>

  <ul id="taskList"></ul>

  <script>
    function addTask() {
      var taskInput = document.getElementById("taskInput");
      var taskList = document.getElementById("taskList");

      if (taskInput.value.trim() !== "") {
        var li = document.createElement("li");
        li.appendChild(document.createTextNode(taskInput.value));
        taskList.appendChild(li);
        taskInput.value = "";
      }
    }
  </script>

</body>
</html>

