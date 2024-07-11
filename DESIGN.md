# Goal

Allow editors in an organization to import bank statements in mt940 format to a common beancount ledger.

## Why

Beancount is double-entry accounting software with some strong guarantees on correctness. Hackerspace Pomorze has rather simple bank statements and importing can be automated to some extent. Also not everyone helping with finances is tech savvy with command line tools like beancount.

# Stack

* Python: beancount is written in Python, has libs with good mt940 support.
* git + GitHub: as data storage. Ledger is already here and it's the best way to audit it.

# How

1. Authorize users via SSO. No time for password management.
2. Present an upload page to drop statements.
3. Import them with user-supplied importers written in python.
4. Allow for basic edits before upload.
5. Push to repository as a branch and redirect to PR creation
