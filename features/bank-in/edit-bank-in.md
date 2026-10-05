# Edit Bank In

## EB.2.1 – Redirect to the login page

* Given I have not logged in
* When I type `/finance/point/bank/in/{id}/edit` into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (54)>)

## EB.2.2 – Redirect to the forbidden page

* Given I already logged in
* And I do not have permission to update bank in
* When I type `/finance/point/bank/in/{id}/edit` into browser
* Then I should be redirected to the forbidden page

![](<../../.gitbook/assets/image (55)>)

## EB.2.3 – The system displays the existing data on the edit form

* Given I already logged in
* And I have permission to update bank in
* And I am on the page `/finance/point/bank`
* When I click on an existing bank in transaction on the list page

<figure><img src="../../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

* And I click the edit button on the detail page

<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

* Then I should be redirected to the edit page

<figure><img src="../../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>

* And I should see the payment date bank account, payment from, notes, account,notes amount, and allocation columns already filled with the existing data

<figure><img src="../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

## EB.2.4 – The system displays the message "Bank account is required"

* Given I already logged in
* And I have permission to update bank in
* And I am on the edit page of an existing bank in
* When I clear the column bank account

<figure><img src="../../.gitbook/assets/image (123).png" alt=""><figcaption></figcaption></figure>

* And I click submit button

<figure><img src="../../.gitbook/assets/image (124).png" alt=""><figcaption></figcaption></figure>

* Then I should see the message "Bank account is required" below the bank account column

<figure><img src="../../.gitbook/assets/image (125).png" alt=""><figcaption></figcaption></figure>

## EB.2.5 – The system displays the message "Payment from is required"

* Given I already logged in
* And I have permission to update bank in
* And I am on the edit page of an existing bank in
* When I clear the column payment from

<figure><img src="../../.gitbook/assets/image (36).png" alt=""><figcaption></figcaption></figure>

* And I click submit button

<figure><img src="../../.gitbook/assets/image (37).png" alt=""><figcaption></figcaption></figure>

* Then I should see the message "Payment from is required" below the payment from column

<figure><img src="../../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

## EB.2.6 – The system displays the message "Account is required"

* Given I already logged in
* And I have permission to update bank in
* And I am on the edit page of an existing bank in
* When I clear the column account

<figure><img src="../../.gitbook/assets/image (39).png" alt=""><figcaption></figcaption></figure>

* And I click submit button

<figure><img src="../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

* Then I should see the message "Account is required" below the account column

<figure><img src="../../.gitbook/assets/image (41).png" alt=""><figcaption></figcaption></figure>

## EB.2.7 – The system displays the message "Amount is required"

* Given I already logged in
* And I have permission to update bank in
* And I am on the edit page of an existing bank in
* When I clear the column amount

<figure><img src="../../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

* And I click submit button

<figure><img src="../../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

* Then I should see the message "Amount is required" below the amount column

<figure><img src="../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>

## EB.2.8 – The system displays the message "Amount must be filled with data numbers"

* Given I already logged in
* And I have permission to update bank in
* And I am on the edit page of an existing bank in
* When I type "xxwed" into column amount

<figure><img src="../../.gitbook/assets/image (45).png" alt=""><figcaption></figcaption></figure>

* And I click submit button

<figure><img src="../../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

* Then I should see the message "Amount must be filled with data numbers" below the amount column

<figure><img src="../../.gitbook/assets/image (47).png" alt=""><figcaption></figcaption></figure>

## EB.2.9 – The system displays the message "Successfully updated"

* Given I already logged in
* And I have permission to update bank in
* And I am on the edit page of an existing bank in
* When I change the bank account to "10210 BANK BCA GIRO KE - 4 258807881"

<figure><img src="../../.gitbook/assets/image (49).png" alt=""><figcaption></figcaption></figure>

* And I change the payment from to "\[CUS-103] PAK ROBBY"

<figure><img src="../../.gitbook/assets/image (50).png" alt=""><figcaption></figcaption></figure>

* And I change the account to "HONORARIUM KONSULTAN"

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

* And I change the notes to "testing update"

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

* And I change the amount to "200.000"

<figure><img src="../../.gitbook/assets/image (53).png" alt=""><figcaption></figcaption></figure>

* And I click submit button

<figure><img src="../../.gitbook/assets/image (126).png" alt=""><figcaption></figcaption></figure>

* Then I should see the message "Successfully updated"

<figure><img src="../../.gitbook/assets/image (128).png" alt=""><figcaption></figcaption></figure>

* And I should be redirected to the detail page

<figure><img src="../../.gitbook/assets/image (129).png" alt=""><figcaption></figcaption></figure>

* And the detail page should display the updated data
* And the system will update the journal entry as shown below.
  * Remove previous journal&#x20;

| Account                                | Debit      | Credit     |
| -------------------------------------- | ---------- | ---------- |
| {HONORARIUM KONSULTAN}                 | Rp.100.000 |            |
| {10210 BANK BCA GIRO KE - 4 258807881} |            | Rp.100.000 |

* &#x20;Record new journal&#x20;

| Account                                | Debit      | Credit     |
| -------------------------------------- | ---------- | ---------- |
| {10210 BANK BCA GIRO KE - 4 258807881} | Rp.200.000 |            |
| {HONORARIUM KONSULTAN}                 |            | Rp.200.000 |

