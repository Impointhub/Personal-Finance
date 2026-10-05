# Reject Cash Out

## BO. 7.1: User redirect to login page

* `GIVEN` user visit `/finance/point/cash-out` url without signin
* `THEN` user redirected to `Sign In` page

![](<../../.gitbook/assets/image (430)>)

## BO.7.2: The system does not display the approval button

* Given the user on the page `/finance/point/cash-out`
* And the user already logged in
* And the user don't have permission `approval_cash_out`
* And the user have data "CO-001"
* Then user can't see button approval

![](<../../.gitbook/assets/image (431)>)

## CO.7.3: Cash out approval status becomes rejected

* Given the user on the page `/finance/point/cash-out`
* And the user already logged in
* And the user have permission `approval_cash_out`
* And the user have data "CO-001"
* When the user click data "CO-001"
* And the user type "Biaya Terlalu Besar" into column "Approval Notes"
* And the user click button "Reject"

![](<../../.gitbook/assets/image (432)>)

* Then user can view notification "Success Rejected"
* And status approval form becomes rejected
* And reason reject show on the detail page
