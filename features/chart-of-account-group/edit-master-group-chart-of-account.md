# Edit- Master group chart of account

## Group-COA 2.1 - redirect to the login page

* `GIVEN` user visit `/chart-of-accounts` url without signin
* `THEN` user redirected to `Sign In` page

![](<../../.gitbook/assets/image (328)>)

## Group-COA 2.2 - redirect to the forbidden page

* Given user is logged in
* And the user does not have permission to edit a chart of accounts.
* When user type `/chart-of-accounts` url into browser
* Then user redirected to forbidden page

![](<../../.gitbook/assets/image (329)>)

## Group-COA 2.3 - Only the group name column can be edited.

* Given user is logged in
* And user have permission "edit\_chart\_of\_account"
* And the user on the list page chart of account
* And user already have major group "current asset"
* And user already have parent group "Cash and Bank"
* And the coa group "gpr01" already have transaction reference
* And user already have folder with "gpr01"
* And user click folder "gpr01"
* And user click button "Edit group"

![](<../../.gitbook/assets/image (330)>)

* Then user redirect to edit form
* And column "group code" should be disable

![](<../../.gitbook/assets/image (331)>)

## Group-COA 2.4 - The system displays the message "This field is required."

* Given user is logged in
* And user have permission "edit\_chart\_of\_account"
* And the user on the list page chart of account
* And user already have major group "current asset".
* And user already have parent group "Cash and Bank"
* When the user click button "edit"

![](<../../.gitbook/assets/image (330)>)

* And user leave empty column group code.

![](<../../.gitbook/assets/image (332)>)

* And user leave empty column group name

![](<../../.gitbook/assets/image (332)>)

* And user click the button "update".

![](<../../.gitbook/assets/image (333)>)

* Then the user can view the notification "{column\_name} is required".

![](<../../.gitbook/assets/image (334)>)

## Group-COA 2.5 - Displays the error message "this fieled\_should be\_unique"

* Given user is logged in
* And user have permission "edit\_chart\_of\_account"
* And the user on the list page chart of account
* And user already have major group "current asset".
* And user already have parent group "Cash and Bank"
* When the user click button "edit"
* And user type "101" into column "Group code"

![](<../../.gitbook/assets/image (335)>)

* And user type "Ganesha park residence" into column "Group Name"

![](<../../.gitbook/assets/image (336)>)

* And user click button "update"

![](<../../.gitbook/assets/image (337)>)

* Then user can view the notification "{column\_name} is already exist"

![](<../../.gitbook/assets/image (338)>)

## Group-COA 2-6.The system displays the message "Successfully updated"

* Given user is logged in
* And user have permission "create\_chart\_of\_account"
* And the user on the list page chart of account
* And user already have major group "current asset"
* And user already have parent group "Cash and Bank"
* And user already have folder with code "101"
* When user click group "101"
* And user click button "edit"
* And user type "group01" into column "Group code"

![](<../../.gitbook/assets/image (339)>)

* And user type "Ganesha park residence" into column "Group Name"

![](<../../.gitbook/assets/image (340)>)

* And user click the button "update".

![](<../../.gitbook/assets/image (341)>)

* Then user redirect to list page

![](<../../.gitbook/assets/image (342)>)

* And user can view notification "Successfully updated"
