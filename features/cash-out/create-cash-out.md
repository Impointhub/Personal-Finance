# Create Cash Out

## CC.F1 - Redirect to login page because user unauthenticated

* Given I have not logged in
* When I type /finance/point/cash into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (369)>)

## CC.F2 - Redirect to the forbidden page because user don't have permission create\_cash out

* Given I already logged in
* And I do not have permission to cash out
* When I open the page /finance/point/cash
* Then I should not see the "Make a Payment" button

<figure><img src="../../.gitbook/assets/image (133).png" alt=""><figcaption></figcaption></figure>

## CC.F3 - The system displays the message "cash account is required" because the user didn't enter a bank account

* Given I already logged in
* And I have permission to create cash out
* And I am on the page /finance/point/cash
* When I click "Make a Payment" button

<figure><img src="../../.gitbook/assets/image (134).png" alt=""><figcaption></figcaption></figure>

* And I leave column cash account empty

<figure><img src="../../.gitbook/assets/image (135).png" alt=""><figcaption></figcaption></figure>

* And I click submit

![](<../../.gitbook/assets/image (373)>)

* Then I should see the message "cash account is required"

<figure><img src="../../.gitbook/assets/image (136).png" alt=""><figcaption></figcaption></figure>

## CB.F4 - The system displays the message "Payment to is required" because the user didn't enter a payment to

* Given I already logged in
* And I have permission to create cash out
* And I am on the page /finance/point/cash
* When I click "Make a Payment" button

![](<../../.gitbook/assets/image (375)>)

* Bank Account And Account displaying the list of charts of accounts accessible to the user.
* When user select account "10122 - Kas Account Cabang Malang 2"

<figure><img src="../../.gitbook/assets/image (137).png" alt=""><figcaption></figcaption></figure>

* And user leave empty column "payment to"

![](<../../.gitbook/assets/image (376)>)

* And user select account "53101 - Accomodation Expense"

![](<../../.gitbook/assets/image (377)>)

* And user type "testing" into column notes

![](<../../.gitbook/assets/image (378)>)

* And user type "100.000" into column amount

![](<../../.gitbook/assets/image (379)>)

* And user select allocation "BANK NISP"

![](<../../.gitbook/assets/image (380)>)

* And user select approved by "kartika"

<figure><img src="../../.gitbook/assets/image (138).png" alt=""><figcaption></figcaption></figure>

* And user click submit

<figure><img src="../../.gitbook/assets/image (139).png" alt=""><figcaption></figcaption></figure>

* Then user can redirect to detail page
* And status approval cash out will be pending
* And system sent approval to approved by

## CB.F5 - The system displays the message "account is required" because the user didn't enter an account

* Given I already logged in
* And I have permission to create cash out
* And I am on the page /finance/point/cash
* When I click "Make a Payment" button

![](<../../.gitbook/assets/image (381)>)

* Cash Account And Account displaying the list of charts of accounts accessible to the user.
* When user select bank account "10122 Kas Kecil Cabang Malang 2"

<figure><img src="../../.gitbook/assets/image (140).png" alt=""><figcaption></figcaption></figure>

* And user select payment to \[CUS-100] Nganjuk

![](<../../.gitbook/assets/image (383)>)

* And user leave empty column account
* And user type "testing" into column notes

![](<../../.gitbook/assets/image (384)>)

* And user type "100.000" into column amount

![](<../../.gitbook/assets/image (385)>)

* And user select "Bank NISP" into colum allocation

![](<../../.gitbook/assets/image (386)>)

* And user select approval by "kartika"

<figure><img src="../../.gitbook/assets/image (141).png" alt=""><figcaption></figcaption></figure>

* And user click submit
* Then user can view notifications "account is required"

![](<../../.gitbook/assets/image (387)>)

* And user should remain on the create page

## CB.F6 - The system displays the message "amount is required" because the user didn't enter an amount

* Given I already logged in
* And I have permission to create cash out
* And I am on the page /finance/point/cash
* When I click "Make a Payment" button

![](<../../.gitbook/assets/image (388)>)

* Bank Account And Account displaying the list of charts of accounts accessible to the user.
* When user select bank account "10122 Kas Kecil Cabang Malang 2"

<figure><img src="../../.gitbook/assets/image (142).png" alt=""><figcaption></figcaption></figure>

