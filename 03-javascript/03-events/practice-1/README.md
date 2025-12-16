# Practice 1: Button Click Counter (Easy)

## Objective
Practice handling click events and updating the UI based on user interaction.

## Requirements

Create a simple click counter application:

1. HTML with:
   - A heading displaying "Click Count: 0"
   - A "Click Me" button
   - A "Reset" button
   - A message area that shows different messages based on count

2. JavaScript functionality:
   - Increment counter when "Click Me" is clicked
   - Update the heading with new count
   - Reset counter to 0 when "Reset" is clicked
   - Display different messages at milestones:
     - At 10 clicks: "You're doing great!"
     - At 25 clicks: "Wow, that's a lot of clicks!"
     - At 50 clicks: "Amazing! You're a clicking master!"
   - Change button color after 10 clicks

## Tips
- Use `addEventListener('click', ...)` for buttons
- Store count in a variable
- Use template literals for dynamic messages
- Use `style` property to change colors
