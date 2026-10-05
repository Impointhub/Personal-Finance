# Read Cash Report

## CR1: User redirect to login page

* Given I am not logged in
* When I type "https://test.app.point.red/finance/point/report/cash" into browser
* Then the system redirects me to the login page

![](<../../.gitbook/assets/image (447)>)

## CR2: Redirect to forbidden page

* Given I already logged in
* And I do not have permission to read cash report
* When I type "https://test.app.point.red/finance/point/report/cash" into browser
* Then the system redirects me to the restricted access page

![](<../../.gitbook/assets/image (448)>)

## CR3: Displaying cash report data

* Given I already logged in
* And I have permission to read cash report
* When I type "https://test.app.point.red/finance/point/report/cash" into browser
* And I select "01 May 2026" into column "period from"

![](<../../.gitbook/assets/image (449)>)

* And I select "31 Aug 2026" into column "period to"

![](<../../.gitbook/assets/image (450)>)

* And I select "Kas Kecil Outlet 1" into column "account"

![](<../../.gitbook/assets/image (451)>)

* And I select "All" into column "subledger"

![](<../../.gitbook/assets/image (452)>)

* Then the system displays the cash report data

![](<../../.gitbook/assets/image (453)>)
