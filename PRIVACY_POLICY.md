# Privacy Policy for Story Plan

**Last updated:** November 7, 2026

---

## Summary

Story Plan is built to keep your personal content on your device.

- **Your journal entries, habits, goals, tasks, media, and location data are stored on your device.** We do not operate a server that stores your content, we have no user account system, and we have no access to your content.
- **If you have Pro and enable Cloud Backup, your data is encrypted before upload** and saved to your own Google Drive. Cloud Backup requires a master passphrase; the app never uploads the raw vault key, and only a passphrase-wrapped copy is stored in your Drive. We cannot read your backups.
- **We do not use your content for advertising, profiling, or marketing, and we do not sell your data.**
- **A small amount of technical information does leave your device** when you use the app — for turning coordinates into an address, for purchase verification, for anonymous usage analytics, and for crash diagnostics. Each of these is explained in full below, and you can turn analytics and crash reporting off in Settings.

We would rather be precise about what leaves your device than tell you nothing does.

---

## Information Collection and Use

### Your content (stored on your device)

Your journal entries, habits, goals, tasks, check-ins, and all associated metadata are stored in the app's private storage on your device. This includes any location information and any media you attach.

We do not have access to this content. It is not transmitted to us, and it is not included in crash reports or analytics.

### Location and address lookup

**What the app does:** When you choose to add a location to a story or task, the app records your coordinates and converts them into a readable address (for example, "Park Road, Pune, Maharashtra").

**What leaves your device:** To perform that conversion, the app uses your device's built-in geocoding service. On most Android devices this is provided by Google, which receives the coordinates in order to return an address. The app does not contact any third-party geocoding provider directly, and no location data is sent to the developer.

**Storage:** The coordinates and the resulting address are stored locally with your entry. If Cloud Backup is enabled, they are included in your encrypted backups.

### Device activity and the apps you use

**Feature:** If you enable Unified Metrics, the app reads screen time and app-usage data on your device to generate charts and insights about how you spend your time. The App Visibility list shows the apps it can describe: those with a launcher icon, plus any app you have used in the last 30 days.

**Permissions used:** `PACKAGE_USAGE_STATS` (app usage). This single permission covers both the numbers and the app list: the app names and icons shown in App Visibility come from your usage data and from Android's list of apps that have a launcher icon. The app never requests permission to see your full list of installed applications.

**Storage:** This data is generated and stored locally. It is not transmitted to the developer, and it is not included in analytics or crash reports.

**If you turn Unified Metrics off,** the app stops reading usage data. You can also revoke the permission at any time in Android Settings.

### Media files

Photos, audio recordings, and videos you attach to entries are stored in the app's private storage on your device. If Cloud Backup is enabled, they are uploaded to your Drive as part of your encrypted backup.

The app requests `RECORD_AUDIO` to record voice entries you choose to create. `READ_MEDIA_AUDIO` (and `READ_EXTERNAL_STORAGE` on older Android versions) is used only when you choose a custom audio file as an alarm sound; it is not used to scan your media library.

### Cloud Backup and Google Drive

**A Story Plan Pro feature.** You can choose to back up your database and media to your own Google Drive.

- **Authentication:** The app uses Google Sign-In and requests only the `drive.file` scope, meaning it can access only files it created. It cannot read the rest of your Drive.
- **Encryption:** Your data is encrypted on your device before upload. Google stores ciphertext it cannot decrypt.
- **Master passphrase:** Cloud Backup cannot be enabled without a master passphrase. The app wraps your vault key with a key derived from that passphrase using PBKDF2 and uploads only the wrapped key. The raw vault key is never uploaded. If an older install has a raw key in Drive, the app migrates it by wrapping the same key; it does not generate a new key or overwrite existing backups.
- **Disabling the passphrase:** The app refuses while encrypted cloud backups or media remain in Drive. Once they are gone, disabling removes the wrapped key and turns Cloud Backup off; it does not delete your local data.
- **What is uploaded:** Your entries, habits, goals, tasks, location history, and any media you have attached.
- **Retention:** Cloud backups stay in your Drive until you delete them from the app or from Google Drive. Signing out does not delete them.

**Creating backups and restoring them is free on every plan.** Uploading to Google Drive is the part that needs Pro. On the free plan you can still create backups on your device, export them, and restore any backup you have — including a cloud backup you made while you had Pro.

**If your Pro plan ends, nothing is hidden and nothing is deleted.** New uploads to Google Drive stop, because Drive backup is a Pro feature. The backups you already made stay in your Drive, stay listed in the app, and stay restorable. The only thing you lose is the ability to upload new ones.

> **Keep your own copy.** Uninstalling the app removes its data from your device. If you have never made a backup, or if you uninstall without one, that data cannot be recovered. To protect yourself, enable Cloud Backup before uninstalling, or use the app's export function to save a backup file somewhere outside the app.

### Purchases and subscriptions

