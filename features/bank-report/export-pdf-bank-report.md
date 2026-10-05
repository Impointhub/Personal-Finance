# Export PDF Bank Report

## EP1: System saves PDF export

* Given I already logged in
* And I have permission to read bank report
* And I on the page "/finance/point/report/bank"

![](<../../.gitbook/assets/image (477)>)

* And I already select filter

![](<../../.gitbook/assets/image (478)>)

* When I click "Export to PDF"

![](<../../.gitbook/assets/image (479)>)

* Then the system generates the PDF file
* And the system displays the message "Your PDF file for Bank Report has been generated."
* And the system generates PDF File as a format : [https://drive.google.com/file/d/1OKuPR05PM4ZAPjsg5skweDK1wgHIvc\_Y/view?usp=sharing](https://drive.google.com/file/d/1OKuPR05PM4ZAPjsg5skweDK1wgHIvc_Y/view?usp=sharing)
