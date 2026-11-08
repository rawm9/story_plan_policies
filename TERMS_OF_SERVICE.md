# Terms of Service for Story Plan

**Last updated:** November 7, 2026

---

## 1. Agreement to These Terms

These Terms of Service ("Terms") form a legal agreement between you and the
developer of the Story Plan app ("the App", "we", "us"). They govern your use of
the App on Android devices.

By installing or using the App, you accept these Terms. If you do not agree with
them, please do not use the App.

The App is also governed by our [Privacy Policy](privacy-policy), which explains
what data is stored where, and who can see it. The Privacy Policy forms part of
these Terms.

---

## 2. What the App Is

Story Plan is a personal journalling and habit-tracking app. It stores your
entries, habits, goals, tasks, and related content **on your device**, and
enables optional features that sync encrypted backups to your own Google Drive.
Drive backup is a Pro feature; creating, exporting and restoring backups is not.

We do not operate a server that stores your content, we do not host a copy of
your content, and we have no account system. A small, stateless Google Cloud
Function is used only to verify Google Play purchases (see Section 6.1); it does
not receive or store your entries. We cannot read your entries, and we cannot
recover them for you.

---

## 3. Licence

Subject to your compliance with these Terms, we grant you a limited,
non-exclusive, non-transferable, revocable licence to install and use the App
on devices you own or control, for your personal or internal use.

The App is licensed to you, not sold to you. The App is protected by copyright
and other intellectual property laws. All title, copyright, and other
intellectual property rights in the App belong to us or our licensors.

You may not:

- copy, modify, or create derivative works of the App;
- reverse-engineer, decompile, or disassemble the App, except to the extent that
  this restriction is prohibited by applicable law;
- redistribute, sublicense, rent, lease, or sell the App;
- remove or alter any copyright, trademark, or attribution notice.

---

## 4. Your Content

### 4.1 You keep ownership

You retain all rights to the content you create in the App — your journal
entries, habits, goals, tasks, images, audio recordings, and anything else you
add ("Your Content"). We claim no ownership of Your Content.

Nothing in these Terms transfers ownership of Your Content to us.

### 4.2 The limited licence you give us

To operate the App, you grant us a worldwide, royalty-free, non-exclusive
licence to host, copy, transmit, display, and process Your Content **solely to
the extent necessary to operate the App for you** — that is, to display it back
to you, to create your backups, and to generate the on-device insights and
summaries you have enabled.

This licence ends when you delete Your Content or uninstall the App, except to
the extent that a backup you have chosen to store in your own Google Drive
remains under your control until you delete it.

### 4.3 You are responsible for Your Content

You are solely responsible for the content you create and for making sure you
have the right to store and use it. The App is not a substitute for your own
judgment about what is appropriate to record.

---

## 5. Backups and Data Recovery

This section matters, so please read it.

**If you have Pro and Cloud Backup is enabled**, the App encrypts your data on
your device before uploading it, and stores it in **your own** Google Drive
account. The App does not upload the raw encryption key; a copy wrapped with a
key derived from your master passphrase is stored in your Drive. Cloud Backup
requires that passphrase. Disabling it is refused while encrypted cloud backups
or media exist; if it succeeds, Cloud Backup is turned off until you set a new
passphrase.

This means:

- **Nobody else can read your backups** — not us, not Google, not anyone with
  access to the file.
- **This also means nobody can recover them for you.** If you lose the device,
  forget the master passphrase, or lose the exported file, the data cannot be
  recovered by you or by us. There is no reset link and no back door, by design.

**Uninstalling the App removes its data from your device.** If you have not made
a backup, or you uninstall without one, that data is gone. Before uninstalling,
or if your device is lost, damaged, or being replaced, make a backup.

**Creating backups and restoring them is free on every plan.** A subscription
is never required to create a backup, export one, or restore one — including a
backup you uploaded to Google Drive while you had Pro. Subscribing changes how
many backups the App retains on your device, and enables uploading new ones to
Google Drive, which is the one part of backup that is a Pro feature.

You can also use **Export Data** to create a plain, unencrypted JSON file and
keep your own copy anywhere you like. Unlike an encrypted backup, that export is
not protected by your master passphrase, so treat it as sensitive. You can import
it on a fresh installation after uninstalling.