**Payments are processed entirely by Google Play.** The app does not receive or store your card details.

- Purchases and subscriptions are made through Google Play Billing. Google acts as the payment processor and issues the receipt.
- **Purchase verification:** To confirm whether a purchase is active, the app sends the Play purchase token and product ID over HTTPS to a small Google Cloud Function operated by the developer (`verifyPurchase`, region `us-central1`). The function requires a Firebase App Check token from a genuine app install, asks the Google Play Developer API about that token, and returns the state. It is stateless: it has no database, stores no purchase record, and does not receive your content. Its logs contain only a 12-character SHA-256 prefix of the token and the resulting state, not the raw token.
- The purchase record is held in your Google Play account. The app stores the purchase token on your device to confirm status and to retry verification. It is pseudonymous account data, not your content.
- Renewals, cancellations, and refunds are managed through Google Play. You can cancel a subscription in your Play Store account at any time; access continues until the end of the paid period.
- Only the monthly plan may offer a 7-day free trial. Play decides whether a given account is eligible; the app does not guarantee a trial to any user and does not run its own trial timer.
- If you unsubscribe, you keep everything you created while subscribed. Nothing is deleted, and existing items remain fully usable. Subscription status affects whether you can create new items beyond the free-plan limits.

### Usage analytics

**Optional, and you can turn it off in Settings.**

The app uses Firebase Analytics (Google) to measure whether the app is working. It records anonymous events such as:

- the paywall being viewed
- a purchase being started, completed, or failed
- the restore-purchases button being tapped
- which features are used and how often

This tells us which features are useful and where people get stuck, so we can decide what to build next. It cannot tell us who you are.

**What this involves:** app interactions, the app's version, your device model, your language, a randomly generated identifier for this app installation, and an approximate location derived from your IP address. It does **not** include your journal entries, habits, goals, tasks, media, location check-ins, device-usage data, or anything you type.

**Turning it off:** Disabling analytics stops all of these events from being sent. The app works the same way either way.

### Crash diagnostics

**You can turn this off in Settings.**

If the app crashes, it can automatically send a report to Firebase Crashlytics (Google) so we can find and fix the problem. Without this, we would only learn about a crash if a user chose to tell us.

**What a crash report contains:** the error type, the stack trace, your device model, your Android version, the app version, and a randomly generated identifier for this installation. It may also include technical breadcrumbs about what the app was doing.

**What a crash report never contains:** your journal entries, habits, goals, tasks, media, location check-ins, or device-usage data. The app does not read your database when sending a report, and we take care not to include personal content in error messages.

### Fonts

The app's fonts are included in the app itself. The app does not download fonts from the internet at runtime, and it does not contact Google's font servers.

### Feedback and log sharing

You can manually share a diagnostic log with us for support. When you do this, the app prepares the log and hands it to your email app or sharing sheet — nothing is sent automatically, and nothing is sent unless you choose to send it.

### No advertising

We do not use your data for advertising, profiling, or marketing. We do not build advertising profiles and we do not sell your data to anyone.

---

## Data Security

- **Cloud backups are encrypted** using AES-256 before being uploaded to your Drive. The raw encryption key is generated on your device and is never uploaded. A copy wrapped with a master-passphrase-derived key is stored in your Drive so another device can restore with the passphrase. We cannot decrypt your backups, and neither can Google.
- **Cloud Backup requires a master passphrase.** The app refuses to create or upload a cloud backup key without one. Restoring a wrapped cloud backup on a new device requires that same passphrase. If you forget it, no one — including us — can recover the cloud backups. Older installs that stored a raw key in Drive are migrated by wrapping the same key after the user sets a passphrase; existing backups are preserved, and cloud uploads stay paused until migration succeeds.
- **Local data is stored in the app's private storage**, which is protected by your device's operating system and its standard file encryption. To be clear about the distinction: the local database is *not* separately encrypted by the app. On a rooted or otherwise compromised device, someone with access to the app's files could read it. Encryption beyond what the operating system provides applies to your backups, not to the local database.
- **Manual exports are different from backups.** "Export Data" creates a plain, unencrypted JSON file containing your entries and related metadata, including attachment file paths and captions, but not the attachment bytes. Treat that file as sensitive and store or share it only where you intend. It is not protected by your master passphrase.
- **A safety copy of your database is written locally, unencrypted, immediately before a restore.** It never leaves your device and is not uploaded, but it does sit in the app's private storage, so it is covered by the same caveat as the local database above.
- **The app can be locked with biometrics** (`USE_BIOMETRIC`), so locked entries stay behind your fingerprint or face unlock.

---

## Data Retention

- **Local data:** stays on your device until you delete it or uninstall the app. Uninstalling removes it.
- **Backups in your Drive:** stay until you delete them from the app or from Drive. Disconnecting the app stops new uploads but does not delete existing files.
- **Analytics data:** retained by Google for a limited period in line with Firebase's own retention policy.
- **Crash reports:** retained by Google for up to 90 days.

