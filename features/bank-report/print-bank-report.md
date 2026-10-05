# Print Bank Report

## BP.1. Then system show pop up print

* Given I already logged in
* And I have permission to read bank report
* And I on the page "/finance/point/report/bank"

![](<../../.gitbook/assets/image (470)>)

* And the report already displays transaction data

![](<../../.gitbook/assets/image (471)>)

* When I click "Print" on the row "BANK-IN/0017/V/26"

![](<../../.gitbook/assets/image (472)>)

* Then the system displays the print preview for "BANK-IN/0017/V/26"
* And the print preview shows the form date, person, account, notes, received, and disbursed amount
* And the system displays a "Print" button and a "Close" button
