# Terminology and glossary template

Use this template to keep product terms consistent across writers, engineers, support, and translators. One glossary serves two purposes:

- **Internal terminology list:** all columns. Writers and reviewers use it to check usage.
- **Public glossary:** only the *Term* and *Definition* columns, published in the docs.

The same table is available as `glossary-template.csv` for spreadsheets.

## Columns

| Column | What to enter |
|---|---|
| Term | The approved term, in the case used in running text. |
| Definition | One sentence, written for the reader. Start with the category: "A [noun] that …". Do not use the term itself in its definition. |
| Preferred usage | Approved forms and example phrasing: plural, verb form, abbreviation, and capitalization rules. |
| Do not use | Synonyms, old names, internal names, and incorrect forms. |
| Notes | Context: when the term was introduced, related terms, translation notes, or the owner who decides. |

## Glossary

| Term | Definition | Preferred usage | Do not use | Notes |
|---|---|---|---|---|
| [Term] | [Definition.] | [Usage.] | [Avoided forms.] | [Notes.] |
| API key | A secret string that identifies your account when you send requests to the Parcelwise API. | "API key", "test key", "live key". Lowercase *key*. | API token, secret key, access key | OAuth access tokens are a different credential. See *access token*. |
| access token | A short-lived credential that a partner app gets from the OAuth token endpoint and sends with API requests. | "access token". Say "expires after 1 hour". | API key, bearer key, session token | Used only for partner apps. |
| carrier | A company that transports and delivers packages, for example a postal service or courier. | "carrier", "carrier service" for a specific delivery option. | courier (except in quotes), shipping provider, vendor | Translation note: not the same as "network carrier" in telecom. |
| label | The printable document with the barcode and addresses that is attached to a package. | "shipping label" on first use, then "label". "Buy a label", not "purchase a label". | waybill, sticker, postage | *Waybill* is acceptable only in content for freight customers. |
| shipment | A package that Parcelwise tracks from label creation to delivery. | "create a shipment", "cancel a shipment". | parcel (for the tracked object), order, consignment | *Parcel* refers to the physical package and its dimensions, as in the `parcel` API object. |
| Sync Agent | The Parcelwise service that runs on your server and sends orders from your database to Parcelwise. | "Parcelwise Sync Agent" on first use, then "the agent". Capitalize *Sync Agent*. | connector, sync daemon, PW agent, the bridge | *The bridge* was the internal code name. Never use it publicly. |
| warehouse | A location from which you ship packages, with its own address and agent. | "warehouse", even for small stockrooms. | location, site, depot, fulfillment center | Each warehouse has one sender address by default. |
| webhook | An HTTP request that Parcelwise sends to your server when an event happens, such as a status change. | "webhook", "webhook endpoint" for your URL. Lowercase, one word. | callback, web hook, Webhook, push notification | |

> **Tips:**
> - Sort rows alphabetically once the glossary has more than about 20 terms.
> - Add a term when a reviewer asks "what does this mean?" or when two documents use different words for the same thing.
> - Give the glossary an owner, and review it at each major release.
> - Many style linters (for example Vale) can read a list of "do not use" terms and flag them automatically.
