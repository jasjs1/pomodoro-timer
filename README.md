<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<meta http-equiv="X-UA-Compatible" content="IE=edge">
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<link rel="stylesheet" href="style.css">
	<title>Programmer Netlink - Pomodoro Timer</title> 
</head>
<body> 

	<div class="header">
	</div>

	<div class="pomodoro">
		<div class="timer">
		  <div class="time"><strong>25:00</strong></div>
		  	<div class="controls">
			<button id="start"><strong>Start</strong></button>

			<button id="stop"><strong>Stop</strong></button>
			<button id="reset"><strong>Reset</strong></button>
		  </div>
		</div>
		<div class="todolist">
			<h3>To-Do List</h3>
			<ul id="task-list"></ul>
			<label for="new-task">New Task:</label>
			<input type="text" id="new-task">
			<button id="add-task">Add Task</button>
		</div>
		<div class="settings">
		  <h3>Timer Settings</h3>
		  <label for="work-time">Work Time (minutes):</label>
		  <input type="number" id="work-time" value="25" min="1">
		  <label for="break-time">Break Time (minutes):</label>
		  <input type="number" id="break-time" value="5" min="1">
		</div>
	</div>
	
	<script src="script.js"></script>
	<script>
		const taskList = document.querySelector('#task-list');
		const newTaskInput = document.querySelector('#new-task');
		const addTaskButton = document.querySelector('#add-task');

		addTaskButton.addEventListener('click', () => {
			const newTask = document.createElement('li');
			newTask.textContent = newTaskInput.value;
			taskList.appendChild(newTask);
			newTaskInput.value = '';
		});
	</script>



</body>
</html>
