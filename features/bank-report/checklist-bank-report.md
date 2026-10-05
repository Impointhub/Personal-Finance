# Checklist bank report

## BK.1. checked checkbox

* Given I already logged in
* And I have permission to read bank report
* And I on the page "/finance/point/report/bank"
* And the report already displays transaction data

![](<../../.gitbook/assets/image (466)>)

* When I click the checkbox on the row "BANK-IN/0017/V/26"

![](<../../.gitbook/assets/image (467)>)

* Then the system marks the row "BANK-IN/0017/V/26" as reconciled

![](<../../.gitbook/assets/image (468)>)

* And the row displays the label "Reconciled"

![](<../../.gitbook/assets/image (469)>)
