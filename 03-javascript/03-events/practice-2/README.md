# Practice 2: Form Validator (Medium)

## Objective
Practice form events, input validation, and providing user feedback.

## Requirements

Create a registration form with real-time validation:

1. HTML form with fields:
   - Username (min 3 characters)
   - Email (valid email format)
   - Password (min 8 characters, must include number)
   - Confirm Password (must match)
   - Submit button

2. JavaScript validation:
   - Validate each field on `blur` (when user leaves field)
   - Show error messages below invalid fields
   - Show success indicators for valid fields
   - Validate on `input` event for immediate feedback
   - Prevent form submission if any field is invalid
   - Show success message on valid submission
   - Disable submit button until all fields are valid

3. Error messages should be specific:
   - "Username must be at least 3 characters"
   - "Please enter a valid email address"
   - "Password must be at least 8 characters and include a number"
   - "Passwords do not match"

## Tips
- Use `addEventListener('blur', ...)` for validation on blur
- Use `addEventListener('input', ...)` for real-time validation
- Use `event.preventDefault()` to prevent form submission
- Create validation functions for each field
- Use regular expressions for email and password validation
