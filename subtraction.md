# Subtraction

Scenario: Subtract two numbers
Given I have a calculator that's turned on

When I enter "number1"
And I press "-" button
And I enter "number2"
And I press "=" button
Then I see the final result

Scenario: overrunning the limits(negative or positive)
When I enter "number1"
And I press "-" button
And I enter "number2"
When I press "=" button
Then I see an error stating the result is out of bounds

Scenario: Both Numbers can be negative
When I press "-" and enter "number1"
And I press "-" button
And I  press "-" and  enter "number2"
And I press "=" button
Then Subtract "number2" from "number2"

Scenario : Subtraction of a-(-b)
Given The calculator is on
When I enter a "number1"
and press "-" button
and press "-" and enter "number2"
and press "=" button
Then the result must show addition considering the numbers positive

Scenario: Numbers can be fraction
When I enter "number1" as fractional number
And I press "-" button
When I enter "number2" as fractional number
And I press "=" button
Then I get a result rounded to an appropriate decimal place

Scenario: Number can be irrational
When I enter "number1" as irrational number
And I press "-" button
When I enter "number2" as irrational number
And I press "=" button
Then consider first six digits after decimal of each number for subtraction

Scenario: Length of each number
When I enter "number1"
And I press "-" button
And I enter "number2"
When I press "=" button
Then I see an error stating the numbers are out of bounds

Scenario: If number1 or number2 is not entered
When I enter "number1"
And I press "-" button
And I press "=" button
Then Display an error stating missing operand

Scenario: If the number is complex
When I enter "number1"
And I press "-" button
And I enter "number2"
When I press "=" button
Then I see an error stating the numbers should be real

Scenario: If we are between some operation
When I enter "number1"
And I press "-" button
And I enter "number2"
When I press "=" button
Then I see an error "another operation in progress"
