# Delete- Master group chart of account

## Group-coa 3-1 Redirect to the login page

* `GIVEN` user visit `/chart-of-accounts` url without signin
* `THEN` user redirected to `Sign In` page

![](<../../.gitbook/assets/image (347)>)

## Group-coa 3-2 Redirect to the forbidden page

* Given user is logged in
* And the user does not have permission to delete a chart of accounts.
* When user type `/chart-of-accounts` url into browser
* Then user redirected to forbidden page

![](<../../.gitbook/assets/image (348)>)

## Group-coa 3-3 The system displays the message "This field is required"

* Given user is logged in
* And users have permission to delete the chart of accounts.
* And password user for the account "Admin123"!
* And user on the list page chart of account
* When user click group "101 GPR"
* And the user clicks the delete button.

![](<../../.gitbook/assets/image (349)>)

* And user leave empty password confirmation empty.

![](<../../.gitbook/assets/image (350)>)

* And user click button delete

![](<../../.gitbook/assets/image (351)>)

* Then user can view notification "Password is required".

![](<../../.gitbook/assets/image (352)>)

* And user should remain on the delete form.

![](<../../.gitbook/assets/image (353)>)

## Group-coa 3-4 Displays the message "wrong password"

* Given user is logged in
* And users have permission to delete the chart of accounts.
* And password user for the account "Admin123"!
* And user on the list page chart of account
* When user click group "101 GPR"
* And the user clicks the delete button.

![](<../../.gitbook/assets/image (349)>)

* And user type "Admin12" into column

![](<../../.gitbook/assets/image (354)>)

* And user click button delete

![](<../../.gitbook/assets/image (355)>)

* Then user can view the notification "wrong password"

![](<../../.gitbook/assets/image (356)>)

* And user should remain on the delete form.

![](<../../.gitbook/assets/image (357)>)

## Group-coa 3-5. Group data will be deleted

* Given user is logged in
* And users have permission to delete the chart of accounts.
* And password user for the account "Admin123"!
* And user on the list page chart of account
* When user click group "101 GPR"
* And the user clicks the delete button.

![](<../../.gitbook/assets/image (358)>)

* And user type "Admin123" into the column.

![](<../../.gitbook/assets/image (359)>)

* And user click button delete

![](<../../.gitbook/assets/image (360)>)

* Then I can view notification "successfully deleted "

![](<../../.gitbook/assets/image (361)>)

* And subgroup within this group will be move to the parent level
