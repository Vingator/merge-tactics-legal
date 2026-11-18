# Merge Tactics — legal pages

Static English/German privacy policy and German Impressum for Merge Tactics.

## Current update: draft pending retention confirmation

Do not deploy this branch yet. The privacy policy's retention paragraph explicitly remains unfinished.

### Confirmed owner details

- Diogo Soares da Cruz Silva, registered sole proprietor, trading as Seven Lamps Studios.
- Public email: sevenlampsstudios@gmail.com.
- Public phone: +49 176 59634413; publication explicitly approved by the owner.
- Approved service address: c/o flexdienst – #22691, Kurt-Schumacher-Straße 74, 67663 Kaiserslautern, Deutschland. Flexdienst FlexApp was purchased and approved as the service address; do not reopen address selection.
- Owner reports no Handelsregister entry, VAT ID or Wirtschafts-ID. Omit inapplicable fields; never publish an ordinary tax number. Do not infer VAT exemption from Nebengewerbe status.
- Intended audience remains 12+. BigQuery export is enabled.

### Remaining facts and release checks

1. Confirm Google Analytics event-data retention (2 or 14 months) and BigQuery dataset/table expiration, including existing exported tables. A free tier does not establish retention. BigQuery sandbox's automatic 60-day expiration must not be assumed for this project. Replace both language versions of the pending paragraph before deployment.
2. The current game has no age-selection or parental-authorization flow. A 12+ audience includes players below the age of independent consent in some jurisdictions. Review and implement appropriate consent and advertising handling before release; the policy does not claim that age verification or parental consent is implemented.
3. Remote Config fetches and uses Firebase installation identifiers before optional analytics consent. Review the operational legal basis and applicable device-storage/access consent requirements; a policy declaration alone does not establish a statutory necessity exemption.
4. Verify disclosures against the production binary and console configuration, including actual ads behavior, Apple App Privacy and Google Play Data safety responses. There is no claim of independently audited legal compliance.

## Source audit

Game source reviewed at `Vingator/merge-tactics` main commit `886c3df145c0ab3a4e811c5c5c768fccf393e78b`.

The code includes StoreKit / Play Billing, separately consented Firebase Analytics and Crashlytics uploads, detailed gameplay replay analytics, Remote Config startup fetches, and Google AdMob / UMP. The old claim that these are only placeholders has been removed. There is no game account or developer cloud save. Device backup is separate.

Habby's and Dream Games' public privacy policies were compared for structure: data/purpose, providers, retention and choices. Their unrelated social, careers and account disclosures were not copied. The Impressum omits speculative register/tax fields and generic legal boilerplate.

## Publishing

GitHub Pages: `main` / repository root. Keep stable links:

- https://vingator.github.io/merge-tactics-legal/
- https://vingator.github.io/merge-tactics-legal/impressum.html
- https://vingator.github.io/merge-tactics-legal/privacy.html

The landing page's existing draft banner remains until the publication blockers above are resolved. Remove it and its noindex directive when deploying finalized content.

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
