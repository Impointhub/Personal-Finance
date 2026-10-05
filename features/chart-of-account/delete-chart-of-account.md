# Delete Chart of Account

### COA3.1 redirect to the login page - _Ref : Clone ERP_

* Given user visit `/chart-of-accounts` url without signin
* Then user redirected to `Sign In` page

![](<../../.gitbook/assets/image (265)>)

### COA3.2 redirect to the forbidden page - _Ref : Clone ERP_

* Given user is logged in

![](<../../.gitbook/assets/image (265)>)

* And user does not have permission to delete a chart of accounts.
* When user type `/chart-of-accounts` url into browser
* Then user redirected to forbidden page

![](<../../.gitbook/assets/image (267)>)

### COA3.3.Displaying notification "can't delete, chart of accounts already has references"

* Given user is logged in

![](<../../.gitbook/assets/image (265)>)

* And user have permission delete the chart of account
* And user on the list page chart of account

![](<../../.gitbook/assets/image (269)>)

* When user click account number "1000-02"

![](<../../.gitbook/assets/image (271)>)

* And user click button "delete"

![](<../../.gitbook/assets/image (272)>)

* Then user can view notification "Failed Delete, Unable to edit this Chart of Account because it is already referenced by existing transactions or configurations."

![](<../../.gitbook/assets/image (273)>)

### COA3.4 The system displays the message "This field is required" - _Ref : Clone ERP_

* Given user is logged in

![](<../../.gitbook/assets/image (265)>)

* And user have permission delete the chart of accounts.
* And user on the list page chart of account

![](<../../.gitbook/assets/image (274)>)

* When user click account number "1000-02"

![](<../../.gitbook/assets/image (271)>)

* And user click button "delete".

![](<../../.gitbook/assets/image (275)>)

* And user leave empty column "password"

![](<../../.gitbook/assets/image (276)>)

* And click button delete

![](<../../.gitbook/assets/image (278)>)

* Then I can view notification "password is required"

![](<../../.gitbook/assets/image (280)>)

### COA3.5 Displays a wrong password notification

* Given user is logged in

![](<../../.gitbook/assets/image (265)>)

* And user have permission to delete the chart of accounts.
* And password user for the account "Admin123!"
* And user on the list page chart of account

![](<../../.gitbook/assets/image (282)>)

* When user click account number "1000-02"

![](<../../.gitbook/assets/image (271)>)

* And user click button "delete".

![](<../../.gitbook/assets/image (272)>)

* And user type "Admin" into column password

![](<../../.gitbook/assets/image (284)>)

* And click button delete

![](<../../.gitbook/assets/image (286)>)

* Then I can view notification "wrong password"

![](<../../.gitbook/assets/image (288)>)

### COA3.6.The system displays the message "Successfully deleted"

* Given user is logged in

![](<../../.gitbook/assets/image (265)>)

* And user have permission to delete the chart of accounts.
* And password user for the account "Admin123!"
* And user on the list page chart of account

![](<../../.gitbook/assets/image (291)>)

* When user click account number "1000-02"

![](<../../.gitbook/assets/image (271)>)

* And user click button "delete".

![](<../../.gitbook/assets/image (275)>)

* And user type "Admin123!" into column password

![](<../../.gitbook/assets/image (293)>)

* And click button delete

![](<../../.gitbook/assets/image (286)>)

* Then I can view notification "Success Delete chart of account"

![](<../../.gitbook/assets/image (297)>)
