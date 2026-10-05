# Filter General Ledger

## GF1: System displays data according to filters

* Given I logged in
* And I has permission to read the general ledger report
* And I on the general ledger page

![](<../../../.gitbook/assets/image (8)>)

* When I selects "01-08-2026" on the column date from

![](<../../../.gitbook/assets/image (9)>)

* And I selects "15-08-2026" on the column date to

![](<../../../.gitbook/assets/image (10)>)

* And I selects "10205-BANK BCA GIRO PUSAT 1" on the column account

![](<../../../.gitbook/assets/image (11)>)

* Then the system updates the table to match the selected date range and account

![](<../../../.gitbook/assets/image (12)>)
