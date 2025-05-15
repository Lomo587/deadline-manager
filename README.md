#  Deadline Manager Component

A simple yet powerful web component for managing and tracking deadlines. It displays a list of tasks with countdowns and allows you to add new tasks with deadlines or durations. When a task expires, it will flash red and briefly shake to draw your attention. It supports sorting and local storage persistence.

---

##  Features

- Add deadlines via **duration** (`HH:MM:SS`) or **datetime** (`ISO 8601`).
- Countdown to deadlines, displaying remaining time.
- Expired deadlines show a negative countdown.
- Flashing red and shaking animation when a deadline expires.
- Checkbox to mark a task as complete, locking the countdown.
- List collapses and expands dynamically based on active/expired status.
- Tasks are sorted with the most urgent at the top.
- Local storage support to persist tasks across page reloads.

---

##  Installation

1. Embed the `<deadline-manager>` component in your HTML file:

```html
<deadline-manager></deadline-manager>
```

2. Include the component script:

Copy the script from the documentation or host it as an external file. Make sure to place the `<script>` tag at the **bottom of the body**:

```html
<script src="deadline-manager.js"></script>
```

---

##  Usage

###  Add New Task
- Click on the **"+ Add New Deadline"** button to open the form.
- Choose between entering a duration (`HH:MM:SS`) or a specific date & time.
- Click **"Add Deadline"** to insert the task into the list.

###  Mark Task as Complete
- Check the box next to a task to mark it as done.
- The task will be struck through and countdown will stop.
- Completed tasks are locked and cannot be undone.

###  Clear Completed Tasks
- Click the **"🧹 Clear"** button to remove all completed tasks.

###  List Management
- Use the **"▼ Show" / "▲ Hide"** buttons to toggle visibility.
- Expired tasks auto-expand when the list is shown.

###  Task Sorting
- Tasks are sorted by urgency — closest to expiration appears at the top.

---

##  API / Properties

### Attributes
- `none`: This component does not accept any external attributes.

---

##  Events

The `<deadline-manager>` component emits:

- `deadline-added`: Fired when a new deadline is added.
- `deadline-removed`: Fired when a deadline is removed (e.g., after completion or clearing).

---

##  Methods

- `addDeadline(event)`: Adds a new deadline based on form input.
- `clearCompleted()`: Removes all completed tasks.
- `updateCountdowns()`: Refreshes countdown timers every second.

---

##  Example

Here’s a basic example:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>My Deadline Manager</title>
  <script src="deadline-manager.js"></script>
</head>
<body>
  <h1>Welcome to Deadline Manager!</h1>
  <deadline-manager></deadline-manager>
</body>
</html>
```

---

##  Local Storage

This component uses the browser’s `localStorage` to persist your tasks:
- Tasks are automatically saved when added, completed, or removed.
- When you reload the page, your task list is restored.

---
