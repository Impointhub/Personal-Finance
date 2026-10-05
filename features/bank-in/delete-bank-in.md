# Delete Bank In

## BI.2.1 – Redirect to the login page when user is not logged in

* Given I have not logged in
* When I type https://test.app.point.red/finance/point/bank into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (88)>)

## BI.2.2 – Redirect to the forbidden page when user does not have permission to delete Bank In

* Given I already logged in
* And I do not have permission to delete bank out
* When I type https://test.app.point.red/finance/point/bank/1 into browser
* Then I can't see button delete

![](<../../.gitbook/assets/image (90)>)

## BI.2.3 – The system displays the message "Password is required"

* Given I already logged in
* And I have permission to delete bank out
* And I am on the page https://test.app.point.red/finance/point/bank/out/1
* When I click delete button

![](<../../.gitbook/assets/image (91)>)

* And I leave column password empty

![](<../../.gitbook/assets/image (93)>)

* And I click delete

![](<../../.gitbook/assets/image (95)>)

* Then I should see the message ""Password is required"

![](<../../.gitbook/assets/image (97)>)

## BI.2.4 – The system displays the message "wrong password"

* Given I already logged in
* And I have permission to delete bank in
* And I am on the page https://test.app.point.red/finance/point/bank/inn/1
* When I click delete button

![](<../../.gitbook/assets/image (91)>)

* And I type "wrongpassword1" into column password

![](<../../.gitbook/assets/image (99)>)

* And I click delete

![](<../../.gitbook/assets/image (101)>)

* Then I should see the message "The password you entered is incorrect"

![](<../../.gitbook/assets/image (103)>)

## BI.2.5 – The system displays the message "Successfully delete"

* Given I already logged in
* And I have permission to delete bank out
* And I am on the page https://test.app.point.red/finance/point/bank/out/1
* When I click delete button

![](<../../.gitbook/assets/image (91)>)

* And I type "admin123" into column password

![](<../../.gitbook/assets/image (99)>)

* And I click delete

![](<../../.gitbook/assets/image (93)>)

* Then I should see the notification "Successfully deleted"

![](<../../.gitbook/assets/image (105)>)
