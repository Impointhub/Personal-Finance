# Edit Cash Out

## EC.F1 - Redirect to login page because user unauthenticated

* **Given** I have not logged in
* **When** I type /finance/point/cashout/1 into browser
* **Then** I should be redirected to the login page

![](<../../.gitbook/assets/image (369)>)

## EC.F2 - Redirect to the forbidden page because user don't have permission edit\_cash out

* **Given** I already logged in
* **And** I do not have permission to edit cash out
* **When** I open the page /finance/point/cashout/1/
* **Then** I can't see button edit on detail page&#x20;

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

## EC.F3 - The system displays the message "cash account is required" because the user didn't enter a cash account

* **Given** I already logged in
* **And** I have permission to edit cash out
* **And** I am on the page /finance/point/cashout/1
* **When** I click "Edit" button

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

* **And** the form is prefilled with the existing cash out data

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

* **And** the columns cash account and account display only the charts of accounts accessible to me
* **And** I clear column cash account

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

* **And** I click submit

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

* **Then** I should see the message "Cash account is required"

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

* **And** I should remain on the edit page

## EC.F4 - The system displays the message "Payment to is required" because the user didn't enter a payment to

* **Given** I already logged in
* **And** I have permission to edit cash out
* **And** I am on the page /finance/point/cashout/1
* **When** I click "Edit" button

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

* **And** the form is prefilled with the existing cash out data

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

* **And** the columns cash account and account display only the charts of accounts accessible to me
* **And** I clear column payment to

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

* **And** I click submit

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

* **Then** I should see the message "Payment to is required"

<figure><img src="../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

* **And** I should remain on the edit page

## EC.F5 - The system displays the message "account is required" because the user didn't enter an account

* **Given** I already logged in
* **And** I have permission to edit cash out
* **And** I am on the page /finance/point/cashout/1
* **When** I click "Edit" button

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

* **And** the form is prefilled with the existing cash out data

<figure><img src="../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

* **And** the columns cash account and account display only the charts of accounts accessible to me
* **And** I clear column account on the first row

<figure><img src="../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

* **And** I click submit

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

* **Then** I should see the message "Account is required"

<figure><img src="../../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

* **And** I should remain on the edit page

## EC.F6 - The system displays the message "amount is required" because the user didn't enter an amount

* **Given** I already logged in
* **And** I have permission to edit cash out
* **And** I am on the page /finance/point/cashout/1
* **When** I click "Edit" button

<figure><img src="../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

* **And** the form is prefilled with the existing cash out data

<figure><img src="../../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

* **And** the columns cash account and account display only the charts of accounts accessible to me
* **And** I clear column amount on the first row

<figure><img src="../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

* **And** I click submit

<figure><img src="../../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

* **Then** I should see the message "Amount is required"

<figure><img src="../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

* **And** I should remain on the edit page

## EC.F7 - The system displays the message "Please enter a valid amount using numbers only." because the user didn't enter an valid amount

* **Given** I already logged in
* **And** I have permission to edit cash out
* **And** I am on the page /finance/point/cashout/1
* **When** I click "Edit" button

<figure><img src="../../.gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

* **And** the form is prefilled with the existing cash out data

<figure><img src="../../.gitbook/assets/image (146).png" alt=""><figcaption></figcaption></figure>

* **And** the columns cash account and account display only the charts of accounts accessible to me
* **And** I type "abc" into column amount on the first row

<figure><img src="../../.gitbook/assets/image (147).png" alt=""><figcaption></figcaption></figure>

* **And** I click submit

<figure><img src="../../.gitbook/assets/image (148).png" alt=""><figcaption></figcaption></figure>

* **Then** I should see the message "Please enter a valid amount using numbers only"

<figure><img src="../../.gitbook/assets/image (149).png" alt=""><figcaption></figcaption></figure>

* **And** I should remain on the edit page

## EC.F8 - The system displays the message "Amount must be greater than zero." because the user didn't enter an amount greater than zero

* **Given** I already logged in
* **And** I have permission to edit cash out
* **And** I am on the page /finance/point/cashout/1
* **When** I click "Edit" button

<figure><img src="../../.gitbook/assets/image (150).png" alt=""><figcaption></figcaption></figure>

* **And** the form is prefilled with the existing cash out data

<figure><img src="../../.gitbook/assets/image (151).png" alt=""><figcaption></figcaption></figure>

* **And** the columns cash account and account display only the charts of accounts accessible to me
* **And** I type "0" into column amount on the first row

<figure><img src="../../.gitbook/assets/image (152).png" alt=""><figcaption></figcaption></figure>

* **And** I click submit

<figure><img src="../../.gitbook/assets/image (153).png" alt=""><figcaption></figcaption></figure>

* **Then** I should see the message "Amount must be greater than zero"

<figure><img src="../../.gitbook/assets/image (154).png" alt=""><figcaption></figcaption></figure>

* **And** I should remain on the edit page

## EC.S1 : The system displays the message "Successfully updated"

* **Given** I already logged in
* **And** I have permission to edit cash out
* **And** I am on the page /finance/point/cashout/1
* **When** I click "Edit" button

<figure><img src="../../.gitbook/assets/image (155).png" alt=""><figcaption></figcaption></figure>

* **And** the form is prefilled with the existing cash out data

<figure><img src="../../.gitbook/assets/image (156).png" alt=""><figcaption></figcaption></figure>

* **And** the columns cash account and account display only the charts of accounts accessible to me
* **And** I type "Edit testing" into column notes on the first row

<figure><img src="../../.gitbook/assets/image (157).png" alt=""><figcaption></figcaption></figure>

* **And** I type "150000" into column amount on the first row

<figure><img src="../../.gitbook/assets/image (158).png" alt=""><figcaption></figcaption></figure>

* **And** I click submit

<figure><img src="../../.gitbook/assets/image (159).png" alt=""><figcaption></figcaption></figure>

* **Then** I should see the notification "Successfully updated"
* **And** I should be redirected to the cash out detail page
