# Create Cash In

## CI.1.1 – Redirect to the login page

* Given I have not logged in
* When I type `/finance/point/cash/in/create` into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (170)>)

## CI.1.2 – Redirect to the forbidden page

* Given I already logged in
* And I do not have permission to create cash in
* When I type `/finance/point/cash/in/` create into browser
* Then I redirect to forbidden page

![](<../../.gitbook/assets/image (171)>)

## CI.1.3 – The system displays the message "Cash account is required"

* Given I already logged in
* And I have permission to create cash in
* And I am on the page `/finance/point/cash`
* When I click receive payment button on the list page

![](<../../.gitbook/assets/image (172)>)

* And I click receive payment

![](<../../.gitbook/assets/image (173)>)

* And I leave empty column cash account

![](<../../.gitbook/assets/image (174)>)

* And I select "\[CUS-103] PAK ROBBY" in payment from field

![](<../../.gitbook/assets/image (175)>)

* And I type "testing" into column "notes"

![](<../../.gitbook/assets/image (176)>)

* And I select account "HONORARIUM KONSULTAN" in account column

![](<../../.gitbook/assets/image (177)>)

* And I type "kelebihan bayar" into column notes

![](<../../.gitbook/assets/image (178)>)

* And I type "1.000.000" into column amount

![](<../../.gitbook/assets/image (179)>)

* And I select "partial allocation" on the column allocation

![](<../../.gitbook/assets/image (180)>)

* And I click submit button

![](<../../.gitbook/assets/image (181)>)

* Then I should see the message "Account is required" below account column

![](<../../.gitbook/assets/image (182)>)

## CI.1.4 – The system displays the message "Payment form is required"

* Given I already logged in
* And I have permission to create cash in
* And I am on the page `/finance/point/cash`
* When I click receive payment button on the list page

![](<../../.gitbook/assets/image (183)>)

* And I click receive payment

![](<../../.gitbook/assets/image (184)>)

* And I select "10101 KAS BESAR" on the column payment from

![](<../../.gitbook/assets/image (185)>)

* And I leave empty column "payment from"

![](<../../.gitbook/assets/image (186)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (187)>)

* And I select account "HONORARIUM KONSULTAN" in account column

![](<../../.gitbook/assets/image (188)>)

* And I type "kelebihan bayar" into column notes

![](<../../.gitbook/assets/image (189)>)

* And I type "100.000" into column amount

![](<../../.gitbook/assets/image (190)>)

* And I select "partial allocation"

![](<../../.gitbook/assets/image (191)>)

* And I click submit button

![](<../../.gitbook/assets/image (192)>)

* Then I should see the message "Payment from is required" below account column

![](<../../.gitbook/assets/image (193)>)

## CI.1.5 – The system displays the message "Account is required"

* Given I already logged in
* And I have permission to create cash in
* And I am on the page `/finance/point/cash`
* When I click receive payment button on the list page

![](<../../.gitbook/assets/image (194)>)

* And I click receive payment

![](<../../.gitbook/assets/image (195)>)

* And I select "10101 KAS BESAR"

![](<../../.gitbook/assets/image (196)>)

* And I select "\[CUS-103] PAK ROBBY" in payment from field

![](<../../.gitbook/assets/image (197)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (198)>)

* And I leave empty column account

![](<../../.gitbook/assets/image (199)>)

* And I type "testing"into column notes

![](<../../.gitbook/assets/image (200)>)

* And I type "100.000" into column amount

![](<../../.gitbook/assets/image (201)>)

* And I select "partial allocation" on the column allocation

![](<../../.gitbook/assets/image (202)>)

* And I click submit button

![](<../../.gitbook/assets/image (203)>)

* Then I should see the message "Account is required" below account column

![](<../../.gitbook/assets/image (204)>)

## CI.1.6 – The system displays the message "Amount is required"

* Given I already logged in
* And I have permission to create cash in
* And I am on the page `/finance/point/cash`
* When I click receive payment button on the list page
* And I click receive payment
* And I select "10101 KAS BESAR" on the column cash account

![](<../../.gitbook/assets/image (205)>)

* And I select "\[CUS-103] PAK ROBBY" in payment from field

![](<../../.gitbook/assets/image (206)>)

* And I type "testing" into column "Notes"

![](<../../.gitbook/assets/image (207)>)

* And I select account "Honorarium konsultan" in account column

![](<../../.gitbook/assets/image (208)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (209)>)

* And I leave empty column "amount"

![](<../../.gitbook/assets/image (210)>)

* And I select "partial allocation" on the column allocation

![](<../../.gitbook/assets/image (211)>)

* And I click submit button

![](<../../.gitbook/assets/image (212)>)

* Then I should see the message "Amount is required" below account column

![](<../../.gitbook/assets/image (213)>)

## CI.1.7 – The system displays the message "Amount must be filled with data numbers"

* Given I already logged in
* And I have permission to create cash in
* And I am on the page `/finance/point/cash`
* When I click receive payment button on the list page
* And I click receive payment
* And I select "10101 KAS BESAR"

![](<../../.gitbook/assets/image (214)>)

* And I select "\[CUS-103] PAK ROBBY" in payment from column

![](<../../.gitbook/assets/image (215)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (216)>)

* And I select account "Honorarium Konsultan" in account column

![](<../../.gitbook/assets/image (217)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (218)>)

* And I type "xxwed" into column amount

![](<../../.gitbook/assets/image (219)>)

* And I select "partial allocation" in allocation column

![](<../../.gitbook/assets/image (220)>)

* And I click submit button

![](<../../.gitbook/assets/image (221)>)

* Then I should see the message "Amount must be filled with data numbers" below account column

![](<../../.gitbook/assets/image (222)>)

## CI.1.8 – The system displays the message "Successfully create"

* Given I already logged in
* And I have permission to create cash in
* And I am on the page `/finance/point/cash`
* When I click receive payment button on the list page

![](<../../.gitbook/assets/image (223)>)

* And I click receive payment

![](<../../.gitbook/assets/image (224)>)

* And I select "10101 KAS BESAR"

![](<../../.gitbook/assets/image (225)>)

* And I select "\[CUS-103] PAK ROBBY" in payment from field

![](<../../.gitbook/assets/image (226)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (227)>)

* And I select "Honorarium konsultan" in account column

![](<../../.gitbook/assets/image (228)>)

* And I type "testing" into column notes

![](<../../.gitbook/assets/image (229)>)

* And I type "100.000" into column amount

![](<../../.gitbook/assets/image (230)>)

* And I click submit button

![](<../../.gitbook/assets/image (231)>)

* Then I should see the message "Successfully created"

![](<../../.gitbook/assets/image (232)>)

* And I should redirect to detail page

![](<../../.gitbook/assets/image (233)>)

*   Then the system will record a journal entry as shown below. Account Debit Credit

    {10101 KAS BESAR}

    Rp.xxx.xxx

    {HONORARIUM KONSULTAN}

    Rp.xxx.xxx
