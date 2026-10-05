# Create Bank Out

## CB.F1 - Redirect to login page because user unauthenticated

* Given I have not logged in
* When I type /finance/point/bank into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (16)>)

## CB.F2 - Redirect to the forbidden page because user don't have permission create\_bank out

* Given I already logged in
* And I do not have permission to create bank out
* When I open the page https://test.app.point.red/finance/point/bank
* Then I should not see the "Make a Payment" button

![](<../../.gitbook/assets/image (17)>)

## CB.F3 - The system displays the message "bank account is required" because the user didn't enter a bank account

* Given I already logged in
* And I have permission to create bank out
* And I am on the page /finance/point/bank
* When I click "Make a Payment" button

![](<../../.gitbook/assets/image (18)>)

* And I leave column bank account empty

![](<../../.gitbook/assets/image (21)>)

* And I click submit

![](<../../.gitbook/assets/image (22)>)

* Then I should see the message "Bank account is required"

![](<../../.gitbook/assets/image (23)>)

CB.F4 - The system displays the message "Payment to is required"&#x20;because the user didn't enter a payment to
------------------------------------------------

* Given I already logged in
* And I have permission to create bank out
* And I am on the page /finance/point/bank
* When I click "Make a Payment" button

<figure><img src="../../.gitbook/assets/image (64).png" alt=""><figcaption></figcaption></figure>

* Bank Account And Account displaying the list of charts of accounts accessible to the user.
* When user select account "20122 - Bank Account Cabang Malang 2"

<figure><img src="../../.gitbook/assets/image (65).png" alt=""><figcaption></figcaption></figure>

* And user leave empty column "payment to"&#x20;

<figure><img src="../../.gitbook/assets/image (66).png" alt=""><figcaption></figcaption></figure>

* And user select account "53101 - Accomodation Expense"&#x20;

<figure><img src="../../.gitbook/assets/image (67).png" alt=""><figcaption></figcaption></figure>

* And user type "testing" into column notes&#x20;

<figure><img src="../../.gitbook/assets/image (68).png" alt=""><figcaption></figcaption></figure>

* And user type "100.000" into column amount&#x20;

<figure><img src="../../.gitbook/assets/image (69).png" alt=""><figcaption></figcaption></figure>

* And user select allocation "BANK NISP"

<figure><img src="../../.gitbook/assets/image (70).png" alt=""><figcaption></figcaption></figure>

* And user select approved by "martien"
* And user click submit&#x20;
* Then user can redirect to detail page&#x20;
* And status approval bank out will be pending&#x20;
* And system sent approval to approved by&#x20;

## CB.F5 - The system displays the message "account is required" because the user didn't enter an account

* Given I already logged in
* And I have permission to create bank out
* And I am on the page /finance/point/bank
* When I click "Make a Payment" button

<figure><img src="../../.gitbook/assets/image (71).png" alt=""><figcaption></figcaption></figure>

* Bank Account And Account displaying the list of charts of accounts accessible to the user.
* When user select bank account "20122 Bank Account Cabang Malang 2"&#x20;

<figure><img src="../../.gitbook/assets/image (80).png" alt=""><figcaption></figcaption></figure>

* And user select payment to \[CUS-100] Nganjuk

<figure><img src="../../.gitbook/assets/image (82).png" alt=""><figcaption></figcaption></figure>

* And user leave empty column account&#x20;
* And user type "testing" into column notes&#x20;

<figure><img src="../../.gitbook/assets/image (83).png" alt=""><figcaption></figcaption></figure>

* And user type "100.000" into column amount&#x20;

<figure><img src="../../.gitbook/assets/image (84).png" alt=""><figcaption></figcaption></figure>

* And user select "Bank NISP" into colum allocation&#x20;

<figure><img src="../../.gitbook/assets/image (85).png" alt=""><figcaption></figcaption></figure>

* And user select "approved by"
* And user click submit&#x20;
* Then user can view notifications "account is required"&#x20;

<figure><img src="../../.gitbook/assets/image (79).png" alt=""><figcaption></figcaption></figure>

* And user should remain on the create page&#x20;

CB.F6 - The system displays the message "amount is required"&#x20;because the user didn't enter an amount
---------------------------------------------

* Given I already logged in
* And I have permission to create bank out
* And I am on the page /finance/point/bank
* When I click "Make a Payment" button

