# Privacy Policy — Copl

**Version 1.0 — effective from 2026-05-19**

This policy explains what Copl does with the data you and your partner enter in the app. We've tried to write it in plain language — if anything is unclear, get in touch.

> *Note: this is an English translation of the Swedish original. The Swedish version is the authoritative one in case of any discrepancy. Synchronize both files when updating the policy.*

---

## Who is responsible

Pontus Brunzell, private individual, is the **data controller** for Copl.

Contact: copl-app@outlook.com

> *Note during development: when the app moves to a company structure, this section will be updated with company name, registration number, and contact details.*

---

## Summary for the impatient

- **You and your partner are the only ones who see your content.** Not us.
- **No ad SDKs, no analytics, no trackers.** None.
- **All data is stored in Sweden.** Region: Stockholm (Supabase).
- **You can at any time** view all data about you, export it, or delete your account.
- **Sensitive data** (intimacy, family notes) will be end-to-end encrypted — at which point not even we as operators can read the content.

---

## 1. What we collect

### 1.1 When you create an account

| Item | What it is | Why we need it |
|---|---|---|
| **Email address** | Your email | Login via magic link. We send only a link there. |
| **Nickname** | What your partner sees | So the app can say "Eva added a task" instead of an ID number |
| **Anonymous account ID** | Random UUID | Internal — links you to your data |

We **never** ask for:
- Real first or last name
- Phone number
- Address
- Date of birth or age
- Gender
- Profile photo (an optional avatar is possible but not required)

### 1.2 When you use the app

