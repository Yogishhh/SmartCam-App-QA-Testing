# Untitled

# 📄 Mobile App Testing Project

---

## 🧾 Project Overview

Application Name: SmartCam App

Platform: iOS

Tester: Yogish

Testing Type: Manual Testing

Modules Tested: Signup & Login

---

## 🎯 Objective

To verify the functionality, validation, and error handling of the Signup and Login features and ensure correct behavior under different conditions.

---

## 🔍 Scope of Testing

Included:

- Input validation
- Error handling
- User flow (Signup → Login)
- Network behavior

Not Included:

- Backend/database testing
- Performance testing

---

## 🧪 Test Scenarios

1. Verify signup with valid details
2. Verify signup with invalid username
3. Verify signup with invalid password
4. Verify signup without internet
5. Verify signup without accepting terms
6. Verify multiple clicks on signup
7. Verify login with valid credentials
8. Verify login with invalid credentials

---

## 📋 Test Cases

### 🧪 TC01 – Signup with valid details

Steps:

1. Open app
2. Navigate to Signup
3. Enter valid username (8–14 alphanumeric)
4. Enter valid password (10–14 characters)
5. Enter valid email
6. Accept Terms & Conditions
7. Click “Create Account”

Expected Result:

Account should be created successfully

Actual Result:

Shows “Network connection is unstable”

Status: ❌ Fail

---

### 🧪 TC02 – Invalid Username

Steps:

1. Enter username with special characters (e.g., 869.4.ixyxtizh)
2. Fill other fields correctly
3. Click “Create Account”

Expected Result:

Username should be rejected

Actual Result:

Username accepted

Status: ❌ Fail

---

### 🧪 TC03 – Invalid Password

Steps:

1. Enter invalid password
2. Click “Create Account”

Expected Result:

Error message should be displayed

Actual Result:

Validation works correctly

Status: ✅ Pass

---

### 🧪 TC04 – Signup without Internet

Steps:

1. Turn off internet
2. Enter valid details
3. Click “Create Account”

Expected Result:

Proper network error message

Actual Result:

Shows generic network error

Status: ⚠️ Partial

---

### 🧪 TC05 – Multiple Clicks on Signup

Steps:

1. Enter valid details
2. Tap “Create Account” multiple times

Expected Result:

Only one request should be processed

Actual Result:

Inconsistent errors displayed

Status: ❌ Fail

---

## 🐞 Bug Reports

### 🐞 Bug 1 – Signup fails with valid data

Type: Functional Bug

Severity: High

Priority: High

Steps to Reproduce:

1. Enter valid details
2. Click “Create Account”

Actual Result:

Account is not created

Expected Result:

Account should be created successfully

---

### 🐞 Bug 2 – Incorrect error message

Type: Error Handling Bug

Severity: Medium

Description:

App shows “Network connection is unstable” even when internet is working

---

### 🐞 Bug 3 – Username validation issue

Type: Validation Bug

Severity: Medium

Description:

App accepts non-alphanumeric characters in username

---

### 🐞 Bug 4 – Inconsistent error messages

Type: Functional Bug

Severity: Medium

Description:

Different error messages shown for same action

---

## 📸 Evidence

![IMG_9402.png](Untitled/IMG_9402.png)

![IMG_9400.png](Untitled/IMG_9400.png)

![IMG_9399.png](Untitled/IMG_9399.png)

![IMG_9398.png](Untitled/IMG_9398.png)

---

## 📊 Observations

- Signup functionality is not working with valid inputs
- Error messages are misleading
- Validation rules are not properly enforced

---

## ✅ Conclusion

The Signup module contains critical functional and validation issues that prevent successful user registration. Fixes are required before release.

---