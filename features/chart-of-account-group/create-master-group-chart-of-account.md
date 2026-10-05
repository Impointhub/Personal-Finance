# Create- Master group chart of account

### Group-COA-1.1 : Create- Master group chart of account redirect to the login page

* `GIVEN` user visit `/chart-of-accounts` url without signin
* `THEN` user redirected to `Sign In` page

![](<../../.gitbook/assets/image (321)>)

### Group-COA-1.2 : redirect to the forbidden page

* Given user is logged in
* And the user does not have permission to create a chart of accounts.
* When user type `/chart-of-accounts` url into browser
* Then user redirected to forbidden page

![](<../../.gitbook/assets/image (322)>)

### Group-COA-1.3 : The system displays the message "{Column\_name} is required"

* Given user is logged in
* And user have permission "create\_chart\_of\_account"
* And the user on the list page chart of account
* And user already have major group "current asset"
* And user already have parent group "Cash and Bank"
* When the user click button (+) on folder icon
* And user leave empty column group code
* And user leave empty column group name
* And user click button "save"
* Then user can view the notification "{column\_name} is required".

![](<../../.gitbook/assets/image (323)>)

### Group-COA-1.4: The system displays the message "Group already exists"

* Given user is logged in
* And user have permission "create\_chart\_of\_account"
* And the user on the list page chart of account
* And user already have major group "current asset"
* And user already have parent group "Cash and Bank"
* And user already have folder with code "101"
* When the user click button (+) on folder icon
* And user type "101" into column "Group code"
* And user type "Ganesha park residence" into column "Group Name"
* And user click button "save"
* Then user can view the notification "{column\_name} is already exist"

![](<../../.gitbook/assets/image (324)>)

### Group-COA-1.5 : The system displays the message "Successfully created group"

* Given user is logged in
* And user have permission "create\_chart\_of\_account"
* And the user on the list page chart of account
* And user already have major group "current asset"
* And user already have parent group "Cash and Bank"
* And user already have folder with code "101"
* When the user click button (+) on folder icon
* And user type "101" into column "Group code"
* And user type "Ganesha park residence" into column "Group Name"
* And user click button "save"

![](<../../.gitbook/assets/image (325)>)

* Then user can view the notification "Successfully created"

![](<../../.gitbook/assets/image (326)>)

* And user redirect to list page group chart of account

![](<../../.gitbook/assets/image (327)>)
