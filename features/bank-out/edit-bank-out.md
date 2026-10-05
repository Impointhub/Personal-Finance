# Edit Bank Out

## EB.F1 - Redirect to login page because user unauthenticated

* Given I have not logged in
* When I type https://test.app.point.red/finance/point/bankout/1 into browser
* Then I should be redirected to the login page

## EB.F2 - Redirect to the forbidden page because user don't have permission edit\_bank out

* Given I already logged in
* And I do not have permission to edit bank out
* When I open the page https://test.app.point.red/finance/point/bankout/1
* Then I should not see the "Edit" button

## EB.F3 - The system displays the message "bank account is required" because the user didn't enter a bank account

{% stepper %}
{% step %}
### Open the edit form

* Given I already logged in
* And I have permission to edit bank out
* And I am on the page https://test.app.point.red/finance/point/bankout/1
* When I click "Edit" button
{% endstep %}

{% step %}
### Verify the prefilled and accessible account data

* And the form is prefilled with the existing bank out data
* And the columns bank account and account display only the charts of accounts accessible to me
{% endstep %}

{% step %}
### Submit without a bank account

* And I clear column bank account
* And I click submit
* Then I should see the message "Bank account is required"
* And I should remain on the edit page
{% endstep %}
{% endstepper %}

## EB.F4 - The system displays the message "Payment to is required" because the user didn't enter a payment to

{% stepper %}
{% step %}
### Open the edit form

* Given I already logged in
* And I have permission to edit bank out
* And I am on the page https://test.app.point.red/finance/point/bankout/1
* When I click "Edit" button
{% endstep %}

{% step %}
### Verify the prefilled and accessible account data

* And the form is prefilled with the existing bank out data
* And the columns bank account and account display only the charts of accounts accessible to me
{% endstep %}

{% step %}
### Submit without a payment recipient

* And I clear column payment to
* And I click submit
* Then I should see the message "Payment to is required"
* And I should remain on the edit page
{% endstep %}
{% endstepper %}

## EB.F5 - The system displays the message "account is required" because the user didn't enter an account

{% stepper %}
{% step %}
### Open the edit form

* Given I already logged in
* And I have permission to edit bank out
* And I am on the page https://test.app.point.red/finance/point/bankout/1
* When I click "Edit" button
{% endstep %}

{% step %}
### Verify the prefilled and accessible account data

* And the form is prefilled with the existing bank out data
* And the columns bank account and account display only the charts of accounts accessible to me
{% endstep %}

{% step %}
### Submit without an account

* And I clear column account on the first row
* And I click submit
* Then I should see the message "Account is required"
* And I should remain on the edit page
{% endstep %}
{% endstepper %}

## EB.F6 - The system displays the message "amount is required" because the user didn't enter an amount

{% stepper %}
{% step %}
### Open the edit form

* Given I already logged in
* And I have permission to edit bank out
* And I am on the page https://test.app.point.red/finance/point/bankout/1
* When I click "Edit" button
{% endstep %}

{% step %}
### Verify the prefilled and accessible account data

* And the form is prefilled with the existing bank out data
* And the columns bank account and account display only the charts of accounts accessible to me
{% endstep %}

{% step %}
### Submit without an amount

* And I clear column amount on the first row
* And I click submit
* Then I should see the message "Amount is required"
* And I should remain on the edit page
{% endstep %}
{% endstepper %}

## EB.F7 - The system displays the message "Please enter a valid amount using numbers only." because the user didn't enter an valid amount

{% stepper %}
{% step %}
### Open the edit form

* Given I already logged in
* And I have permission to edit bank out
* And I am on the page https://test.app.point.red/finance/point/bankout/1
* When I click "Edit" button
{% endstep %}

{% step %}
### Verify the prefilled and accessible account data

* And the form is prefilled with the existing bank out data
* And the columns bank account and account display only the charts of accounts accessible to me
{% endstep %}

{% step %}
### Submit an invalid amount

* And I type "abc" into column amount on the first row
* And I click submit
* Then I should see the message "Please enter a valid amount using numbers only"
* And I should remain on the edit page
{% endstep %}
{% endstepper %}

## EB.F8 - The system displays the message "Amount must be greater than zero." because the user didn't enter an amount greater than zero

{% stepper %}
{% step %}
### Open the edit form

* Given I already logged in
* And I have permission to edit bank out
* And I am on the page https://test.app.point.red/finance/point/bankout/1
* When I click "Edit" button
{% endstep %}

{% step %}
### Verify the prefilled and accessible account data

* And the form is prefilled with the existing bank out data
* And the columns bank account and account display only the charts of accounts accessible to me
{% endstep %}

{% step %}
### Submit a zero amount

* And I type "0" into column amount on the first row
* And I click submit
* Then I should see the message "Amount must be greater than zero"
* And I should remain on the edit page
{% endstep %}
{% endstepper %}

## EB.S1 : The system displays the message "Successfully updated"

{% stepper %}
{% step %}
### Open the edit form

* Given I already logged in
* And I have permission to edit bank out
* And I am on the page https://test.app.point.red/finance/point/bankout/1
* When I click "Edit" button
{% endstep %}

{% step %}
### Verify the prefilled and accessible account data

* And the form is prefilled with the existing bank out data
* And the columns bank account and account display only the charts of accounts accessible to me
{% endstep %}

{% step %}
### Update the bank out

* And I type "Edit testing" into column notes on the first row
* And I type "150000" into column amount on the first row
* And I click submit
* Then I should see the notification "Successfully updated"
* And I should be redirected to the bank out detail page
{% endstep %}
{% endstepper %}
