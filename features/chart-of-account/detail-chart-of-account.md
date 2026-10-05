# Detail Chart of Account

### COA5.1 redirect to the login page - _Ref : Clone ERP_

* Given user visit `/chart-of-accounts` url without signin
* Then user redirected to `Sign In` page

![](<../../.gitbook/assets/image (263)>)

### COA5.2 redirect to the forbidden page - _Ref : Clone ERP_

* Given user is logged in

![](<../../.gitbook/assets/image (263)>)

* And user dont have permission to read a chart of accounts.
* When user type `/chart-of-accounts` url into browser
* Then user redirected to forbidden page

![](<../../.gitbook/assets/image (264)>)

### COA5.3.Displays detail chart of account - _Ref : Clone ERP_

* Given user is logged in

![](<../../.gitbook/assets/image (263)>)

* And user have permission to read a chart of accounts.
* And user on the list page chart of accounts

![](<../../.gitbook/assets/image (266)>)

* And user have account number "1000-02"

![](<../../.gitbook/assets/image (268)>)

* When user click "1000-02" on the column number

![](<../../.gitbook/assets/image (268)>)

* Then user can view detail page chart of account

![](<../../.gitbook/assets/image (270)>)
