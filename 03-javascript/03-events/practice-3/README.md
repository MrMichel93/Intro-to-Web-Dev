# Practice 3: Interactive Game (Hard)

## Objective
Build a complete interactive game combining multiple event types and game logic.

## Requirements

Create a "Reaction Time Game":

1. Game features:
   - Start button to begin game
   - Game area that changes color randomly
   - User must click when they see a specific color (e.g., green)
   - Track reaction time in milliseconds
   - Keep score of correct/incorrect clicks
   - Display best time
   - Round counter (5 rounds per game)
   - Reset and play again

2. Game flow:
   - Click "Start Game"
   - After random delay (1-3 seconds), area turns green
   - User clicks as fast as possible
   - Record reaction time
   - If clicked too early (before green): penalty
   - After 5 rounds: show final score and best time
   - Option to play again

3. Events to handle:
   - Click events on start button and game area
   - Mouse enter/leave for hover effects
   - Keyboard event for spacebar to click
   - Track timing with `setTimeout()` and `Date.now()`

4. Display:
   - Current round number
   - Last reaction time
   - Best reaction time
   - Score (correct vs total)
   - Instructions
   - Game state messages

## Tips
- Use `setTimeout()` for random delays
- Use `Date.now()` to track timestamps
- Store game state in an object
- Use different colors/classes for game states
- Add transitions for smooth color changes
- Prevent cheating (clicking before green appears)
