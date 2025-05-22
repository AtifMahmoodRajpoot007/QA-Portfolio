# 🐞 Bug Report: Mobile Login Issue

---

## 🔍 Summary
Users are experiencing **login failures** on the mobile app. Upon submitting their credentials, the login screen either **freezes** or displays an error message, preventing successful access.

---

## 🛠️ Environment
- **App Version:** 2.5.1  
- **Platforms Affected:**  
  - iOS 15.4 (iPhone 12)  
  - Android 12 (Samsung Galaxy S21)  
- **Network Conditions:**  
  - Wi-Fi (various networks)  
  - Cellular data (4G/5G)  
- **Frequency:** Intermittent (~60% of attempts fail)

---

## 🧭 Steps to Reproduce
1. Launch the mobile app on a supported device.
2. Navigate to the **Login** screen.
3. Enter a valid **username** and **password** combination.
4. Tap the **Login** button.
5. Observe the behavior.

---

## 🎯 Expected Result
- The user should be authenticated successfully.
- The app should redirect the user to the **Home screen** immediately after login.
- No freezing or error messages should appear.

---

## 🚫 Actual Result
- The **Login** button becomes unresponsive after tapping.
- An error popup is displayed:  
  > **"Unable to connect to server."**
- The app freezes completely, requiring a **force close and restart** to recover.
- This behavior happens inconsistently, causing **frustration** for users.

---

## 📋 Additional Details
- **Web and desktop app versions work flawlessly**, ruling out backend-wide issues.
- No recent backend deployments or API changes reported in the last 24 hours.
- Network conditions (Wi-Fi or mobile data) do not influence occurrence.
- Error reproducibility rate is approximately **60%**, making it a high-impact, intermittent bug.
- User reports indicate the issue sometimes resolves after multiple retry attempts, but this is not guaranteed.
- Crash and error logs have been collected and attached below for deeper analysis.

---

## 🐞 Logs / Screenshots

### 📸 Login Error Screenshot  
!![Login Error Screenshot](login_error.png)


---

### 📝 Excerpt from Error Logs
```plaintext
[2025-05-21 14:32:10] ERROR: Network timeout while attempting to reach authentication API.
[2025-05-21 14:32:10] WARN: Retry attempt 1 failed.
[2025-05-21 14:32:12] ERROR: Server returned 503 Service Unavailable.
[2025-05-21 14:32:12] INFO: User login request aborted due to network failure.
