# calculator

## Append to Display

When a user clicks on a button (e.g. "7", "+", etc.), the appendToDisplay function is called with the value of the button as an argument. This function simply appends the value to the current value of the display input element using the += operator.

### Example

If the current value of the display is "12" and the user clicks on the "3" button, the appendToDisplay function will append "3" to the display value, making it "123".

## Clear Display

When the user clicks on the "C" button, the clearDisplay function is called, which simply sets the value of the display input element to an empty string ("").

## Calculate

When the user clicks on the "=" button, the calculate function is called. This function uses the eval function to evaluate the current value of the display as a mathematical expression.

## Step-by-Step Process

1. The eval function takes the current value of the display as a string (e.g. "12+3\*4").
2. It parses the string as a mathematical expression, using the JavaScript syntax rules.
3. It evaluates the expression, performing the necessary calculations (e.g. multiplying 3 and 4, then adding 12).
4. The result of the evaluation is returned as a number (e.g. 24).
5. The calculate function sets the value of the display input element to the result of the evaluation (e.g. "24").

## Important Note

The eval function can pose a security risk if used with untrusted input, since it can evaluate arbitrary JavaScript code. However, in this case, the input is coming from the user's interactions with the calculator, so it's relatively safe.

## Error Handling

If the user enters an invalid mathematical expression (e.g. "12+3\*"), the eval function will throw a SyntaxError. The calculate function catches this error and sets the value of the display input element to "Error".