**If your subscription ends, nothing is deleted and nothing is hidden.** New
uploads to Google Drive stop. Every backup you already made — local or in Drive —
stays in your Drive, stays listed in the App, and stays restorable. The App does
not turn off a setting you chose and does not remove backups you can see.

---

## 6. Subscriptions, Trials, and Payments

### 6.1 Payments are handled by Google

All purchases are processed through **Google Play Billing**. Google acts as the
payment processor. We never receive or store your card or bank details.

The purchase record is kept in your Google Play account. To confirm whether a
purchase is active, the App sends the Play purchase token and product ID over
HTTPS to a small Google Cloud Function operated by us (`verifyPurchase`, region
`us-central1`). The function requires a Firebase App Check token from a genuine
app install, asks the Google Play Developer API about that token, and returns the
state. It is stateless: it has no database, stores no purchase record, and does
not receive your content. Its logs contain only a short SHA-256 prefix of the
token and the resulting state. The App stores the token on your device to confirm
status and retry verification.

### 6.2 Free trials

Only the **monthly** plan may offer a 7-day free trial. Any trial is offered,
granted, and administered by **Google Play**; eligibility is decided by Play and
is not guaranteed to every account. The App does not run its own trial timer, and
trial availability and length may change at our discretion. You can end a trial
early through Google Play.

### 6.3 Renewal and cancellation

Subscriptions renew automatically at the end of each billing period until you
cancel. You can cancel at any time through your Google Play Store account, and
**we cannot cancel a subscription for you**.

If you cancel, your access to paid features continues until the end of the period
you have already paid for. There is no partial refund from us; refunds are
handled by Google under the Google Play refund policy.

### 6.4 Prices and changes

Prices are set in your local currency and may include taxes. If we change a
price, existing subscribers keep their current price until their next renewal,
and we will give notice in the App before any change takes effect.

### 6.5 What a subscription does and does not do

A Story Plan Pro subscription **raises limits and unlocks optional features**. It
does not grant access to anything you have not already created.

**If your subscription ends, nothing you created is deleted.** Your entries,
habits, goals, tasks, media, and backups remain on your device and remain fully
usable. The free plan continues to let you:

- create unlimited tasks, journal entries, events, and life-code items (with up to 1 media attachment per task or journal entry);
- track up to 3 active habits;
- create up to 3 goals for Month and Quarter horizons, and 1 goal for Year, Decade, and Life horizons;
- use alarms, habit freezes, and daily and weekly recaps;
- create, export, and restore backups on your device;
- restore any backup, including one uploaded to Google Drive while you had Pro;
- keep up to 3 retained backups on your device.

Pro raises the number of retained backups, provides unlimited habits, unlocks unlimited goals across all horizons (Month, Quarter, Year, Decade, Life), unlocks longer recap frequencies (Monthly, Quarterly, Yearly) and multi-horizon synthesis, allows unlimited media attachments per task and journal entry, extends analytics beyond the free 7-day window, adds Correlation Insights over your full history, adds Google Drive cloud backup, and adds home-screen widgets.

The precise limits are listed in the App on the plans screen, and the App is
the authoritative source — this summary is for convenience, not for substitution.

### 6.6 Refunds

Unless required by law, all purchases are final. Please read the Google Play
refund policy before purchasing.

---

## 7. Acceptable Use

You agree not to use the App to:

- store or distribute content that is unlawful, defamatory, or that infringes
  anyone else's rights;
- store content that you do not have the right to store;
- reverse engineer, tamper with, or interfere with the App's operation or
  security;
- use the App in a way that breaks applicable law.

---

## 8. Third-Party Services

The App can interact with third-party services, including Google Play, Google
Sign-In, Google Drive, Google Firebase, Google Cloud Functions, and Firebase App
Check. Those services are governed by their own terms and privacy policies, which
we do not control.

Your use of them is subject to:

- **Google Play** — purchases, subscriptions, and billing;
- **Google Sign-In and Google Drive** — optional Cloud Backup (a Pro feature),
  which accesses only files the App creates;
- **Firebase and Google Cloud (Google)** — optional usage analytics and crash
  diagnostics, App Check attestation, and the stateless purchase-verification
  Cloud Function, as described in the Privacy Policy.

If you do not connect a Google service, the App does not use it.

---

