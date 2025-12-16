# Practice 2: Dynamic List (Medium)

## Objective
Practice creating, adding, and removing DOM elements dynamically.

## Requirements

Create a dynamic list manager:

1. HTML with:
   - An input field for new items
   - An "Add Item" button
   - An empty `<ul>` for the list
   - Display count of items

2. JavaScript functionality:
   - Add new items to the list when button is clicked
   - Each list item should have a "Delete" button
   - Delete individual items when delete button is clicked
   - Update the count display
   - Clear the input after adding
   - Prevent adding empty items

## Tips
- Use `createElement()` to create new elements
- Use `appendChild()` to add elements
- Use `remove()` or `removeChild()` to delete
- Add event listeners to dynamically created buttons
- Use `textContent` or `value` to get input values