### Deleting your data

You can delete your data at any time:

- **Individual items** — delete entries, habits, goals, and tasks from within the app.
- **Media** — delete attachments from an entry, or from My Data.
- **Backups** — delete backups individually from My Data.
- **All local data** — Story Plan currently has no in-app "delete everything" button. Use Android Settings → Apps → Story Plan → Storage & cache → Clear storage, or uninstall the app; both remove the app's local database and files. Clearing app data also removes the local vault key, so cloud backups will need the master passphrase to restore afterward.
- **Cloud data** — delete the backup folder from your Google Drive, or revoke the app's Drive access in your Google account settings. Your files then become yours alone, in your own Drive.

Note that deleting a backup does not delete the data already restored from it. Delete the local copy separately by deleting it in the app or uninstalling.

---

## Your Rights and Control

- **Access and export** — export your data at any time from My Data.
- **Delete** — remove your data as described above.
- **Correct** — edit any entry, habit, goal, or task directly in the app.
- **Withdraw consent** — turn off analytics and crash reporting in Settings, and revoke any permission in Android Settings.
- **Disconnect Google** — sign out of Cloud Backup to remove the app's access to your Drive.

Because we do not operate a content server and there is no user account, exercising these rights is something you do directly in the app or in your own Google account. The purchase-verification function is stateless and does not hold a copy of your content. We cannot retrieve content for you, because we never held it.

---

## Permissions Explained

| Permission | Why it's used |
|---|---|
| `INTERNET` | Connecting to Google Drive for backup, to Google Play and the purchase-verification Cloud Function for billing, and to Firebase for analytics and crash reporting. |
| `ACCESS_NETWORK_STATE` | Checking whether you are online before syncing. |
| `POST_NOTIFICATIONS` | Reminders, alarms, and habit and task notifications. |
| `SCHEDULE_EXACT_ALARM` | Scheduling your alarms at the exact time you set, so they fire when you expect. The app continues to work if this is not granted. |
| `RECEIVE_BOOT_COMPLETED` | Re-registering your alarms after the device restarts. |
| `VIBRATE` | Vibration for alarms and reminders. |
| `WAKE_LOCK` | Keeping the CPU awake while an alarm is ringing. |
| `FOREGROUND_SERVICE` | Running the alarm service reliably even when the app is closed. |
| `FOREGROUND_SERVICE_SPECIAL_USE` | Keeping the alarm ringing reliably with wake lock until dismissed or snoozed, as required on modern Android versions. |
| `REQUEST_IGNORE_BATTERY_OPTIMIZATIONS` | Requesting exemption so your alarms are not delayed or dropped by aggressive battery saving. |
| `USE_BIOMETRIC` | Unlocking the app with your fingerprint or face. |
| `USE_FULL_SCREEN_INTENT` | Showing an alarm as a full-screen activity so a habit or task alarm is seen immediately. |
| `SYSTEM_ALERT_WINDOW` | Declared for compatibility with alarm presentation on some Android versions. The app currently checks/requests it but does not draw system overlays and does not use it to access your data. |
| `RECORD_AUDIO` | Recording voice entries you choose to create. |
| `READ_MEDIA_AUDIO` | Selecting a custom audio file as an alarm sound. Not used to scan your media library or for backup. |
| `READ_EXTERNAL_STORAGE` | The pre-Android-13 equivalent for selecting a custom alarm sound. Not used to scan your media library or for backup. |
| `ACCESS_FINE_LOCATION` / `ACCESS_COARSE_LOCATION` | Getting your coordinates when you choose to add a location to a story or task. |
| `PACKAGE_USAGE_STATS` | Reading screen time for Unified Metrics, and identifying the apps in that usage data. |

Every one of these can be revoked in Android Settings. The app continues to work; the related feature will not.

---

## Children's Privacy

The app is not directed at children under 13, and we do not knowingly collect personal information from children under 13. Because all content is stored on your device and we do not operate a server that stores content, we do not hold any content about any user, child or otherwise. The stateless purchase-verification function does not retain purchase or content records.

If you believe a child under 13 has provided personal information, contact us and we will help you remove it from their device.

---

## Changes to This Privacy Policy

We may update this policy as the app changes. The **Last updated** date at the top always reflects the current version, and changes take effect when published. If a change materially affects how your data is handled, we will say so in the app before it takes effect.

---

## Contact Us

- **Email:** storyplandev@gmail.com

For any privacy question, request to delete data, or to report a concern, email us. If you are in the EEA or UK and wish to complain to a supervisory authority, you are free to do so.

---

## Data Controller

The data controller for Story Plan is the app developer.

Most data is stored on your device or in your own cloud storage, so the developer does not have access to your personal content unless you explicitly provide it for support. The stateless purchase-verification function transiently processes the purchase token. The limited data described under *Usage analytics* and *Crash diagnostics* is processed by Google, acting as our processor under those services' own terms and privacy policies.
