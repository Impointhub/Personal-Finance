# Edit Cash In

### Edit Cash In

#### EC.2.1 – Redirect to the login page

* Given I have not logged in
* When I type `/finance/point/cash/in/{id}/edit` into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (170)>)

#### EC.2.2 – Redirect to the forbidden page

* Given I already logged in
* And I do not have permission to update cash in
* When I type `/finance/point/cash/in/{id}/edit` into browser
* Then I should be redirected to the forbidden page

![](<../../.gitbook/assets/image (171)>)

#### EC.2.3 – The system displays the existing data on the edit form

* Given I already logged in
* And I have permission to update cash in
* And I am on the page `/finance/point/cash/`
* When I click on an existing cash in transaction on the list page

<figure><img src="../../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure>

* And I click the edit button on the detail page

<figure><img src="../../.gitbook/assets/image (98).png" alt=""><figcaption></figcaption></figure>

* Then I should be redirected to the edit page

<figure><img src="../../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

* And I should see the payment date, cash account, payment from, notes, account, amount, and allocation columns already filled with the existing data

<figure><img src="../../.gitbook/assets/image (101).png" alt=""><figcaption></figcaption></figure>

#### EC.2.4 – The system displays the message "Cash account is required"

* Given I already logged in
* And I have permission to update cash in
* And I am on the edit page of an existing cash in
* When I clear the column cash account

<figure><img src="../../.gitbook/assets/image (102).png" alt=""><figcaption></figcaption></figure>

* And I click submit button

<figure><img src="../../.gitbook/assets/image (103).png" alt=""><figcaption></figcaption></figure>

* Then I should see the message "Cash account is required" below the cash account column

<figure><img src="../../.gitbook/assets/image (104).png" alt=""><figcaption></figcaption></figure>

#### EC.2.5 – The system displays the message "Payment from is required"

* Given I already logged in
* And I have permission to update cash in
* And I am on the edit page of an existing cash in
* When I clear the column payment from

<figure><img src="../../.gitbook/assets/image (105).png" alt=""><figcaption></figcaption></figure>

* And I click submit button

<figure><img src="../../.gitbook/assets/image (106).png" alt=""><figcaption></figcaption></figure>

* Then I should see the message "Payment from is required" below the payment from column

<figure><img src="../../.gitbook/assets/image (107).png" alt=""><figcaption></figcaption></figure>

#### EC.2.6 – The system displays the message "Account is required"

* Given I already logged in
* And I have permission to update cash in
* And I am on the edit page of an existing cash in
* When I clear the column account

<figure><img src="../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>

* And I click submit button

<figure><img src="../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>

* Then I should see the message "Account is required" below the account column

<figure><img src="../../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>

#### EC.2.7 – The system displays the message "Amount is required"

* Given I already logged in
* And I have permission to update cash in
* And I am on the edit page of an existing cash in
* When I clear the column amount

<figure><img src="../../.gitbook/assets/image (111).png" alt=""><figcaption></figcaption></figure>

* And I click submit button

<figure><img src="../../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>

* Then I should see the message "Amount is required" below the amount column

<figure><img src="../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>

#### EC.2.8 – The system displays the message "Amount must be filled with data numbers"

* Given I already logged in
* And I have permission to update cash in
* And I am on the edit page of an existing cash in
* When I type "xxwed" into column amount

<figure><img src="../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>

* And I click submit button

<figure><img src="../../.gitbook/assets/image (115).png" alt=""><figcaption></figcaption></figure>

* Then I should see the message "Amount must be filled with data numbers" below the amount column

<figure><img src="../../.gitbook/assets/image (116).png" alt=""><figcaption></figcaption></figure>

#### EC.2.9 – The system displays the message "Successfully updated"

* Given I already logged in
* And I have permission to update cash in
* And I am on the edit page of an existing cash in
* When I change the payment from "\[CUS-103] PAK ROBBY" to "\[CUS-88] Bu sari"

<figure><img src="../../.gitbook/assets/image (117).png" alt=""><figcaption></figcaption></figure>

* And I change the notes from "testing" to "testing update"

<figure><img src="../../.gitbook/assets/image (118).png" alt=""><figcaption></figcaption></figure>

* And I change amount from "100000" to "200000"

<figure><img src="../../.gitbook/assets/image (119).png" alt=""><figcaption></figcaption></figure>

* And I click submit button

<figure><img src="../../.gitbook/assets/image (120).png" alt=""><figcaption></figcaption></figure>

* Then I should see the message "Successfully updated"

<figure><img src="../../.gitbook/assets/image (121).png" alt=""><figcaption></figcaption></figure>

* And I should be redirected to the detail page

<figure><img src="../../.gitbook/assets/image (122).png" alt=""><figcaption></figcaption></figure>

* And the detail page should display the updated data
*   And the system will update the journal entry as shown below.

    * Remove previous jurnal&#x20;

    | Account                | Debit      | Credit     |
    | ---------------------- | ---------- | ---------- |
    | {HONORARIUM KONSULTAN} | Rp.100.000 |            |
    | {KAS BESAR}            |            | Rp.100.000 |



    * Record jurnal&#x20;

| Account                | Debit      | Credit     |
| ---------------------- | ---------- | ---------- |
| {KAS BESAR}            | Rp.200.000 |            |
| {HONORARIUM KONSULTAN} |            | Rp.200.000 |



*



*
