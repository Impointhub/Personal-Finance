# Detail Cash Out

## DBO.1 : User redirect to login page

* Given I have not logged in
* When I type /finance/point/cash/out/1 into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (421)>)

## DBO.2 : User redirect to forbidden page

* Given I already logged in
* And I do not have permission to view bank out detail
* When I type /finance/point/bank/out/1 into browser
* Then I should be redirected to the forbidden page

![](<../../.gitbook/assets/image (422)>)

## DBO.3 : Displaying the cash-out details page

* Given I already logged in
* And I have permission to view cash out detail
* When I type /finance/point/bank/out/1 into browser
* Then I should see the cash out detail page

<figure><img src="../../.gitbook/assets/image (160).png" alt=""><figcaption></figcaption></figure>
