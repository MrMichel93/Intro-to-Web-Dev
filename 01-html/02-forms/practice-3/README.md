# Practice 3: Survey Form (Hard)

## Objective

Create a comprehensive survey form that uses various input types, proper organization with fieldsets, and demonstrates advanced form features. This will test your complete understanding of HTML forms.

## Requirements

Create a file named `survey.html` that includes:

1. Proper HTML5 document structure
2. A page title: "Customer Satisfaction Survey"
3. An `<h1>` heading: "Customer Satisfaction Survey"
4. An introductory paragraph explaining the survey
5. Multiple `<fieldset>` sections with `<legend>` tags for organization:

   **Section 1: Personal Information**
   - Full Name (text, required)
   - Email (email, required)
   - Age (number, min 13, max 120)
   
   **Section 2: Product Experience**
   - How did you hear about us? (dropdown with options: Social Media, Friend, Advertisement, Search Engine, Other)
   - How long have you been a customer? (radio buttons: Less than 6 months, 6-12 months, 1-2 years, More than 2 years)
   - Which products have you used? (multiple checkboxes: at least 4 products)
   
   **Section 3: Satisfaction Ratings**
   - Overall satisfaction (range slider, 0-10)
   - Product quality (range slider, 0-10)
   - Customer service (range slider, 0-10)
   - Value for money (range slider, 0-10)
   
   **Section 4: Feedback**
   - What did you like most? (textarea, 3 rows)
   - What could we improve? (textarea, 3 rows)
   - Would you recommend us to others? (radio: Yes, No, Maybe)
   - Any additional comments? (textarea, 4 rows, optional)

6. A submission section with:
   - Date (date input, required)
   - A checkbox: "I consent to my responses being used for improvement purposes" (required)
   - Submit button: "Submit Survey"
   - Reset button: "Clear All"

## Tips

- Use multiple `<fieldset>` elements to group related questions
- Add meaningful `<legend>` text for each section
- Use appropriate input types for better UX
- Consider using `min` and `max` attributes for validation
- Add placeholders and labels for all inputs
- Display the current value of range sliders using labels

## Bonus Challenges

- Add a file upload field for "Upload screenshot"
- Include a color picker for "Favorite brand color"
- Add a time input for "Best time to contact you"
- Create a custom styling note at the top
- Add helper text under complex fields

## Solution

Try to complete this on your own first!

<details>
<summary>Click to see solution</summary>

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Customer Satisfaction Survey</title>
</head>
<body>
    <h1>Customer Satisfaction Survey</h1>
    
    <p>Thank you for taking the time to complete our survey! Your feedback helps us improve our products and services. This survey should take approximately 5-10 minutes to complete.</p>
    
    <form action="#" method="POST">
        
        <!-- Section 1: Personal Information -->
        <fieldset>
            <legend>Personal Information</legend>
            
            <label for="fullname">Full Name:</label><br>
            <input type="text" id="fullname" name="fullname" 
                   placeholder="John Doe" required><br><br>
            
            <label for="email">Email Address:</label><br>
            <input type="email" id="email" name="email" 
                   placeholder="john.doe@example.com" required><br><br>
            
            <label for="age">Age:</label><br>
            <input type="number" id="age" name="age" 
                   min="13" max="120" placeholder="25"><br>
        </fieldset><br>
        
        <!-- Section 2: Product Experience -->
        <fieldset>
            <legend>Product Experience</legend>
            
            <label for="source">How did you hear about us?</label><br>
            <select id="source" name="source" required>
                <option value="">Please select...</option>
                <option value="social">Social Media</option>
                <option value="friend">Friend or Family</option>
                <option value="ad">Advertisement</option>
                <option value="search">Search Engine</option>
                <option value="other">Other</option>
            </select><br><br>
            
            <p>How long have you been a customer?</p>
            <input type="radio" id="duration1" name="duration" value="0-6months">
            <label for="duration1">Less than 6 months</label><br>
            
            <input type="radio" id="duration2" name="duration" value="6-12months">
            <label for="duration2">6-12 months</label><br>
            
            <input type="radio" id="duration3" name="duration" value="1-2years">
            <label for="duration3">1-2 years</label><br>
            
            <input type="radio" id="duration4" name="duration" value="2+years">
            <label for="duration4">More than 2 years</label><br><br>
            
            <p>Which products have you used? (Select all that apply)</p>
            <input type="checkbox" id="product1" name="products" value="product-a">
            <label for="product1">Product A</label><br>
            
            <input type="checkbox" id="product2" name="products" value="product-b">
            <label for="product2">Product B</label><br>
            
            <input type="checkbox" id="product3" name="products" value="product-c">
            <label for="product3">Product C</label><br>
            
            <input type="checkbox" id="product4" name="products" value="product-d">
            <label for="product4">Product D</label><br>
        </fieldset><br>
        
        <!-- Section 3: Satisfaction Ratings -->
        <fieldset>
            <legend>Satisfaction Ratings</legend>
            <p><em>Rate each aspect from 0 (Very Dissatisfied) to 10 (Very Satisfied)</em></p>
            
            <label for="overall">Overall Satisfaction:</label><br>
            <input type="range" id="overall" name="overall" 
                   min="0" max="10" value="5">
            <span>0 - 10</span><br><br>
            
            <label for="quality">Product Quality:</label><br>
            <input type="range" id="quality" name="quality" 
                   min="0" max="10" value="5">
            <span>0 - 10</span><br><br>
            
            <label for="service">Customer Service:</label><br>
            <input type="range" id="service" name="service" 
                   min="0" max="10" value="5">
            <span>0 - 10</span><br><br>
            
            <label for="value">Value for Money:</label><br>
            <input type="range" id="value" name="value" 
                   min="0" max="10" value="5">
            <span>0 - 10</span><br>
        </fieldset><br>
        
        <!-- Section 4: Feedback -->
        <fieldset>
            <legend>Your Feedback</legend>
            
            <label for="liked">What did you like most about our products/services?</label><br>
            <textarea id="liked" name="liked" rows="3" cols="60" 
                      placeholder="Tell us what you enjoyed..."></textarea><br><br>
            
            <label for="improve">What could we improve?</label><br>
            <textarea id="improve" name="improve" rows="3" cols="60" 
                      placeholder="Your suggestions for improvement..."></textarea><br><br>
            
            <p>Would you recommend us to others?</p>
            <input type="radio" id="rec-yes" name="recommend" value="yes">
            <label for="rec-yes">Yes</label><br>
            
            <input type="radio" id="rec-no" name="recommend" value="no">
            <label for="rec-no">No</label><br>
            
            <input type="radio" id="rec-maybe" name="recommend" value="maybe">
            <label for="rec-maybe">Maybe</label><br><br>
            
            <label for="comments">Any additional comments:</label><br>
            <textarea id="comments" name="comments" rows="4" cols="60" 
                      placeholder="Optional: Share any other thoughts..."></textarea><br>
        </fieldset><br>
        
        <!-- Submission Section -->
        <fieldset>
            <legend>Submission</legend>
            
            <label for="date">Date:</label><br>
            <input type="date" id="date" name="date" required><br><br>
            
            <input type="checkbox" id="consent" name="consent" required>
            <label for="consent">I consent to my responses being used for improvement purposes</label><br><br>
            
            <button type="submit">Submit Survey</button>
            <button type="reset">Clear All</button>
        </fieldset>
        
    </form>
    
    <p><em>Thank you for your valuable feedback!</em></p>
</body>
</html>
```

</details>
