# Detail Bank In

## BI.4.1 – Redirect to the login page

* Given I have not logged in
* When I type https://test.app.point.red/finance/point/bank into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (51)>)

## BI.4.2 – Redirect to the forbidden page

* Given I already logged in
* And I do not have permission to read bank out
* When I type https://test.app.point.red/finance/point/bank/ into browser
* Then I should be redirected to the forbidden page

![](<../../.gitbook/assets/image (52)>)

## BI.4.3 – The system displays the detail of the selected Bank In transaction

* Given I already logged in
* And I have permission to read bank in
* When I type https://test.app.point.red/finance/point/bank/in/1 into browser
* Then I should see the bank in detail page

![](<../../.gitbook/assets/image (53)>)
