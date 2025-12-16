# Practice 3: Todo App (Hard)

## Objective
Build a complete todo list application with full CRUD functionality and local storage.

## Requirements

Create a full-featured todo app:

1. HTML with:
   - Input field for todo text
   - Priority selector (High, Medium, Low)
   - "Add Todo" button
   - Filter buttons (All, Active, Completed)
   - Todo list container
   - Statistics display (total, active, completed)

2. JavaScript features:
   - Add todos with text and priority
   - Mark todos as complete (toggle)
   - Delete individual todos
   - Edit existing todos (click to edit)
   - Filter todos by status
   - Clear all completed todos
   - Save to localStorage
   - Load from localStorage on page load
   - Display statistics

3. Styling:
   - Completed todos have strikethrough
   - Different colors for priorities
   - Visual feedback on interactions

## Tips
- Use data attributes to store todo IDs
- Use `localStorage.setItem()` and `localStorage.getItem()`
- Store todos as JSON string
- Use event delegation for dynamic elements
- Create reusable functions for rendering
