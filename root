<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do App</title>
  <style>
    * { box-sizing: border-box; margin:0; padding:0; font-family: Arial, sans-serif; }
    body { background:#f0f2f5; display:flex; justify-content:center; align-items:center; height:100vh; }
    .container { background:#fff; padding:20px; border-radius:10px; box-shadow:0 4px 10px rgba(0,0,0,0.1); width:100%; max-width:400px; }
    h1 { text-align:center; margin-bottom:20px; color:#333; }
    .input-section { display:flex; gap:10px; margin-bottom:20px; }
    input { flex:1; padding:10px; border:1px solid #ccc; border-radius:5px; }
    button { padding:10px 15px; border:none; background:#007bff; color:white; border-radius:5px; cursor:pointer; }
    button:hover { background:#0056b3; }
    ul { list-style:none; }
    li { padding:10px; background:#f9f9f9; margin-bottom:10px; border-radius:5px; display:flex; justify-content:space-between; align-items:center; }
    li.completed { text-decoration:line-through; color:gray; }
    .deleteBtn { background:red; border:none; color:white; padding:5px 10px; border-radius:5px; cursor:pointer; }
    .deleteBtn:hover { background:darkred; }
  </style>
</head>
<body>
  <div class="container">
    <h1>My To-Do List</h1>
    <div class="input-section">
      <input type="text" id="taskInput" placeholder="Enter a task...">
      <button id="addBtn">Add</button>
    </div>
    <ul id="taskList"></ul>
  </div>

  <script>
    const taskInput = document.getElementById('taskInput');
    const addBtn = document.getElementById('addBtn');
    const taskList = document.getElementById('taskList');

    // Vazifani qo'shish
    addBtn.addEventListener('click', () => {
      const taskText = taskInput.value.trim();
      if(taskText === "") return;

      const li = document.createElement('li');
      li.textContent = taskText;

      // Completed toggle
      li.addEventListener('click', () => {
        li.classList.toggle('completed');
      });

      // Delete tugma
      const deleteBtn = document.createElement('button');
      deleteBtn.textContent = "Delete";
      deleteBtn.className = "deleteBtn";
      deleteBtn.addEventListener('click', (e) => {
        e.stopPropagation();
        taskList.removeChild(li);
      });

      li.appendChild(deleteBtn);
      taskList.appendChild(li);
      taskInput.value = "";
    });
  </script>
</body>
</html>
