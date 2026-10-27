# 3-Step User Authentication

A PHP practice project implementing a multi-level login flow for a mock banking web application: password → security question → pattern-based "combination lock" step.

## Authentication flow (`front/`)

1. **Step 1 – Password** (`index.php`, `login_db.php`) — username/password login, with separate Admin/Employee user types.
2. **Step 2 – Security question** (`security_signup.php`, `security_signuprun.php`) — a secret question/answer set at signup, re-verified at login.
3. **Step 3 – Pattern** (`pattern_login.php`, `pattern_add.php`) — a 5-color click-sequence "pattern lock" set at signup and re-entered at login.

## Banking application (`front/banking/`)

The authentication flow gates a small banking app with role-based pages:
- **Admin** — add/edit/delete staff and customers
- **Staff** — approve/deny pending ATM card and cheque book requests
- **Customer** — view accounts, manage beneficiaries

## Notes

- Early coursework/learning project, not production-hardened: some pages use the deprecated `mysql_*` API alongside `mysqli_*`, and database credentials are hardcoded inline rather than loaded from environment config.
- `login/` contains unrelated standalone practice snippets from the same coursework (a basic HTML form, a couple of small Python exercises) — not part of the authentication flow itself.
