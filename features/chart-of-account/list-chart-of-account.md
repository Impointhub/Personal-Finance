# List Chart of Account

### COA4.1 redirect to the login page

* Given user visit `/chart-of-accounts` url without signin
* Then user redirected to `Sign In` page

![](<../../.gitbook/assets/image (247)>)

### COA4.2 redirect to the forbidden page - _Ref : Clone ERP_

* Given user is logged in

![](<../../.gitbook/assets/image (247)>)

* And user dont have permission to read a chart of accounts.
* When user type `/chart-of-accounts` url into browser
* Then user redirected to forbidden page

![](<../../.gitbook/assets/image (248)>)

### COA4.3 displays the message "you don't have any data yet"

* Given user is logged in

![](<../../.gitbook/assets/image (247)>)

* And user have permission to read chart of accounts.
* And user don't have data chart of accounts.
* Then user can view data notification "you don't have any data yet."

![](<../../.gitbook/assets/image (250)>)

### COA4.4.Displays all chart of accounts data that has been entered.

* Given user is logged in

![](<../../.gitbook/assets/image (247)>)

* And user have permission to read chart of accounts.
* And user have data chart account
* Then user can view all chart of account data that has been entered

![](<../../.gitbook/assets/image (253)>)

* And chart of account data sort based on account number

![](<../../.gitbook/assets/image (255)>)
