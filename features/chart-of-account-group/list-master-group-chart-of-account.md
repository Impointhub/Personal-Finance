# List Master group chart of account

## Group-COA 4.1 Redirect to the login page

* `GIVEN` user visit `/chart-of-accounts` url without signin
* `THEN` user redirected to `Sign In` page

![](<../../.gitbook/assets/image (343)>)

## Group-COA 4.2 Redirect to the forbidden page

* Given user is logged in
* And the user does not have permission to group a chart of accounts.
* When user type `/chart-of-accounts` url into browser
* Then user redirected to forbidden page

![](<../../.gitbook/assets/image (344)>)

## Group-COA.4-3 displays the message "you don't have any data yet."

* Given user is logged in
* And the user has permission to read the chart of accounts.
* And users don't have data chart of accounts.
* Then the user can view the data notification "You don't have any data yet."

![](<../../.gitbook/assets/image (345)>)

## Group-COA-4.4. Displays all group chart of accounts data that have been entered.

* Given user is logged in
* And the user has permission to read the chart of accounts.
* And users have group chart of account
* Then the user can view the data have been entered

![](<../../.gitbook/assets/image (346)>)
