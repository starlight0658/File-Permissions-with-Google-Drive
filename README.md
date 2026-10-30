# File Permissions with Google Drive

**Google Drive · Google Docs · Google Sheets · Access Control · Permission Testing**

## Overview

Performed a hands-on file-sharing and access-control lab using Google Drive, Google Docs, and Google Sheets. Compared **Restricted**, **Anyone with the link — Viewer**, and **Anyone with the link — Editor** settings; tested access from a separate Safari private-browsing session; examined parent-folder sharing; and reviewed individual-user authorization and removal.

The screenshots document the settings used **and the observed results**, including an instance where the spreadsheet still appeared as **View only**. No assumption is made that changing a setting automatically grants effective access to every file.

## Lab environment

| Component | Use |
| --- | --- |
| Google Drive | File and folder sharing, link access, individual permissions |
| Google Docs | Test document, read-only and editing validation |
| Google Sheets | Test spreadsheet and permission verification |
| Safari Private Browsing | Separate visitor session to test effective access |
| Test resources | `My cat document`, `Public access`, `Weekly budget` |

## Permission scenarios

| Scenario | Access configured or tested | Screenshot evidence |
| --- | --- | --- |
| Document shared by link | Viewer; read-only visitor access | 06–08 |
| Document shared by link | Editor; separate-session text entry | 09–10 |
| Document restricted | Restricted; sign-in prompt observed | 11–12 |
| Shared parent folder | Anyone with the link — Viewer; document moved into folder | 13–18 |
| Shared spreadsheet | Editing test; later `View only` observation | 19–22 |
| Named collaborator | Editor on a Restricted folder; removal staged, not yet saved | 23–24 |

## Screenshot walkthrough

All **24 screenshots** are displayed below, in the order captured. Personal account identifiers and the unique document URL have been redacted before publication.


### Create a test document


**01. Start a new Google Doc**  
Opened Google Drive’s Google Docs creation menu to create a test document.

![01. Start a new Google Doc](screenshots/01-new-google-doc.png)


**02. Create the test document**  
Created **My cat document** and entered the initial word, `Cat`.

![02. Create the test document](screenshots/02-create-test-document.png)


**03. Locate the document in Drive**  
Verified the new document appeared in Google Drive’s recent files.

![03. Locate the document in Drive](screenshots/03-locate-document.png)


### Test public Viewer and Editor access


**04. Prepare an independent access test**  
Opened the document link for testing in a separate private-browsing session. The document URL is redacted.

![04. Prepare an independent access test](screenshots/04-copy-document-link.png)


**05. Observe initial private-session access**  
The private session displayed a Google sign-in screen before public-link access was configured.

![05. Observe initial private-session access](screenshots/05-private-session-login.png)


**06. Configure public Viewer access**  
Set **General access → Anyone with the link → Viewer**, without allowing public editing.

![06. Configure public Viewer access](screenshots/06-anyone-link-viewer.png)


**07. Verify the Viewer experience**  
Opened the test document without the owner’s signed-in session; **Request edit access** was displayed.

![07. Verify the Viewer experience](screenshots/07-viewer-document.png)


**08. Compare owner and visitor sessions**  
Viewed the same document side by side in the owner and private sessions to validate read access without editing rights.

![08. Compare owner and visitor sessions](screenshots/08-owner-vs-viewer.png)


**09. Grant link-based Editor access**  
Changed **Anyone with the link** to **Editor** for a controlled editing test.

![09. Grant link-based Editor access](screenshots/09-public-link-editor.png)


**10. Confirm editing in the private session**  
Added text from the separate session after Editor permission was enabled.

![10. Confirm editing in the private session](screenshots/10-private-editor-test.png)


### Restore restricted access


**11. Return the document to Restricted**  
Changed **General access** back to **Restricted** to remove anonymous link access.

![11. Return the document to Restricted](screenshots/11-restore-restricted.png)


**12. Observe signed-in requirement**  
The separate session showed a sign-in prompt when accessing the document under the changed access conditions.

![12. Observe signed-in requirement](screenshots/12-private-session-signin.png)


### Configure and test folder sharing


**13. Create a shared parent folder**  
Created the **Public access** folder to test folder-level sharing behavior.

![13. Create a shared parent folder](screenshots/13-create-shared-folder.png)


**14. Open folder sharing settings**  
Used the folder’s context menu to open its sharing permissions.

![14. Open folder sharing settings](screenshots/14-folder-sharing-menu.png)


**15. Configure folder Viewer access**  
Set the folder to **Anyone with the link → Viewer**.

![15. Configure folder Viewer access](screenshots/15-folder-viewer-access.png)


**16. Review the access-change warning**  
Moved the document into the shared folder and observed Google Drive’s warning that visibility could change.

![16. Review the access-change warning](screenshots/16-move-permission-warning.png)


**17. Verify document placement**  
Confirmed **My cat document** appeared inside the **Public access** folder.

![17. Verify document placement](screenshots/17-document-inside-folder.png)


**18. Retest document from the private window**  
The visitor could view the document, while **Request edit access** remained visible.

![18. Retest document from the private window](screenshots/18-visitor-read-only-after-move.png)


### Test a shared Google Sheet and effective access


**19. Add a second file for testing**  
The shared folder contained both **My cat document** and a **Weekly budget** Google Sheet.

![19. Add a second file for testing](screenshots/19-test-files-in-folder.png)


**20. Test a spreadsheet editing session**  
Opened the spreadsheet in a private session and demonstrated text entry.

![20. Test a spreadsheet editing session](screenshots/20-sheet-edit-test.png)


**21. Change folder link permission to Editor**  
Selected **Anyone with the link → Editor** and reviewed the available Viewer, Commenter, and Editor roles.

![21. Change folder link permission to Editor](screenshots/21-folder-editor-permission.png)


**22. Observe the spreadsheet’s effective access**  
A later private-window view displayed **View only**, showing why actual access should be tested after changing sharing settings.

![22. Observe the spreadsheet’s effective access](screenshots/22-sheet-view-only-test.png)


### Grant and stage revocation of individual access


**23. Share with a named collaborator**  
Set **General access → Restricted** and displayed a named collaborator with **Editor** access. Identifying details are redacted.

![23. Share with a named collaborator](screenshots/23-specific-person-editor.png)


**24. Stage removal of collaborator access**  
Selected **Remove** for the collaborator. The dialog shows **Pending changes**, so a subsequent **Save** is required to finalize removal.

![24. Stage removal of collaborator access](screenshots/24-remove-collaborator.png)


## Skills demonstrated

- Applied Google Drive **link-sharing roles** and **restricted access** settings.
- Validated **effective permissions** using a separate browser session rather than trusting configuration alone.
- Compared file and parent-folder sharing and observed access-change warnings.
- Tested **read-only** and **write** scenarios in Docs and Sheets.
- Applied **individual-user access** and inspected the staged removal workflow.

> **Security note:** The repository contains anonymized screenshots only. The final screenshot displays removal as **pending**; it does not independently prove the permission change was saved.
