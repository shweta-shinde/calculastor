# Multiply

Scenario: Result overflow
When I enter "number1"
and I press "*" button
And I enter "number2"
and I press "=" button
Then show an error message stating the final result is out of bounds

Scenario: One number is negative
When I press "-" and enter "number1"
and I press "*" button
And I enter "number2"
and I press "=" button
Then give the final result of multiplication with a negative sign

Scenario: Both numbers are negative
When I press "-" and enter "number1"
and I press "*" button
And I press "-" and enter "number2"
and I press "=" button
Then give the final result of multiplication with a positive sign

Scenario: One or both numbers are zero
When I enter "number1"
and I press "*" button
And I enter "number2"
and I press "=" button
Then the final result is zero

Scenario: Decimal value multiplication
When I enter "number1" as decimal number
and I press "*" button
And I enter "number2" as decimal number
and I press "=" button
Then Display result by placing the decimal sign at appropriate place

Scenario: Irrational value multiplication
When I enter "number1" as irrational number
and I press "*" button
And I enter "number2" as irrational number
and I press "=" button
Then Display result considering first six digit after decimal point

Scenario: Simple multiplication
When I enter "number1"
and I press "*" button
And I enter "number2"
and I press "=" button
Then display final result of multiplication

Scenario: Rational multiplication
Scenario: Decimal & integer multiplication
When I enter "number1" as decimal number
and I press "*" button
And I enter "number2" as integer number
and I press "=" button
Then Display result by placing the decimal sign at appropriate place

Scenario: More than two numbers multiplication
When I enter "number1"
And I press "*" button
And I enter "number2"
And I press "*" button
And so on till "numbern"
And I press "=" button
Then I see the multiplication of all given numbers as the result

Scenario: Range of operand exceeds allowed limit
When I enter "number1"
and I press "*" button
And I enter "number2"
and I press "=" button
Then show an error message "input is out of bounds"

Scenario: Pressing "multiply button" more than once
When I enter "number1"
and I press "*" button more than once
And I enter "number2"
and I press "=" button
Then show an error message "invalid operation"

Scenario: Interleaving operators (Press *, then press /, then press +)
When I enter "number1"
and I press "*" button
and I enter other operators
And I enter "number2"
and I press "=" button
Then show an error message "invalid operation"

Scenario: Decimal value capping
When I enter "number1"
and I press "*" button
And I enter "number2"
and I press "=" button
Then Round the final result of multiplication to six decimal places
