# 🛫 US-Bangla Airlines — Bug Report (QA)

A professional **Quality Assurance Bug Report** for the US-Bangla Airlines website ([usbair.com](https://usbair.com/)), covering **6 documented bugs** across Functional, UI/Visual, Security, Usability, and Crash categories — discovered through manual exploratory testing on Desktop Web (Windows 10/11).

---

## 📋 Report Summary

| Field | Details |
|---|---|
| **Total Bugs** | 6 |
| **P1 — Urgent** | 2 |
| **P2 — High** | 4 |
| **Affected Product** | https://usbair.com/ |
| **Platform** | Desktop Web — Windows 10/11 |
| **Browsers** | Chrome / Edge (latest stable) |
| **Prepared** | March 2026 |

---

## 🐛 Bug Summary Table

| Bug ID | Title | Severity | Priority | Category |
|---|---|---|---|---|
| USBA-FT-001 | Country Selection Does Not Set Default Departure City in "From" Field | High | P2 | Functional / UI Visual |
| USBA-UI-002 | "Check-in" Modal Displays Oversized, Non-Responsive Content with Background Scrolling | Medium | P2 | UI Visual / Usability |
| USBA-NAV-003 | Returning from "Manage Booking" External Page Leaves Homepage Booking Widget Blank with Persistent Loader | High | P2 | Functional / Usability |
| USBA-AUTH-004 | Clicking Header Logo Unexpectedly Logs User Out; Back Button Restores Session — Inconsistent Auth State | High | **P1** | Security / Functional |
| USBA-BOOK-005 | Change Flight / View Booking Flow Returns Generic Error Then 500 Internal Server Error | High | **P1** | Functional / Crash |
| USBA-FRM-006 | Phone Input: Pasting Full International Number Duplicates/Clears Country Code and Triggers Invalid State | Medium | P2 | Functional / Usability |

---

## 🔍 Bug Details

### 🔴 USBA-AUTH-004 — Inconsistent Auth State on Logo Click *(P1 — Urgent)*
**Category:** Security / Functional

Clicking the US-Bangla header logo while logged in silently logs the user out. Clicking the browser Back button restores the session — creating an unpredictable auth state without any intentional login/logout action.

- **Expected:** Logo navigates to homepage while preserving authenticated session.
- **Actual:** User is logged out silently; back button restores session.
- **Impact:** Bookings could be incorrectly attributed; session data may leak across contexts.

---

### 🔴 USBA-BOOK-005 — Change Flight Flow Returns 500 Error *(P1 — Urgent)*
**Category:** Functional / Crash

From a logged-in booking details page, attempting to Change Flight first returns a generic notifier error, then clicking "View my booking" exposes a raw **500 Internal Server Error** page.

- **Expected:** Change Flight opens workflow or shows a clear eligibility message.
- **Actual:** Generic error → raw 500 page. User is fully blocked from self-service booking changes.

---

### 🟡 USBA-FT-001 — Country Selector Doesn't Auto-fill "From" Field *(P2)*
**Category:** Functional / UI Visual

Selecting Bangladesh (BD) correctly auto-fills "Dhaka (DAC)" in the departure field, but selecting Saudi Arabia (SA) or other countries leaves the field silently empty with no error or prompt.

---

### 🟡 USBA-UI-002 — Check-in Modal Layout Issues *(P2)*
**Category:** UI Visual / Usability

The Check-in modal renders oversized content with double scrollbars (both modal and page scroll simultaneously), the close button overlaps the site header, and background scrolling is not locked while the modal is open.

---

### 🟡 USBA-NAV-003 — Back Navigation Leaves Booking Widget Stuck *(P2)*
**Category:** Functional / Usability

After navigating to the external Manage Booking system and pressing Back, the homepage booking widget shows a persistent loading spinner indefinitely. Users must manually refresh to recover, blocking the booking conversion flow.

---

### 🟡 USBA-FRM-006 — Phone Field Breaks When Pasting International Number *(P2)*
**Category:** Functional / Usability

Pasting a full international number (e.g., `+8801877335477`) into the phone field duplicates the country code or triggers an immediate validation error. Editing the pasted value then clears the country-code selector — leaving the form in an unrecoverable invalid state.

---

## 🗂️ Bug Category Overview

| Category | Bug Count | Bug IDs |
|---|---|---|
| Functional | 5 | FT-001, NAV-003, AUTH-004, BOOK-005, FRM-006 |
| UI / Visual | 2 | FT-001, UI-002 |
| Usability | 3 | UI-002, NAV-003, FRM-006 |
| Security | 1 | AUTH-004 |
| Crash | 1 | BOOK-005 |

---

## 🛠️ Environment

| Parameter | Value |
|---|---|
| **OS** | Windows 10 / 11 |
| **Browsers** | Google Chrome (latest), Microsoft Edge (latest) |
| **Viewport** | ~1365×768 (desktop) |
| **Test Type** | Manual Exploratory Testing |
| **Target URL** | https://usbair.com/ |

---

## 📁 Repository Contents

```
USBanglaAirlines-BugReport/
│
├── Bug_Report_US-Bangla_Airlines.pdf   # Full detailed bug report (PDF)
└── README.md                           # This file
```

---



---

## 🔧 Tools Used

| Tool | Purpose |
|---|---|
| Browser DevTools | Network inspection, console error analysis |
| Chrome / Edge | Cross-browser testing |
| Manual Exploratory Testing | Bug discovery and reproduction |

---
## 🎥 Demonstration Video

**Watch the full bug demonstration walkthrough:**

[![Watch on YouTube](https://img.shields.io/badge/YouTube-Watch%20Demo-red?logo=youtube)](https://youtu.be/KWaU-1MS6uY)


---

<br>
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">


## <b>Connect with Me at</b>
<br>
<div align='center'>





<a href="https://www.facebook.com/ashak.odree/" target="blank">
<img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/facebook.svg" alt="ashakuzzaman odree" height="30" width="40" /></a>


<a href="https://www.instagram.com/ashak_odree/" target="blank">
<img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/instagram.svg" alt="ashak_odree" height="30" width="40" /></a>


<a href="https://www.linkedin.com/in/ashak-odree/" target="blank">
<img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/linked-in-alt.svg" alt="ashakuzzaman odree" height="30" width="40" /></a>


<a href="https://twitter.com/ashak_odree" target="blank">
<img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/twitter.svg" alt="@ashak_odree" height="30" width="40" /></a>
	
<a href="https://www.youtube.com/channel/UC8_-lmRrTG990jkiQ7pFsUw" target="blank">
<img align="center" src="https://raw.githubusercontent.com/rahuldkjain/github-profile-readme-generator/master/src/images/icons/Social/youtube.svg" alt="Ashak Odree" height="30" width="40" /></a>	

