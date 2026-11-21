# Merge Tactics — legal pages

Static English/German privacy policy and German Impressum for Merge Tactics.

## Current update

As of 21 November 2026, both languages describe the optional iOS 0.1.4 Apple sign-in and Firebase cloud save, account deletion, Firebase Authentication retention and local reminders. They distinguish the local age-group selection, separate online-configuration choice and non-personalized rewarded ads in 0.1.4 from the behavior in earlier versions.

English and German analytics retention disclosures use the owner's confirmed console settings: event data 2 months, user data 14 months, BigQuery exports 60 days (confirmed 18 November 2026). This documentation update does not change those settings.

### Confirmed owner details

- Diogo Soares da Cruz Silva, registered sole proprietor, trading as Seven Lamps Studios.
- Public email: sevenlampsstudios@gmail.com.
- Public phone: +49 176 59634413; publication explicitly approved by the owner.
- Approved service address: c/o flexdienst – #22691, Kurt-Schumacher-Straße 74, 67663 Kaiserslautern, Deutschland. Flexdienst FlexApp was purchased and approved as the service address; do not reopen address selection.
- Owner reports no Handelsregister entry, VAT ID or Wirtschafts-ID. Omit inapplicable fields; never publish an ordinary tax number. Do not infer VAT exemption from Nebengewerbe status.
- Intended audience remains 12+. BigQuery export is enabled.

### Game release checks

1. Test the mobile 0.1.4 privacy screen on a fresh install and on an upgrade from a previously opted-in device. Under 16 and undisclosed age selections should leave optional analytics, crash uploads, Remote Config and rewarded ads off. For 16 and older, test independent opt-ins and withdrawal. Check SDK initialization, ad requests and the UMP flow on signed builds.
2. In iOS 0.1.4, verify the Apple sign-in, restore, disconnect and delete-account paths using a test account and the production project configuration. Account deletion should remove the Firestore profile, revoke Apple authorization and delete the Firebase Auth user while retaining the phone’s local progress.
3. Verify disclosures against the production binary and console configuration, including actual ads behavior, Apple App Privacy and Google Play Data safety responses. There is no claim of independently audited legal compliance.

## Source audit

The iOS cloud-save and notification disclosures follow [game revision `23947042`](https://github.com/Vingator/merge-tactics/commit/23947042b5202cd54b0fe469d1e0a8a76c5a2aeb). The 0.1.4 mobile privacy choices and ad reporting follow [game revision `54bc2aee`](https://github.com/Vingator/merge-tactics/commit/54bc2aeea1a803156e0c00bad559a678c6e0c6c6).

The code includes StoreKit / Play Billing, separately consented Firebase Analytics and Crashlytics uploads, detailed gameplay replay analytics, Remote Config startup fetches, and Google AdMob / UMP. The old claim that these are only placeholders has been removed. iOS 0.1.4 adds optional Sign in with Apple, Firebase Authentication and a Firestore save linked to the account. Device backup and local notification scheduling are separate.

Habby's and Dream Games' public privacy policies were compared for structure: data/purpose, providers, retention and choices. Their unrelated social, careers and account disclosures were not copied. The Impressum omits speculative register/tax fields and generic legal boilerplate.

## Publishing

GitHub Pages: `main` / repository root. Keep stable links:

- https://vingator.github.io/merge-tactics-legal/
- https://vingator.github.io/merge-tactics-legal/impressum.html
- https://vingator.github.io/merge-tactics-legal/privacy.html

The landing page no longer carries the obsolete draft banner or noindex directive. Merging to main publishes the documentation; the separate game release checks above remain applicable.

## Reference sources

- [§ 5 DDG](https://www.gesetze-im-internet.de/ddg/__5.html)
- [GDPR](https://eur-lex.europa.eu/eli/reg/2016/679/oj)
- [§ 25 TDDDG](https://www.gesetze-im-internet.de/ttdsg/__25.html)
- [Firebase privacy](https://firebase.google.com/support/privacy)
- [Analytics retention settings](https://support.google.com/analytics/answer/7667196)
- [BigQuery sandbox](https://cloud.google.com/bigquery/docs/sandbox)
- [AdMob data disclosure](https://developers.google.com/admob/ios/privacy/data-disclosure)
- [GitHub privacy](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)
- Structure comparison: [Habby](https://www.habby.com/privacyPolicy.html), [Dream Games](https://www.dreamgames.com/en/privacy)
