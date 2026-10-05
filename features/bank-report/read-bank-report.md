# Read Bank Report

## BR1: User redirect to login page

* Given I am not logged in
* When I open the page "https://test.app.point.red/finance/point/report/bank"
* Then the system redirects me to the login page

![](<../../.gitbook/assets/image (487)>)

## BR2: Redirect to forbidden page

* Given I already logged in
* And I do not have permission to read bank report
* When I open the page "https://test.app.point.red/finance/point/report/bank"
* Then the system redirects me to the restricted access page

![](<../../.gitbook/assets/image (488)>)

## BR3: Displaying bank report data

* Given I already logged in
* And I have permission to read bank report
* And I on the page "https://test.app.point.red/finance/point"
* When I click "Bank Report"

![](<../../.gitbook/assets/image (489)>)

* Then the system opens the page "https://test.app.point.red/finance/point/report/bank"

![](<../../.gitbook/assets/image (490)>)

* And the system displays the bank report page