<figure><img src="../../.gitbook/assets/image (72).png" alt=""><figcaption></figcaption></figure>

* Bank Account And Account displaying the list of charts of accounts accessible to the user.
* When user select bank account "20122 Bank Account Cabang Malang 2"

<figure><img src="../../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>

* And user select payment to \[CUS-100] Nganjuk&#x20;

<figure><img src="../../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

* And user leave empty column account&#x20;
* And user type "testing" into column notes&#x20;

<figure><img src="../../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>

* And user leave empty column amount&#x20;

<figure><img src="../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>

* And user select "Bank NISP" into colum allocation&#x20;

<figure><img src="../../.gitbook/assets/image (78).png" alt=""><figcaption></figcaption></figure>

* And user select approved by&#x20;
* And user klik submit&#x20;
* Then user can view notification "amount is required"&#x20;

<figure><img src="../../.gitbook/assets/image (87).png" alt=""><figcaption></figcaption></figure>

* And user should remain on the create page&#x20;

CB.F7 - The system displays the message "Please enter a valid amount using numbers only."&#x20;because the user didn't enter an valid amount
---------------------------------------------------

* Given user already logged in
* And user  have permission to create bank out
* And user on the page /finance/point/bank
* When user click make a payment&#x20;

<figure><img src="../../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>

* Bank Account And Account displaying the list of charts of accounts accessible to the user.
* When user select bank account "20122 Bank Account Cabang Malang 2"
* And user select payment to "\[Cus-100] Nganjuk"&#x20;
* And user select account "53101 Accomodation Expenses"&#x20;
* And user type "Testing" into column Notes&#x20;
* And user type "abc" Into column Amount
* And user select "BANK NISP" Into column allocation&#x20;
* And user select "Budi Santoso" into column approval by&#x20;
* And user click submit&#x20;
* Then user can view notification "Please enter a valid amount using numbers only"
* And user should remain on the create page&#x20;

CB.F8 - The system displays the message "Amount must be greater than zero."\
because the user didn't enter an amount greater than zero
---------------------------------------------------------

* Given user already logged in
* And user  have permission to create bank out
* And user on the page /finance/point/bank
* When user click make a payment&#x20;

<figure><img src="../../.gitbook/assets/image (90).png" alt=""><figcaption></figcaption></figure>

* Bank Account And Account displaying the list of charts of accounts accessible to the user.
* When user select bank account "20122 Bank Account Cabang Malang 2"

<figure><img src="../../.gitbook/assets/image (91).png" alt=""><figcaption></figcaption></figure>

* And user select payment to "\[Cus-100] Nganjuk"&#x20;

<figure><img src="../../.gitbook/assets/image (92).png" alt=""><figcaption></figcaption></figure>

* And user select account "53101 Accomodation Expenses"&#x20;

<figure><img src="../../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>

* And user type "Testing" into column Notes&#x20;

<figure><img src="../../.gitbook/assets/image (94).png" alt=""><figcaption></figcaption></figure>

* And user type "0" Into column Amount

<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

* And user select "BANK NISP" Into column allocation&#x20;

<figure><img src="../../.gitbook/assets/image (59).png" alt=""><figcaption></figcaption></figure>

* And user select "Budi Santoso" into column approval by&#x20;

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

* And user click submit&#x20;

<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

* Then user can view notification "Amount must be greater than zero"&#x20;

<figure><img src="../../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

* And user should remain on the create page&#x20;

## CB.S1 : The system displays the message "Successfully created"

* Given user already logged in
* And user have permission to create bank out
* And user on the page /finance/point/bank
* When user click "Make a Payment" button

![](<../../.gitbook/assets/image (18)>)

* And user select "20122 Bank Account Cabang Malang 2"

<figure><img src="../../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

* And user select "\[CUS-100] Nganjuk" into column payment to&#x20;

<figure><img src="../../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

* And user select "
* And I click submit
* Then I should see the notification "Successfully created"

![](<../../.gitbook/assets/image (28)>)

* And I should be redirected to the bank out detail page

![](<../../.gitbook/assets/image (29)>)

* Then the system will record a journal entry as shown below.

| Account                                   | Debit      | Credit     |
| ----------------------------------------- | ---------- | ---------- |
| (account selected from the payment order) | Rp.xxx.xxx |            |
| {Bank Cabang Malang 2}                    |            | Rp.xxx.xxx |

