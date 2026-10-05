# List Bank Out

## LBO.1 : User redirect to login page

* Given I have not logged in
* When I type https://test.app.point.red/finance/point/bank/out/1 into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (44)>)

## LBO.2 : User redirect to forbidden page

* Given I already logged in
* And I do not have permission to read bank out
* When I type https://test.app.point.red/finance/point/bank/ into browser
* Then I should be redirected to the forbidden page

![](<../../.gitbook/assets/image (45)>)

## LBO.3 : Displays list of entered bank-out data

* Given I already logged in
* And I have permission to view bank out list
* When I type https://test.app.point.red/finance/point/bank/out/1 into browser
* Then I should see the list of entered bank out data

![](<../../.gitbook/assets/image (46)>)
