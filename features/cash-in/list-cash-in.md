# List Cash In

## CI.3.1 – Redirect to the login page when user is not logged in

* Given I have not logged in
* When I type `/finance/point/cash` into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (166)>)

## CI.3.2 – Redirect to the forbidden page

* Given I already logged in
* And I do not have permission to read cash in
* When I type `/finance/point/cash` into browser
* Then I should be redirected to the forbidden page

![](<../../.gitbook/assets/image (167)>)

## CI.3.3 – The system displays the message "you don't have any data yet"

* Given I already logged in
* And I have permission to read cash in
* And I don't have the cash in data yet
* When I type `/finance/point/cash/` into browser
* Then I can see text "you don't have any data yet"

![](<../../.gitbook/assets/image (168)>)

## CI.3.4 – The system displays all Cash In data that has been entered by the user

* Given I already logged in
* And I have permission to read cash in
* And I already have data cash in
* When I type `/finance/point/cash/` into browser
* Then the system dispays all cash in data that has been entered

![](<../../.gitbook/assets/image (169)>)
