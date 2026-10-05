# Create chart of account

### _COA1.1 redirect to the login page_

* Given user visit `/chart-of-accounts` url without signin
* Then user redirected to `Sign In` page

![](<../../.gitbook/assets/image (234)>)

### COA1.2 redirect to the forbidden page

* Given user is logged in

![](<../../.gitbook/assets/image (234)>)

* And the user does not have permission to create a chart of accounts.
* When user type `/chart-of-accounts` url into browser
* Then user redirected to forbidden page

![](/broken/files/2ae003f5727b1e448598ebecfe4deb5eaf3de5be)

### _COA1.3. The system displays the message "This field is required"_

* Given User is logged in
* And user have permission "create\_chart\_of\_account"
* And the user on the list page chart of account

![](<../../.gitbook/assets/image (235)>)

* When user click "Create COA"

![](<../../.gitbook/assets/image (236)>)

* And user leave empty column "Main category"

![](<../../.gitbook/assets/image (237)>)

* And user leave empty column "Major group"

![](<../../.gitbook/assets/image (238)>)

* And user type "1000-01" into column "Account number"

![](<../../.gitbook/assets/image (239)>)

* And user leave empty column "Account Name"

![](<../../.gitbook/assets/image (240)>)

* And user leave empty column "Balance Normal"

![](<../../.gitbook/assets/image (241)>)

* And user click save COA

![](<../../.gitbook/assets/image (242)>)

* Then user can view notification "Unable to save record, Please correct the errors highlighted below"

![](<../../.gitbook/assets/image (243)>)

### COA1.4 The system displays the message "account number already exists"

* Given the user is logged in

![](<../../.gitbook/assets/image (234)>)

* And user have permission "create\_chart\_of\_account"
* And user have data account number "1000-01"
* And the user on the list page chart of account

![](<../../.gitbook/assets/image (244)>)

* When user click "Create COA"

![](<../../.gitbook/assets/image (236)>)

* And user click choosen main category "Asset"

![](<../../.gitbook/assets/image (245)>)

* And user click choosen major group "Current Asset"

![](<../../.gitbook/assets/image (246)>)

* And user type "1000-01" into column Account number

![](<../../.gitbook/assets/image (249)>)

* And user type "piutang usaha" into column Account name

![](<../../.gitbook/assets/image (251)>)

* And user click choosen balance normal "Debit"

![](<../../.gitbook/assets/image (252)>)

* And user click choose cashflow category "operating"

![](<../../.gitbook/assets/image (254)>)

* And column "is cash account" disable

![](<../../.gitbook/assets/image (256)>)

* And user click "save coa"

![](<../../.gitbook/assets/image (257)>)

* Then user can view error message "Unable to save record. please correct the errors highlighted below."

![](<../../.gitbook/assets/image (258)>)

### COA1.5. The system displays the message "Successfully created"

* Given the user is logged in

![](<../../.gitbook/assets/image (234)>)

* And user have permission "create\_chart\_of\_account"
* And the user on the list page chart of account

![](<../../.gitbook/assets/image (259)>)

* When user click "Create COA"

![](<../../.gitbook/assets/image (236)>)

* And user click choosen main category "Asset"

![](<../../.gitbook/assets/image (245)>)

* And user click choosen major group "Current Asset"

![](<../../.gitbook/assets/image (238)>)

* And user type "1000-02" into column Account number.

![](<../../.gitbook/assets/image (239)>)

* And user type "piutang usaha" into the column "Account name".

![](<../../.gitbook/assets/image (251)>)

* And user click choosen balance normal "Debit".

![](<../../.gitbook/assets/image (241)>)

* And user click choosen cashflow category "operating"

![](<../../.gitbook/assets/image (254)>)

* And column "is cash account" disable

![](<../../.gitbook/assets/image (260)>)

* And user click "save COA".

![](<../../.gitbook/assets/image (257)>)

* Then user can view notification "Success create chart of account"

![](<../../.gitbook/assets/image (261)>)

* And user redirect to list page.

![](<../../.gitbook/assets/image (262)>)
