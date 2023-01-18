# Best Practices and Tips

When writing scripts for FiveM, it's important to keep in mind some best practices and tips to make sure that your code is clean, readable, and efficient.

## Naming Conventions
It's important to use clear and consistent names for variables, functions, and events. Avoid using abbreviations or single letters, and use camelCase or snake_case depending on your preference.
```lua
-- Good naming
local playerHealth = 100
function checkPlayerHealth()
  -- code
end

-- Bad naming
local plH = 100
function chkPlH()
  -- code
end
```

## Commenting your Code
It's a good practice to leave comments in your code to explain what certain parts of your script do. This makes it easier for other developers to understand and maintain your code.

```lua
-- Commenting your code
function checkPlayerHealth()
  -- Check if player's health is below a certain threshold
  if playerHealth < 50 then
    -- Trigger an event to alert the player
    TriggerEvent("playerLowHealth")
  end
end
```

## Organizing your Code
It's important to organize your code into functions, so that it's easier to read, debug, and maintain. Try to keep each function focused on a specific task and avoid too much nesting or long functions.

```lua
-- Organizing your code
function checkPlayerHealth()
  -- Check if player's health is below a certain threshold
  if playerHealth < 50 then
    -- Trigger an event to alert the player
    TriggerEvent("playerLowHealth")
  end
end

function displayHealthWarning()
    -- Display a warning message to the player
    exports.myUI:showAlert("Your health is low!", "warning")
end

AddEventHandler("playerLowHealth", displayHealthWarning)
```

## Avoiding Global Variables
It's best practice to avoid using global variables as much as possible, as they can cause conflicts and make it harder to track where a variable is being used. Instead, use local variables and pass them as arguments to functions.
```lua
-- Avoiding global variables
local playerHealth = 100

function checkPlayerHealth(health)
  -- Check if player's health is below a certain threshold
  if health < 50 then
    -- Trigger an event to alert the player
    TriggerEvent("playerLowHealth")
  end
end

checkPlayerHealth(playerHealth)
```

## Error Handling
It's important to handle errors in your script to prevent it from crashing or breaking. Use the pcall function to catch errors, and use the error function to display a message to the user.

```lua
-- Error handling
local success, error = pcall(functionThatMightError)
if not success then
  error("An error occurred: " .. error)
end
```
## Performance Optimization
Performance is an important aspect when developing scripts for FiveM. Here are a few tips to keep in mind:
- Try to avoid using loops where possible, especially when working with large data sets.
- Use the appropriate data types for variables and try to avoid unnecessary type conversions.
- Avoid using too many nested if-else statements, as they can affect the performance of your script.

By following these best practices and tips, you can ensure that your scripts are well-organized, efficient, and easy to maintain. It's important to keep in mind that these are general guidelines and there may be exceptions to them. However, following these guidelines will help you to write clean, readable, and effective code.