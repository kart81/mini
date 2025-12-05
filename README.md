

---

# ⏰ Mini Projects – Clock & To-Do List

A collection of simple beginner-friendly JavaScript projects demonstrating DOM manipulation, time functions, and local storage usage.

---

## 📌 Projects Included

### 1️⃣ **Digital Clock**

A real-time digital clock built using HTML, CSS, and JavaScript.

#### **Features**

* Displays current **time** and **date**
* Updates every second
* Lightweight and responsive design

#### **Technologies**

* HTML
* CSS
* JavaScript (`setInterval`, `Date()` API)

#### **How it Works**

The clock uses JavaScript's `Date()` object to fetch the current date & time and updates the UI every second using `setInterval()`.

#### **Demo Code Snippet**

```javascript
function updateTime() {
  const now = new Date();
  document.getElementById("time").innerText = now.toLocaleTimeString();
  document.getElementById("date").innerText = now.toLocaleDateString();
}

setInterval(updateTime, 1000);
updateTime();
```

---

### 2️⃣ **To-Do List App**

A simple task manager that stores tasks in the browser using Local Storage.

#### **Features**

* Add new tasks
* Mark tasks as completed
* Delete tasks
* Automatically saves tasks in **Local Storage**
* Clean and minimal UI

#### **Technologies**

* HTML
* CSS
* JavaScript (LocalStorage API)

#### **How it Works**

Each task is stored inside `localStorage` so the list remains even after refreshing the page.

#### **Demo Code Snippet**

```javascript
function addTask() {
  const taskInput = document.getElementById("taskInput");
  const tasks = JSON.parse(localStorage.getItem("tasks")) || [];

  tasks.push(taskInput.value);
  localStorage.setItem("tasks", JSON.stringify(tasks));

  taskInput.value = "";
  renderTasks();
}
```

---

## 🚀 How to Run the Projects

1. Download or clone the project:

   ```bash
   git clone https://github.com/your-username/mini-projects.git
   ```
2. Open the project folder
3. Run any `.html` file directly in your browser

---

## 📁 Project Structure

```
mini-projects/
│
├── clock/
│   ├── index.html
│   ├── style.css
│   └── script.js
│
└── todo-list/
    ├── index.html
    ├── style.css
    └── script.js
```

---

## ✨ Future Enhancements

* Add dark/light theme toggle
* Add analog clock version
* Add drag-and-drop support for tasks
* Add deadlines and reminders

---

## 🤝 Contributing

Feel free to fork this project and improve it! Pull requests are welcome.

---

## 📜 License

This project is open-source and available under the MIT License.

---


