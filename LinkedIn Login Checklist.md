# LinkedIn Login Checklist

## Priority Legend
| Priority | Description |
|----------|------------|
| P0 | Critical: must-have, blocks login |
| P1 | High: important functionality, no workaround |
| P2 | Medium: nice to have, partial impact |
| P3 | Low: cosmetic or minor UX issue |

## Test Cases
| ID | Test Name | Priority | Description | Steps of Execution | Test Data | Expected Results | Status |
|----|-----------|---------|-------------|------------------|-----------|-----------------|--------|
| TC00 | Login page opens correctly | P0 | Check that login page loads | 1. Open https://www.linkedin.com/login;<br>2. Verify email and password fields, LinkedIn logo, buttons “Continue with Google” and “Sign in with Apple” are visible;<br>3. Verify links “Forgot password?” and “Join now” are visible. | - | Login page loads with all listed elements visible | Not Executed |
| TC01 | Valid login | P0 | Login with valid credentials | 1. Enter valid email or phone number;<br>2. Enter valid password;<br>3. Click “Sign in” | test@example.com / ValidPass123 OR +1234567890 / ValidPass123 | User is redirected to https://www.linkedin.com/feed/ | Not Executed |
| TC02 | Invalid login (wrong credentials) | P1 | Error message for invalid email or password | 1. Enter valid email or phone number;<br>2. Enter wrong password;<br>3. Click “Sign in” | test@example.com / WrongPass123 | Generic error: "Wrong email or password. Try again or create an account." | Not Executed |
| TC03 | Invalid login (non-existing account) | P1 | Error message for email or phone not registered | 1. Enter invalid email or phone number;<br>2. Enter any password;<br>3. Click “Sign in” | wrong@example.com / WrongPass321 OR +0987654321 / WrongPass321 | Generic error: "Wrong email or password. Try again or create an account." | Not Executed |
| TC04 | Empty input fields | P0 | Validation for empty inputs | 1. Leave email and password fields empty;<br>2. Click “Sign in” | - | Validation error: indicating fields are required | Not Executed |
| TC05 | Only email entered | P2 | Validation for missing password | 1. Enter email;<br>2. Leave password-field empty;<br>3. Click “Sign in” | test@example.com | Validation error: Password is required - Please enter a password | Not Executed |
| TC06 | Only password entered | P2 | Validation for missing email or phone number | 1. Leave email-field empty;<br>2. Enter password;<br>3. Click “Sign in” | ValidPass123 | Validation error: Email is required - Please enter an email address or phone number. | Not Executed |
| TC07 | Login with leading/trailing spaces | P2 | Ignore spaces in input fields | 1. Enter email with spaces before/after;<br>2. Enter password with spaces;<br>3. Click “Sign in” | " test@example.com " / " ValidPass123 " | User logs in successfully, spaces trimmed | Not Executed |
| TC08 | Password field masking | P3 | Check password field is masked | 1. Enter password in field | ValidPass123 | Password characters masked (dots shown instead of characters) | Not Executed |
| TC09 | "Forgot password" link | P2 | Verify “Forgot password?” link works | 1. Click “Forgot password?” link | - | User is redirected to password recovery page | Not Executed |
| TC10 | Password visibility toggle | P3 | Show/hide password functionality | 1. Enter password;<br>2. Click visibility toggle icon | ValidPass123 | Password becomes visible/unmasked | Not Executed |
| TC11 | "Keep me logged in" checkbox | P3 | Verify functionality of "Keep me logged in" option | 1. Check the "Keep me logged in" checkbox;<br>2. Enter valid credentials;<br>3. Click “Sign in”;<br>4. Close and reopen browser | test@example.com / ValidPass123 OR +1234567890 / ValidPass123 | User remains logged in | Not Executed |
| TC12 | Caps Lock warning | P3 | Warning when Caps Lock is on | 1. Enable Caps Lock;<br>2. Focus on password field | ValidPass123 | Caps Lock warning message displayed | Not Executed |
| TC13 | Continue with Google button | P2 | Verify “Continue with Google” button works | 1. Click “Continue with Google” button | Google account details (if needed) | Google sign-in flow is triggered or window opens | Not Executed |
| TC14 | Sign in with Apple button | P2 | Verify “Sign in with Apple” button works | 1. Click “Sign in with Apple” button | Apple ID credentials (if needed) | Apple sign-in flow is triggered or window opens | Not Executed |
| TC15 | "Join now" link | P2 | Verify “Join now” link leads to registration | 1. Click “Join now” | - | Redirected to LinkedIn registration | Not Executed |
| TC16 | Invalid/special characters input | P1 | Check how system handles unsupported or special characters in login fields | 1. Enter invalid characters (e.g. !@#$%^&*<>"") in email or phone fields;<br>2. Enter any password;<br>3. Click “Sign in” | "<>\n""\ \n‘\n' OR 1=1; DROP TABLE users; --" | Generic error: “Wrong email or password. Try again or create an account.” No UI break or system error | Not Executed |
| TC17 | LinkedIn logo redirect | P2 | Verify that clicking the LinkedIn logo redirects appropriately | 1. Click the LinkedIn logo on the login page | - | User is redirected to https://www.linkedin.com/ (if not logged in) OR to https://www.linkedin.com/feed/ (if already logged in) | Not Executed |
| TC18 | Footer content | P3 | Verify footer elements and language selector on login page | 1. Scroll to page bottom;<br>2. Verify links: “User Agreement”, “Privacy Policy”, etc.;<br>3. Verify language selector is visible and works | - | All footer links and language selector are visible and functional | Not Executed |
