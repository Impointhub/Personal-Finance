# List Cash Out

## LBO.1 : User redirect to login page

* Given I have not logged in
* When I type /finance/point/cash/out/1 into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (424)>)

## LBO.2 : User redirect to forbidden page

* Given I already logged in
* And I do not have permission to read cash out
* When I type /finance/point/cash/ into browser
* Then I should be redirected to the forbidden page

![](<../../.gitbook/assets/image (425)>)

## LBO.3 : Displays list of entered bank-out data

* Given I already logged in
* And I have permission to view cash out list
* When I type /finance/point/cash/out/1 into browser
* Then I should see the list of entered cash out data

![](<../../.gitbook/assets/image (426)>)
