# Edit Chart of Account

### COA2.1 redirect to the login page - _Ref : Clone ERP_

* Given user visit `/chart-of-accounts` url without signin
* Then user redirected to `Sign In` page

![](<../../.gitbook/assets/image (277)>)

### COA2.2 redirect to the forbidden page - _Ref : Clone ERP_

* Given user is logged in

![](<../../.gitbook/assets/image (277)>)

* And the user does not have permission to edit a chart of accounts.
* When user type `/chart-of-accounts` url into browser
* Then user redirected to forbidden page

![](<../../.gitbook/assets/image (279)>)

### COA2.3.Displaying notification "can't edit, chart of accounts already has references"

* Given the user is logged in

![](<../../.gitbook/assets/image (277)>)

* And user have permission "edit\_chart\_of\_account"
* And the user on the list page chart of account

![](<../../.gitbook/assets/image (281)>)

* And account 1000-01 already has a reference.
* And the user clicks the account number "1000-01"

![](<../../.gitbook/assets/image (283)>)

* And user click button update

![](<../../.gitbook/assets/image (285)>)

* Then user can view notification "Failed Update, Unable to edit this Chart of Account because it is already referenced by existing transactions or configurations."

![](<../../.gitbook/assets/image (287)>)

### COA2.4 The system displays the message "This field is required"

* Given user is logged in

![](<../../.gitbook/assets/image (277)>)

* And user have permission "edit\_chart\_of\_account"
* And user on the list page chart of account

![](<../../.gitbook/assets/image (289)>)

* When user click account number "1000-02"

![](<../../.gitbook/assets/image (283)>)

* And user click button update

![](<../../.gitbook/assets/image (285)>)

* And user leave empty column "main category"

![](<../../.gitbook/assets/image (290)>)

* And user leave empty column "major group"

![](<../../.gitbook/assets/image (292)>)

* And user type "1000-02" into column account number

![](<../../.gitbook/assets/image (294)>)

* And user leave empty column "Account name"

![](<../../.gitbook/assets/image (295)>)

* And user leave empty column "balance normal"

![](<../../.gitbook/assets/image (296)>)

* And user leave empty column "cashflow category"

![](<../../.gitbook/assets/image (298)>)

* And user toggle checkbox "is cash account"

![](<../../.gitbook/assets/image (299)>)

* And user click save coa

![](<../../.gitbook/assets/image (300)>)

* Then I can view "Unable to save record, Please correct the errors highlighted below"

### COA2.5 The system displays the message "account number already exists"

* Given user is logged in

![](<../../.gitbook/assets/image (277)>)

* And user have permission "edit\_chart\_of\_account"
* And user on the list page chart of account

![](<../../.gitbook/assets/image (301)>)

* When user click account number "1000-02"

![](<../../.gitbook/assets/image (283)>)

* And user click button update

![](<../../.gitbook/assets/image (302)>)

* And I choosen main category "Asset".

![](<../../.gitbook/assets/image (303)>)

* And I choosen major group "Current Asset"

![](<../../.gitbook/assets/image (304)>)

* And I type "1000-01" into column "Account Number"

![](<../../.gitbook/assets/image (305)>)

* And I type "Sewa Dibayar Dimuka" into column "Account Name"

![](<../../.gitbook/assets/image (306)>)

* And I choosen balance normal "Debit"

![](<../../.gitbook/assets/image (307)>)

* And I choosen cashflow category "operating"

![](<../../.gitbook/assets/image (308)>)

* And Cash account disable

![](<../../.gitbook/assets/image (309)>)

* And I click save coa

![](<../../.gitbook/assets/image (310)>)

* Then I should view notification "Unable to save record, Please correct the errors highlighted below"

![](<../../.gitbook/assets/image (311)>)

### COA2.6.The system displays the message "Successfully updated"

* Given user is logged in

![](<../../.gitbook/assets/image (277)>)

* And user have permission "edit\_chart\_of\_account"
* And user on the list page chart of account

![](<../../.gitbook/assets/image (312)>)

* When user click account number "1000-02"

![](<../../.gitbook/assets/image (283)>)

* And user click button update

![](<../../.gitbook/assets/image (313)>)

* And I choosen main category "Asset".

![](<../../.gitbook/assets/image (303)>)

* And I choosen major group "Current Asset"

![](<../../.gitbook/assets/image (304)>)

* And I type "1000-02" into column "Account Number"

![](<../../.gitbook/assets/image (314)>)

* And I type "Sewa Dibayar Dimuka" into column "Account Name"

![](<../../.gitbook/assets/image (315)>)

* And I choosen balance normal "Debit"

![](<../../.gitbook/assets/image (316)>)

* And I choosen cashflow category "operating"

![](<../../.gitbook/assets/image (317)>)

* And Cash account disable

![](<../../.gitbook/assets/image (318)>)

* And I click save coa

![](<../../.gitbook/assets/image (319)>)

* Then I should view notification "Success update chart of account"

![](<../../.gitbook/assets/image (320)>)

* And I redirect to list page
