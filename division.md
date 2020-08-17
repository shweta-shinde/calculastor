Scenario: Second number is 0 (friendly message)
When I enter "number1"
and press "/" button
and I enter 0
Then display error message "Invalid Operation"

Scenario: Fractional division
When I enter "number1"
and press "/" button
and I enter "number2"
Then display final fractional result

Scenario: First number is 0
When I enter 0
and press "/" button
and I enter "number1"
Then display result as 0

Scenario: Denominator is greater than numerator
When I enter "number1"
and press "/" button
and I enter "number2"
Then display final fractional result

Scenario: Final result is irrational
When I enter "number1"
and press "/" button
and I enter "number2"
Then display result rounded to six decimal places

Scenario: Result exceeding limit of display
When I enter "number1"
and I press "/" button
And I enter "number2"
and I press "=" button
Then show an error message "result is out of bounds"

Scenario: Divisor is irrational (3/pi)
When I enter "number1"
and press "/" button
and I enter "number2"
Then display result rounded to six decimal places

Scenario: When both numbers are imaginary (friendly message)
When I enter imaginary "number1"
and press "/" button
and I enter imaginary "number2"
Then display error message "Invalid Operation"

Scenario: Both are zero
When I enter 0
and press "/" button
and I enter 0
Then display error message "Invalid Operation"

Scenario: Result of denominator is zero (5/(3-3))
When I enter "number1"
and press "/" button
and I enter "number3"
Then display error message "Invalid Operation"

Scenario: both dividend and divisors are non-number (friendly message)
When I enter "number1"
and press "/" button
and I enter "number3"
Then display error message "Invalid Operation"

