# Create Bank In

## BI.1.1 – Redirect to the login page

* Given I have not logged in
* When I type [https://test.app.point.red/finance/point/bank/in/create](https://test.app.point.red/finance/point/cash/in/create) into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (54)>)

## BI.1.2 – Redirect to the forbidden page

* Given I already logged in
* And I do not have permission to create cash in
* When I type [https://test.app.point.red/finance/point/bank/in/create](https://test.app.point.red/finance/point/cash/in/create) into browser
* Then I redirect to forbidden page

![](<../../.gitbook/assets/image (55)>)

## BI.1.3 – The system displays the message "Bank Account is required"

* Given I already logged in
* And I have permission to create cash in
* And I am on the page https://test.app.point.red/finance/point/bank
* When I click receive payment button on the list page

![](<../../.gitbook/assets/image (56)>)

* And I click receive payment

![](<../../.gitbook/assets/image (57)>)

* And I leave empty column bank account

![](<../../.gitbook/assets/image (58)>)

* And I select "\[CUS-103] PAK ROBBY" in payment from field

![](<../../.gitbook/assets/image (59)>)

* And I type "testing" into column "notes"

![](<../../.gitbook/assets/image (60)>)

* And I select account "HONORARIUM KONSULTAN" in account column

![](<../../.gitbook/assets/image (61)>)

* And I type "kelebihan bayar" into column notes

![](<../../.gitbook/assets/image (62)>)

* And I type "100.000" into column amount

![](<../../.gitbook/assets/image (63)>)

* And I select "partial allocation" on the column allocation

![](<../../.gitbook/assets/image (64)>)

* And I click submit button

![](<../../.gitbook/assets/image (65)>)

* Then I should see the message "Bank Account is required" below account column

![](<../../.gitbook/assets/image (66)>)

## BI.1.4 – The system displays the message "Payment form is required"

* Given I already logged in
* And I have permission to create cash in
* And I am on the page https://test.app.point.red/finance/point/bank
* When I click receive payment button on the list page

![](<../../.gitbook/assets/image (56)>)

* And I click receive payment

![](<../../.gitbook/assets/image (57)>)

* And I select "10210 BANK BCA GIRO KE - 4 258807881" on the column bank account

![](<../../.gitbook/assets/image (67)>)

* And I leave empty column "payment from"

![](<../../.gitbook/assets/image (68)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (60)>)

* And I select account "HONORARIUM KONSULTAN" in account column

![](<../../.gitbook/assets/image (61)>)

* And I type "kelebihan bayar" into column notes

![](<../../.gitbook/assets/image (62)>)

* And I type "100.000" into column amount

![](<../../.gitbook/assets/image (63)>)

* And I select "partial allocation"

![](<../../.gitbook/assets/image (64)>)

* And I click submit button

![](<../../.gitbook/assets/image (65)>)

* Then I should see the message "Payment from is required" below account column

![](<../../.gitbook/assets/image (69)>)

## BI.1.5 – The system displays the message "Account is required"

* Given I already logged in
* And I have permission to create cash in
* And I am on the page https://test.app.point.red/finance/point/bank
* When I click receive payment button on the list page

![](<../../.gitbook/assets/image (56)>)

* And I click receive payment

![](<../../.gitbook/assets/image (57)>)

* And I select "10210 BANK BCA GIRO KE - 4 258807881" on the column bank account

![](<../../.gitbook/assets/image (70)>)

* And I select "\[CUS-103] PAK ROBBY" in payment from column

![](<../../.gitbook/assets/image (71)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (60)>)

* And I leave empty column account

![](<../../.gitbook/assets/image (72)>)

* And I type "testing"into column notes

![](<../../.gitbook/assets/image (73)>)

* And I type "100.000" into column amount

![](<../../.gitbook/assets/image (74)>)

* And I select "partial allocation" on the column allocation

![](<../../.gitbook/assets/image (75)>)

* And I click submit button

![](<../../.gitbook/assets/image (76)>)

* Then I should see the message "Account is required" below account column

![](<../../.gitbook/assets/image (77)>)

## BI.1.6 – The system displays the message "Amount is required"

* Given I already logged in
* And I have permission to create bank in
* And I am on the page https://test.app.point.red/finance/point/bank
* When I click receive payment button on the list page

![](<../../.gitbook/assets/image (78)>)

* And I click receive payment

![](<../../.gitbook/assets/image (79)>)

* And I select "10210 BANK BCA GIRO KE - 4 258807881" on the column bank account

![](<../../.gitbook/assets/image (80)>)

* And I select "\[CUS-103] PAK ROBBY" in payment from column

![](<../../.gitbook/assets/image (81)>)

* And I type "testing" into column "Notes"

![](<../../.gitbook/assets/image (82)>)

* And I select account "Honorarium konsultan" in account column

![](<../../.gitbook/assets/image (83)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (84)>)

* And I leave empty column "amount"

![](<../../.gitbook/assets/image (85)>)

* And I select "partial allocation" on the column allocation

![](<../../.gitbook/assets/image (86)>)

* And I click submit button

![](<../../.gitbook/assets/image (87)>)

* Then I should see the message "Amount is required" below account column

![](<../../.gitbook/assets/image (89)>)

## BI.1.7 – The system displays the message "Amount must be filled with data numbers"

* Given I already logged in
* And I have permission to create bank in
* And I am on the page https://test.app.point.red/finance/point/bank
* When I click receive payment button on the list page

![](<../../.gitbook/assets/image (78)>)

* And I click receive payment

![](<../../.gitbook/assets/image (79)>)

* And I select "10210 BANK BCA GIRO KE - 4 258807881" on the column bank account

![](<../../.gitbook/assets/image (92)>)

* And I select "\[CUS-103] PAK ROBBY" in payment from column

![](<../../.gitbook/assets/image (94)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (96)>)

* And I select account "Honorarium Konsultan" in account column

![](<../../.gitbook/assets/image (98)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (100)>)

* And I type "xxwed" into column amount

![](<../../.gitbook/assets/image (102)>)

* And I select "partial allocation" in allocation column

![](<../../.gitbook/assets/image (104)>)

* And I click submit button

![](<../../.gitbook/assets/image (106)>)

* Then I should see the message "Amount must be filled with data numbers" below account column

![](<../../.gitbook/assets/image (107)>)

## BI.1.8 – The system displays the message "Successfully create"

* Given I already logged in
* And I have permission to create bank in
* And I am on the page https://test.app.point.red/finance/point/bank
* When I click receive payment button on the list page

![](<../../.gitbook/assets/image (78)>)

* And I click receive payment

![](<../../.gitbook/assets/image (79)>)

* And I select "10210 BANK BCA GIRO KE - 4 258807881"

![](<../../.gitbook/assets/image (108)>)

* And I select "\[CUS-103] PAK ROBBY" in payment from column

![](<../../.gitbook/assets/image (109)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (110)>)

* And I select "Honorarium konsultan" in account column

![](<../../.gitbook/assets/image (111)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (112)>)

* And I type "100.000" into column amount

![](<../../.gitbook/assets/image (113)>)

* And I click submit button

![](<../../.gitbook/assets/image (114)>)

* Then I should see the message "Successfully created"

![](<../../.gitbook/assets/image (115)>)

* And I should redirect to detail page

![](<../../.gitbook/assets/image (116)>)

* Then the system will record a journal entry as shown below.

| Account                                 | Debit      | Credit     |
| --------------------------------------- | ---------- | ---------- |
| {10210 BANK BCA GIRO KE - 4 2588807881} | Rp.xxx.xxx |            |
| {HONORARIUM KONSULTAN}                  |            | Rp.xxx.xxx |
