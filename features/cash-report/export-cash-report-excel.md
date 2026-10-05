# Export Cash Report (Excel)

## EE1: System saves export in Excel format

* Given I already logged in
* And I have permission to read cash report
* And I on the page "https://test.app.point.red/finance/point/report/cash"
* And I already select filter
* When I click "Export to Excel"

![](<../../.gitbook/assets/image (437)>)

* Then the system generates the Excel file
* And the system displays the message "Your Excel file for Cash Report has been generated."

![](<../../.gitbook/assets/image (438)>)

* And the system generate excel as format [https://docs.google.com/spreadsheets/d/1a\_J0AHqpnn39AqlGJGcThcYIcQKZzNjx/edit?usp=sharing\&ouid=100441136837797679779\&rtpof=true\&sd=true](https://docs.google.com/spreadsheets/d/1a_J0AHqpnn39AqlGJGcThcYIcQKZzNjx/edit?usp=sharing\&ouid=100441136837797679779\&rtpof=true\&sd=true)
