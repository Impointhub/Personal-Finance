# Detail Cash In

## CI.4.1 – Redirect to the login page when user is not logged in

* Given I have not logged in
* When I type `/finance/point/cash` into browser
* Then I should be redirected to the login page

![](<../../.gitbook/assets/image (153)>)

## CI.4.2 – Redirect to the forbidden page when user does not have permission to access Cash In detail

* Given I already logged in
* And I do not have permission to read cash in
* When I type `/finance/point/cash/` into browser
* Then I should be redirected to the forbidden page

![](<../../.gitbook/assets/image (155)>)

## CI.4.3 – The system displays the detail of the selected Cash In transaction

* Given I already logged in
* And I have permission to read cash in
* When I type `/finance/point/cash/in/1` into browser
* Then I should see the cash in detail page

![](<../../.gitbook/assets/image (157)>)
