# Export Excel Bank Report

## EE1: System saves export in PDF format

* Given I already logged in
* And I have permission to read bank report
* And I on the page "/finance/point/report/bank"

![](<../../.gitbook/assets/image (473)>)

* And I already select filter

![](<../../.gitbook/assets/image (474)>)

* When I click "Export to Excel"

![](<../../.gitbook/assets/image (475)>)

* Then the system generates the Excel file
* And the system displays the message "Your Excel file for Bank Report has been generated."

![](<../../.gitbook/assets/image (476)>)

* And the system generates the file excel as a format : [https://docs.google.com/spreadsheets/d/1\_\_IeuQIHPYB3ZK7QfKjGsS\_VeIAOMbsg/edit?usp=sharing\&ouid=100441136837797679779\&rtpof=true\&sd=true](https://docs.google.com/spreadsheets/d/1__IeuQIHPYB3ZK7QfKjGsS_VeIAOMbsg/edit?usp=sharing\&ouid=100441136837797679779\&rtpof=true\&sd=true)
