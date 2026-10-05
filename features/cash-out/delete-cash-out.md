# Delete Cash Out

## DLB.1 : User redirect to login page

* Given I have not logged in
* When I type /finance/point/cash/out/1 into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (410)>)

## DLB.2 : Cannot see delete button

* Given I already logged in
* And I do not have permission to delete cash out
* And I am on the page /finance/point/cash/out/1
* Then I should not see the delete button"

![](<../../.gitbook/assets/image (411)>)

## DLB.3 : Display message password required

* Given I already logged in
* And I have permission to delete cash out
* And I am on the page /finance/point/cash/out/1
* When I click delete button

![](<../../.gitbook/assets/image (412)>)

* And I leave column password empty

![](<../../.gitbook/assets/image (413)>)

* And I click delete

![](<../../.gitbook/assets/image (414)>)

* Then I should see the message ""Password is required"

![](<../../.gitbook/assets/image (415)>)

## DLB.4 : Send notification wrong password

* Given I already logged in
* And I have permission to delete cash out
* And I am on the page /finance/cash/out/1
* When I click delete button

![](<../../.gitbook/assets/image (412)>)

* And I type "wrongpassword1" into column password

![](<../../.gitbook/assets/image (416)>)

* And I click delete

![](<../../.gitbook/assets/image (414)>)

* Then I should see the message "The password you entered is incorrect"

![](<../../.gitbook/assets/image (417)>)

## DLB.5 : Display notification successfully deleted

* Given I already logged in
* And I have permission to delete cash out
* And I am on the page /finance/point/cash/out/1
* When I click delete button

![](<../../.gitbook/assets/image (412)>)

* And I type "admin123" into column password

![](<../../.gitbook/assets/image (418)>)

* And I click delete

![](<../../.gitbook/assets/image (419)>)

* Then I should see the notification "Successfully deleted"

![](<../../.gitbook/assets/image (420)>)
