# Delete Bank Out

## DLB.1 : User redirect to login page

* Given I have not logged in
* When I type https://test.app.point.red/finance/point/bank/out/1 into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (33)>)

## DLB.2 : Cannot see delete button

* Given I already logged in
* And I do not have permission to delete bank out
* And I am on the page https://test.app.point.red/finance/point/bank/out/1
* Then I should not see the delete button"

![](<../../.gitbook/assets/image (34)>)

## DLB.3 : Display message password is required

* Given I already logged in
* And I have permission to delete bank out
* And I am on the page https://test.app.point.red/finance/point/bank/out/1
* When I click delete button

![](<../../.gitbook/assets/image (35)>)

* And I leave column password empty

![](<../../.gitbook/assets/image (36)>)

* And I click delete

![](<../../.gitbook/assets/image (37)>)

* Then I should see the message ""Password is required"

![](<../../.gitbook/assets/image (38)>)

## DLB.4 : Send notification wrong password

* Given I already logged in
* And I have permission to delete bank out
* And I am on the page https://test.app.point.red/finance/point/bank/out/1
* When I click delete button

![](<../../.gitbook/assets/image (35)>)

* And I type "wrongpassword1" into column password

![](<../../.gitbook/assets/image (39)>)

* And I click delete

![](<../../.gitbook/assets/image (37)>)

* Then I should see the message "The password you entered is incorrect"

![](<../../.gitbook/assets/image (40)>)

## DLB.5 : Display notification successfully deleted

* Given I already logged in
* And I have permission to delete bank out
* And I am on the page https://test.app.point.red/finance/point/bank/out/1
* When I click delete button

![](<../../.gitbook/assets/image (35)>)

* And I type "admin123" into column password

![](<../../.gitbook/assets/image (41)>)

* And I click delete

![](<../../.gitbook/assets/image (42)>)

* Then I should see the notification "Successfully deleted"

![](<../../.gitbook/assets/image (43)>)
