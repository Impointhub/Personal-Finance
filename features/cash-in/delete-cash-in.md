# Delete Cash In

## CI.2.1 – Redirect to the login page

* Given I have not logged in
* When I type `/finance/point/cash/in/1` into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (151)>)

## CI.2.2 – User can't see button delete

* Given I already logged in
* And I do not have permission to delete cash in
* When I type `/finance/point/cash/in/1` into browser
* Then I can't see button delete

![](<../../.gitbook/assets/image (152)>)

## CI.2.3 – The system displays the message "Password is required"

* Given I already logged in
* And I have permission to delete cash in
* And password account "admin123"
* And I am on the page `/finance/point/cash/in/1`
* When I click delete button

![](<../../.gitbook/assets/image (154)>)

* And I leave column password empty

![](<../../.gitbook/assets/image (156)>)

* And I click delete

![](<../../.gitbook/assets/image (158)>)

* Then I should see the message "Password is required"

![](<../../.gitbook/assets/image (159)>)

## CI.2.4 – The system displays the message "wrong password"

* Given I already logged in
* And I have permission to delete cash in
* And password account "admin123"
* And I am on the page `/finance/point/cash/in/1`
* When I click delete button

![](<../../.gitbook/assets/image (154)>)

* And I type "wrongpassword1" into column password

![](<../../.gitbook/assets/image (160)>)

* And I click delete

![](<../../.gitbook/assets/image (161)>)

* Then I should see the message "The password you entered is incorrect"

![](<../../.gitbook/assets/image (162)>)

## CI.2.5 – The system displays the message "Successfully delete"

* Given I already logged in
* And I have permission to delete cash in
* And password account "admin123"
* And I am on the page `/finance/point/cash/in/1`
* When I click delete button

![](<../../.gitbook/assets/image (154)>)

* And I type "admin123" into column password

![](<../../.gitbook/assets/image (163)>)

* And I click delete

![](<../../.gitbook/assets/image (164)>)

* Then I should see the notification "Successfully deleted"

![](<../../.gitbook/assets/image (165)>)
