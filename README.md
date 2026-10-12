# IT Helpdesk Lab — Jira Service Management

This project documents three IT support cases managed in Jira Service Management, covering investigation, troubleshooting, customer communication, verification, and resolution.

I created this lab to develop practical helpdesk skills and demonstrate how I investigate issues, document findings, and communicate with users.

## Skills Practiced

- Creating, assigning, and updating support tickets
- Asking questions to identify symptoms, scope, and access requirements
- Interpreting simulated network troubleshooting results
- Practicing identity verification and account-unlock workflows through role-play
- Troubleshooting macOS file permissions using Terminal
- Applying least privilege when restoring file access
- Writing internal technical notes and customer-facing replies
- Recording verification results and requesting customer confirmation

## Case 1: Connected to Wi-Fi but Unable to Browse Websites

A fictional employee reported that their laptop connected to office Wi-Fi but could not load websites or connect to Microsoft Teams.

Simulated results from `ipconfig`, `ping`, and `nslookup` pointed to an incorrect manually configured DNS server. The simulated fix restored the scenario’s approved automatic DNS settings, followed by successful DNS lookups, application checks, and customer confirmation.

The Jira ticket was resolved with the resolution **Fixed**.

## Case 2: Work Account Lockout After a Password Change

A fictional employee reported being unable to sign in after changing their password.

Through role-played investigation, I identified repeated attempts with the old password as the cause of the lockout. The scenario included simulated identity verification and an authorized account unlock. A password reset was unnecessary because the employee remembered the current password.

The fictional customer confirmed successful access, and the Jira ticket was resolved with the resolution **Fixed**.

## Case 3: Unable to Read a File on macOS

A fictional employee reported receiving “Permission denied” when attempting to read a text file.

I reproduced the issue on my Mac using a dedicated test file. Using `whoami` and `ls`, I confirmed that my local account owned the file and could access its parent folder, but the file’s permissions were set to `000`.

I applied `chmod 400` to grant owner-only read access, matching the scenario’s read-only requirement. I verified that the permissions changed to `-r--------` and that `cat` successfully displayed the file’s contents.

The diagnosis, fix, and verification were documented in Jira.

## Lab Scope

All ticket workflows were performed in Jira Service Management. Customer identities, business scenarios, and customer responses were fictional and role-played for training.

- **Case 1:** The Windows environment, diagnostic results, and DNS configuration changes were simulated.
- **Case 2:** Identity verification, account status checks, and the account unlock were simulated. No Windows or Active Directory account was modified.
- **Case 3:** The file-access error, permission checks, permission change, and verification were performed on my Mac using a dedicated test file. Commands ran under my local account; Alex was the fictional Jira customer, not a separate macOS user.

For Case 1, I used one Jira account as both customer and support agent. Later cases used separate Jira customer and agent accounts.

## Detailed Case Studies

Each case study includes investigation notes, troubleshooting steps, outcomes, and screenshots.

- [Case 1: Connected to Wi-Fi but Unable to Browse Websites](cases/01-dns-connectivity.md)
- [Case 2: Work Account Lockout After a Password Change](cases/02-account-lockout.md)
- [Case 3: Unable to Read a File on macOS](cases/03-macos-file-permissions.md)
