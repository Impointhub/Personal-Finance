# Detail Bank Out

## DBO.1 : User redirect to login page

* Given I have not logged in
* When I type https://test.app.point.red/finance/point/bank/out/1 into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (30)>)

## DBO.2 : User redirect to forbidden page

* Given I already logged in
* And I do not have permission to view bank out detail
* When I type https://test.app.point.red/finance/point/bank/out/1 into browser
* Then I should be redirected to the forbidden page

![](<../../.gitbook/assets/image (31)>)

## DBO.3 : Displaying the bank-out details page

* Given I already logged in
* And I have permission to view bank out detail
* When I type https://test.app.point.red/finance/point/bank/out/1 into browser
* Then I should see the bank out detail page

![](<../../.gitbook/assets/image (32)>)
