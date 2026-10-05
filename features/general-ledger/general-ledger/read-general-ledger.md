# Read General Ledger

## GL1: User redirect to login page

* Given I have not logged in
* When I type `/accounting/general-ledger` into browser
* Then I should be redirected to the login page

![](../../../.gitbook/assets/image)

## GL2: Redirect to forbidden page

* Given I already logged in
* And I do not have permission to read general ledger
* When I type `/accounting/general-ledger` create into browser
* Then I redirect to forbidden page

![](<../../../.gitbook/assets/image (1)>)

## GL3: Displaying General Ledger data

* Given I logged in
* And I has permission to read the general ledger report
* When I navigates to "/accounting/general-ledger"

![](<../../../.gitbook/assets/image (2)>)

* And I selects "01-08-2026" on column date from

![](<../../../.gitbook/assets/image (3)>)

* And I selects "31-08-2026" on column date to

![](<../../../.gitbook/assets/image (4)>)

* And I selects account "10101 · Cash on hand"

![](https://pointhubdocs.gitbook.io/erpsaas/~gitbook/image?url=https%3A%2F%2F4040199489-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FSt0IMR50HP72xQrcq86I%252Fuploads%252FtNxMObb7vQLueXvbseC0%252Fimage.png%3Falt%3Dmedia%26token%3D4f2f0ec5-66c2-43e4-9a39-5d3bb6d49f8a\&width=768\&dpr=3)

* Then the system displays the general ledger data for the selected date range and account

![](<../../../.gitbook/assets/image (5)>)