* And user select payment to \[CUS-100] Nganjuk

![](<../../.gitbook/assets/image (390)>)

* And user leave empty column account
* And user type "testing" into column notes

![](<../../.gitbook/assets/image (391)>)

* And user leave empty column amount

![](<../../.gitbook/assets/image (392)>)

* And user select "Bank NISP" into colum allocation

![](<../../.gitbook/assets/image (393)>)

* And user select approved by
* And user klik submit
* Then user can view notification "amount is required"

![](<../../.gitbook/assets/image (394)>)

* And user should remain on the create page

## CB.F7 - The system displays the message "Please enter a valid amount using numbers only." because the user didn't enter an valid amount

* Given user already logged in
* And user have permission to create cash out
* And user on the page /finance/point/cash
* When user click make a payment

![](<../../.gitbook/assets/image (395)>)

* Cash Account And Account displaying the list of charts of accounts accessible to the user.
* When user select cash account "10122 Kas Kecil Cabang Malang 2"

<figure><img src="../../.gitbook/assets/image (22).png" alt=""><figcaption></figcaption></figure>

* And user select payment to "\[Cus-100] Nganjuk"

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

* And user select account "53101 Accomodation Expenses"

<figure><img src="../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

* And user type "Testing" into column Notes

<figure><img src="../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

* And user type "abc" Into column Amount

<figure><img src="../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

* And user select "BANK NISP" Into column allocation

<figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

* And user select "Budi Santoso" into column approval by

<figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

* And user click submit

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption></figcaption></figure>

* Then user can view notification "Please enter a valid amount using numbers only"

<figure><img src="../../.gitbook/assets/image (31).png" alt=""><figcaption></figcaption></figure>

* And user should remain on the create page

## CB.F8 - The system displays the message "Amount must be greater than zero." because the user didn't enter an amount greater than zero

* Given user already logged in
* And user have permission to create cash out
* And user on the page /finance/point/cash
* When user click make a payment

![](<../../.gitbook/assets/image (396)>)

* Bank Account And Account displaying the list of charts of accounts accessible to the user.
* When user select bank account "10122 Kas kecil Cabang Malang 2"

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

* And user select payment to "\[Cus-100] Nganjuk"

![](<../../.gitbook/assets/image (398)>)

* And user select account "53101 Accomodation Expenses"

![](<../../.gitbook/assets/image (399)>)

* And user type "Testing" into column Notes

![](<../../.gitbook/assets/image (400)>)

* And user type "0" Into column Amount

![](<../../.gitbook/assets/image (401)>)

* And user select "BANK NISP" Into column allocation

![](<../../.gitbook/assets/image (402)>)

* And user select "Budi Santoso" into column approval by

![](<../../.gitbook/assets/image (403)>)

* And user click submit

![](<../../.gitbook/assets/image (404)>)

* Then user can view notification "Amount must be greater than zero"

![](<../../.gitbook/assets/image (405)>)

* And user should remain on the create page

## CB.S1 : The system displays the message "Successfully created"

* Given user already logged in
* And user have permission to create cash out
* And user on the page /finance/point/cash
* When user click "Make a Payment" button

<figure><img src="../../.gitbook/assets/image (33).png" alt=""><figcaption></figcaption></figure>

* And user select "10122 Kas Kecil Cabang Malang 2"

<figure><img src="../../.gitbook/assets/image (34).png" alt=""><figcaption></figcaption></figure>

* And user select "\[CUS-100] Nganjuk" into column payment to

![](<../../.gitbook/assets/image (407)>)

* And user select account "53101.Accomodation Expense"

<figure><img src="../../.gitbook/assets/image (143).png" alt=""><figcaption></figcaption></figure>

* And I click submit

<figure><img src="../../.gitbook/assets/image (144).png" alt=""><figcaption></figcaption></figure>

* Then I should see the notification "Successfully created"
* And I should be redirected to the bank out detail page
* Then the system will record a journal entry as shown below.

| Account                                   | Debit      | Credit     |
| ----------------------------------------- | ---------- | ---------- |
| (account selected from the payment order) | Rp.xxx.xxx |            |
| {Kas Kecil Cabang Malang 2}               |            | Rp.xxx.xxx |