## 9. Availability and Changes

We may modify, suspend, or discontinue any part of the App, including features
that operate offline. We do not promise that the App will always be available,
uninterrupted, or free of errors.

Because your content is stored on your device, uninstalling the App or a
platform change may make some content inaccessible. Keep your own backups.

---

## 10. Disclaimer of Warranties

**To the fullest extent permitted by law, the App is provided "as is" and
"as available", without warranties of any kind, whether express or implied,
including implied warranties of merchantability, fitness for a particular
purpose, title, and non-infringement.**

We do not warrant that the App will be error-free, uninterrupted, or that your
content will be preserved. The App is a personal productivity tool, and you are
responsible for keeping your own backups.

---

## 11. Limitation of Liability

**To the fullest extent permitted by law, in no event shall we be liable for any
indirect, incidental, special, consequential, exemplary, or punitive damages, or
for any loss of data, loss of profits, loss of goodwill, or business
interruption, arising out of or in connection with your use of the App or these
Terms — even if we have been advised of the possibility of such damages.**

**Our total aggregate liability arising out of or relating to the App or these
Terms shall not exceed the greater of (a) the amount you paid us for the App in
the twelve months before the event giving rise to the claim, or (b) USD 20.**

Nothing in this section excludes or limits liability that cannot lawfully be
excluded or limited, including liability for death or personal injury caused by
negligence, or for fraud or fraudulent misrepresentation. Some jurisdictions do
not allow certain limitations, so parts of this section may not apply to you.

**Particular note on data loss:** because the App stores your content on your
device and we hold no copy of it, we cannot and do not accept responsibility for
lost data. Keep your own backups — Section 5 explains how.

---

## 12. Indemnity

You agree to indemnify, defend, and hold us harmless from any claim, demand,
loss, or expense (including reasonable legal fees) arising out of Your Content,
your use of the App in violation of these Terms, or your violation of any law or
the rights of a third party.

---

## 13. Termination

You may stop using the App at any time, and uninstalling it ends your licence.

We may suspend or terminate your access if you materially breach these Terms,
for example by using the App unlawfully. Where we terminate access, we will
explain why and give you a reasonable opportunity to fix the problem where that
is possible.

Because your content is stored on your device, terminating access does not
delete it. Uninstalling the App does. If you believe we have terminated your
access in error, contact us.

---

## 14. Changes to These Terms

We may update these Terms as the App changes. The **Last updated** date at the
top always reflects the current version, and changes take effect when published.

If a change materially affects your rights, we will bring it to your attention
in the App before it takes effect. Continuing to use the App after a change
takes effect means you accept the updated Terms. If you do not agree, please
stop using the App.

---

## 15. Governing Law and Disputes

These Terms are governed by the laws applicable at the place of the developer,
without regard to conflict-of-law rules.

Any dispute arising out of or relating to these Terms or the App will be
resolved first through good-faith discussion between you and us. If we cannot
reach an agreement, you and we may pursue any remedy available to us under
applicable law, before any court of competent jurisdiction.

If you are a consumer in the EEA or the UK, you retain the benefit of any
mandatory consumer protections under the law of your country of residence, and
you may bring proceedings in the courts there.

You may contact us first at the email address in Section 17.

---

## 16. Age

The App is not directed to children under 13. By using it, you confirm you are
at least 13 years old, or the age of digital consent where you live. If you are
under 18, please use the App with a parent or guardian's involvement.

---

## 17. Contact Us

- **Email:** storyplandev@gmail.com

If you have a question about these Terms, want to report a problem, or need help
with your data, email us. We aim to reply within a reasonable time.

---

## 18. Data Controller

The data controller for Story Plan is the app developer.

Because content is stored on your device and we do not operate a server that
stores content, we hold no copy of your content. The stateless purchase
verification function transiently processes a Play purchase token. Limited data
described under *Usage analytics* and *Crash diagnostics* in the Privacy Policy
is processed by Google, acting as our processor under those services' own terms
and privacy policies.

---

*These Terms are a plain-language starting point written by the developer, not
legal advice, and have not been reviewed by a lawyer. If you need terms
appropriate to your circumstances — particularly if the App becomes significant
to your business, is monetised at scale, or is distributed in a jurisdiction
where consumer law is strict — have a qualified lawyer review and adapt them.*
