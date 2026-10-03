# Bug Report

**Bug ID:** `BUG-002`

**Title:** Checkout displays only First Name validation when all required fields are empty

**Severity / Priority:** Medium / Medium · **Environment:** Google Chrome 153.0.8010.53 (64-bit), Windows

**Affected requirement(s):** REQ-4.2, SHOP-214, TC-16

**Steps to reproduce:**
1. Log in to https://www.saucedemo.com as `standard_user` / `secret_sauce`.
2. Add any product to the cart.
3. Open the cart and click **Checkout**.
4. Leave First Name empty.
5. Leave Last Name empty.
6. Leave Postal Code empty.
7. Click **Continue**.
8. Click **Continue** again without entering any values.

**Expected result:** User remains on the Checkout Information page and validation messages are displayed for all three required fields: First Name, Last Name, and Postal Code.

**Actual result:** User remains on the Checkout Information page. All three fields are marked invalid, but only the message **"Error: First Name is required"** is displayed. Repeating the action produces the same result.

**Evidence:** `BUG-002_checkout_validation.png` — Screenshot captured during TC-16 execution showing all three fields marked invalid and the First Name validation message.

**Status:** Open

**Notes:** The behavior is reproducible. TC-16 fails against the agreed SHOP-214 acceptance criteria.