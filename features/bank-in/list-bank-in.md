# List Bank In

## BI.3.1 – Redirect to the login page

* Given I have not logged in
* When I type https://test.app.point.red/finance/point/bank into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (47)>)

## BI.3.2 – Redirect to the forbidden page

* Given I already logged in
* And I do not have permission to read bank out
* When I type https://test.app.point.red/finance/point/bank/ into browser
* Then I should be redirected to the forbidden page

![](<../../.gitbook/assets/image (48)>)

## BI.3.3 – The system displays the message "you don't have any data yet"

* Given I already logged in
* And I have permission to read bank in
* And I don't have the bank-in data yet
* When I type https://test.app.point.red/finance/point/bank/ into browser
* Then I can see text "you don't have any data yet"

![](<../../.gitbook/assets/image (49)>)

## BI.3.4 – The system displays all Bank In data that has been entered by the user

* Given I already logged in
* And I have permission to read bank in
* And I already have data bank-in
* When I type https://test.app.point.red/finance/point/bank/ into browser
* Then the sysmtem dispays all bank in data that has been entered

![](<../../.gitbook/assets/image (50)>)