The content you and your partner enter:
- Tasks, to-do lists, shopping lists
- Calendar events
- Family information (children's names, shoe sizes, doctors, allergies)
- Meal planning
- Workout logs
- Weekly routines
- Homework
- Budget (income, expenses)
- Agreements between you
- Appreciations you send each other
- Daily and weekly mood check-ins
- Intimacy data (logs, preferences, goals) — only if you actively enable the module
- Reminders you send each other
- Short messages

We *don't ask* for any of this — you choose what to enter.

### 1.3 Technical data

- **Push token** for the device (so we can send notifications to that device)
- **Device type and app version** (iOS/Android, for debugging)
- **Timestamps** on your actions (when you logged in, when a row was created)

### 1.4 What we do **not** collect

- Location (GPS, IP-based geolocation)
- Contacts / address book from your phone
- Behavioral tracking or analytics
- Advertising identifiers (IDFA, GAID)
- Cookies (the app uses none)
- Bank transactions or card details
- Health data beyond what you yourself log in the intimacy module

---

## 2. Why we process data — legal basis

Per purpose:

| Purpose | Legal basis (GDPR) |
|---|---|
| Create account, log in | **Contract** (Art. 6.1.b) — you enter into an agreement with us to use the app |
| Store your entries and show them to your partner | **Contract** |
| Send push notifications about tasks and events | **Legitimate interest** (Art. 6.1.f) — the app would be meaningless without notifications; minimal impact on you |
| Store intimacy data | **Explicit consent** (Art. 9.2.a) — you actively enable the module and can disable it at any time |
| Error reporting (when Sentry is active) | **Legitimate interest** — technical crash reports without personal data |

Intimacy data is a **special category of personal data** under GDPR Art. 9. We handle it with extra care: opt-in, optional PIN lock, planned end-to-end encryption.

---

## 3. Where data is stored

| Where | What | Geography |
|---|---|---|
| **Supabase** | All database content, authentication, files | **Sweden (Stockholm)** — EU region, data never leaves the EU |
| **Apple Push Notification Service (APNS)** | Push token + notification content in transit | Apple's global infrastructure |
| **Google Firebase Cloud Messaging (FCM)** | Push token + notification content in transit | Google's global infrastructure |
| **Expo** | App builds, OTA updates (no user data) | USA |
| **Sentry** (when active) | Crash reports | EU region (configured) |

No other third parties have access to data.

---

## 4. How long data is kept

- **Active accounts:** No automatic deletion. Data lives as long as you use the app.
- **Ended relationships** (where both partners have ended or you deleted your account): Soft delete first. **Hard deletion within 30 days.**
- **Closed accounts:** All your data is deleted within 30 days.
- **Backups:** We take manual backups with limited retention. Backups older than 3 months are deleted.
- **Server logs:** Maximum 7 days.

---

## 5. Who sees data

### You and your partner
You see each other's content within your relationship. That is the entire point of the app.

### Us (operators)
- Technically, we can reach the database via Supabase administration tools.
- In practice, we don't look at user data — there are no routine tasks that require it.
- When debugging a specific issue, we may need to read individual rows, always with the purpose of fixing the problem and nothing else.
- When **end-to-end encryption is in place**, we will *not even be able* to read intimacy data, family notes, or agreements — it is encrypted on your device before being stored.

### Third parties
- **Supabase** stores the data but has no routines that open it. They have their own privacy policy.
- **Apple and Google** see push notification content on the way to your phone. We send generic notification texts ("Something new from your partner") where possible.
- **No others.**

### What we *don't* do
- We **never sell** data.
- We **never share** data with ad networks or data brokers.
- We **don't combine** your data with external data sources.

---

## 6. Security

- **Row Level Security (RLS)** on all database tables — it is technically impossible for a user to read data from a relationship they are not a member of.
- **HTTPS** encrypts all traffic between your phone and our servers.
- **End-to-end encryption** will be implemented for sensitive fields (intimacy, family notes, agreements, appreciations) before public launch. After that, not even we as operators will be able to read the content.
- **PIN lock** on the intimacy module can be activated locally on your device.
- **Discreet mode** hides sensitive sections from the app's home screen.
- **Passwords don't exist** — we use magic links via email, which eliminates password leak risks.

---

## 7. Your rights under GDPR

You have the following rights and can exercise them at any time:

| Right | How to do it |
|---|---|
| **Know** what data we have about you | Settings → "Your data" — shows everything stored about you personally |
| **Correct** inaccurate data | You can change all your own content directly in the app |
| **Erasure** of your data ("the right to be forgotten") | Settings → Delete account — all data disappears within 30 days |
| **Receive** your data (portability) | Settings → Export our data (coming in next version) — JSON file with all rows |
| **Restrict** processing | Pause the relationship (Settings → Pause) — data becomes read-only |
| **Object** to processing | Contact us (see below) |
| **Withdraw consent** for the intimacy module | Settings → turn off Closeness/Intimacy — the data is deleted |

We respond to all requests **within 30 days**, usually much sooner.

---

## 8. Complaints

If you believe we are handling your personal data incorrectly, you can:

1. **Contact us first** — we want to know and would like to fix it.
2. **File a complaint with the Swedish Authority for Privacy Protection (IMY):**
   - Web: https://www.imy.se
   - Phone: +46 8 657 61 00
   - Mail: IMY, Box 8114, 104 20 Stockholm, Sweden

---

## 9. Automated decisions and profiling

We use **no** automated decision-making or profiling. No algorithms draw conclusions about you that affect you.

---

## 10. Children

Copl is not intended for children under 16. Parents may store information *about* their children (names, shoe sizes, allergies) as part of the family module — but the children themselves should not create accounts.

Parents are responsible for informing their children about what data is stored about them.

---

## 11. Changes to this policy

This policy may be updated as the app evolves or as legislation changes. Major changes are announced in the app and, when needed, via email.

**Version history:**

| Version | Date | Change |
|---|---|---|
| 1.0 | 2026-05-19 | First published version. |

---

## 12. Contact

For privacy questions, GDPR requests, or curiosity:

**Email:** copl-app@outlook.com

**Postal address:** provided on request

---

*The Swedish version of this policy is authoritative. In case of discrepancy between translations, the Swedish version applies. See [PRIVACY.md](PRIVACY.md) for the Swedish original.*

*Internal source document with technical details (for developers): [`docs/INTEGRITET.md`](docs/INTEGRITET.md) in the codebase.*
