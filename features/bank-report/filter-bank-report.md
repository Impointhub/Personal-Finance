# Filter Bank Report

## BF1: System displays data according to filters

* Given I already logged in
* And I have permission to read bank report
* And I on the page "https://test.app.point.red/finance/point/report/bank"
* When I click "Filter"

![](<../../.gitbook/assets/image (480)>)

* And I select "01 May 2026" into column "date from"

![](<../../.gitbook/assets/image (481)>)

* And I select "31 Aug 2026" into column "date to"

![](<../../.gitbook/assets/image (482)>)

* And I select "Bank BCA Giro KE-4 2588807881" into column "account"

![](<../../.gitbook/assets/image (483)>)

* And I select "All" into column "subledger"

![](<../../.gitbook/assets/image (484)>)

* And I click "Apply filter"

![](<../../.gitbook/assets/image (485)>)

* Then the system displays the bank report data filtered by "01 May 2026", "31 Aug 2026", "Bank BCA Giro KE-4 2588807881" and "All" subledger.

![](<../../.gitbook/assets/image (486)>)
