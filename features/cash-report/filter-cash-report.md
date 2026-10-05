# Filter Cash Report

## CF1: System displays data according to filters

* Given I already logged in
* And I have permission to read cash report
* And I type "https://test.app.point.red/finance/point/report/cash" into browser
* When I click "Filter"

![](<../../.gitbook/assets/image (440)>)

* And I select "01 May 2026" into column "date from"

![](<../../.gitbook/assets/image (441)>)

* And I select "31 Aug 2026" into column "date to"

![](<../../.gitbook/assets/image (442)>)

* And I select "Kas Kecil Outlet 1" into column "account"

![](<../../.gitbook/assets/image (443)>)

* And I select "All" into column "subledger"

![](<../../.gitbook/assets/image (444)>)

* And I click "Apply filter"

![](<../../.gitbook/assets/image (445)>)

* Then the system displays the cash report data filtered by "01 May 2026", "31 Aug 2026", "Kas Kecil Outlet 1" and "All" subledger

![](<../../.gitbook/assets/image (446)>)
