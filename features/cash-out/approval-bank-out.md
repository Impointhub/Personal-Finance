# Approval Bank Out

{% stepper %}
{% step %}
## CO.6.1: User redirect to login page

* `GIVEN` user visit `/finance/point/bank-out` url without signin
* `THEN` user redirected to `Sign In` page

![](<../../.gitbook/assets/image (427)>)
{% endstep %}

{% step %}
## CO.6.2: The system does not display the approval button

* Given the user on the page `/finance/point/bank-out`
* And the user already logged in
* And the user don't have permission `approval_bank_out`
* And the user have data "BO-001"
* When the user click "BO-001"
* Then user can't see the approval button

![](<../../.gitbook/assets/image (428)>)
{% endstep %}

{% step %}
## CO.6.3: Cash out approval status becomes approved

* Given the user on the page `/finance/point/cash-out`
* And the user already logged in
* And the user have permission `approval_cash_out`
* And the user have data "BO-001"
* When user click "BO-001"
* And user click button "approve"

![](<../../.gitbook/assets/image (429)>)

* Then user can view notification "Successfully Approved"
* And status approval form becomes approved
{% endstep %}
{% endstepper %}
