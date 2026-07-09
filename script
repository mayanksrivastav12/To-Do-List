// Step 1: Grab references to the HTML elements we need to work with
const taskInput = document.getElementById("taskInput");
const addBtn = document.getElementById("addBtn");
const taskList = document.getElementById("taskList");

// Step 2: When the "Add" button is clicked, run addTask()
addBtn.addEventListener("click", addTask);

// Step 3 (bonus): Also allow pressing "Enter" key to add a task
taskInput.addEventListener("keypress", function (event) {
  if (event.key === "Enter") {
    addTask();
  }
});

// This function creates a new task and adds it to the list
function addTask() {
  const taskText = taskInput.value.trim(); // trim() removes extra spaces

  // If the input is empty, do nothing
  if (taskText === "") {
    return;
  }

  // Step A: Create a new <li> element for this task
  const li = document.createElement("li");

  // Step B: Create a <span> to hold the task text
  const span = document.createElement("span");
  span.textContent = taskText;
  span.classList.add("task-text");

  // Step C: Clicking the text toggles "completed" style (strikethrough)
  span.addEventListener("click", function () {
    span.classList.toggle("completed");
  });

  // Step D: Create a delete button for this task
  const deleteBtn = document.createElement("button");
  deleteBtn.textContent = "Delete";
  deleteBtn.classList.add("delete-btn");

  // Step E: Clicking delete removes this <li> from the list
  deleteBtn.addEventListener("click", function () {
    li.remove();
  });

  // Step F: Put the span and button inside the <li>
  li.appendChild(span);
  li.appendChild(deleteBtn);

  // Step G: Add the <li> to the <ul> task list
  taskList.appendChild(li);

  // Step H: Clear the input box for the next task
  taskInput.value = "";
  taskInput.focus();
}
