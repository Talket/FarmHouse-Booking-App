# FarmHouse Booking — Technical Overview

> Public product-engineering notes based on the existing product description and its published privacy policy and terms. This is not a deployment manual or a complete system specification.

**Google Play:** [https://play.google.com/store/apps/details?id=com.farmhouse.app&pcampaignid=web_share](https://play.google.com/store/apps/details?id=com.farmhouse.app&pcampaignid=web_share)  
**Android package:** `com.farmhouse.app`

## Product roles

The marketplace has two primary user journeys:

- **Owner:** creates an account and submits a property listing.
- **Visitor:** discovers listings, reviews property information and contacts the owner to arrange details.

A listing may contain a farmhouse name, description, address, city/state, coordinates, photographs, pricing, amenities, rules, contact information and availability. The public terms place responsibility for the accuracy of listing details on the owner.

## Known technology and integrations

- **Mobile:** Flutter / Dart.
- **Authentication:** Firebase Authentication, as described in the public privacy documentation.
- **Location:** optional device-location access for nearby discovery, maps and directions.
- **Advertising:** Google AdMob is identified in the privacy policy as a possible advertising provider.

This note intentionally does not assert a specific database schema, storage bucket design, backend topology or payment integration that is not documented here.

## Product flow

1. An owner or visitor opens the Android app.
2. Account-specific features use the app's authentication flow.
3. Owners submit property details and listing media.
4. Visitors discover listings and review the available property information.
5. Visitors verify important details and contact the owner to arrange a stay.

## Trust, privacy and safety

The public privacy policy describes account details, listing details, device diagnostics and optional location information. It also describes advertising-related data that may be handled by third-party providers. The product should request permissions in context and explain their purpose clearly.

The public terms describe the product as a discovery and communication platform. Unless the app expressly offers a different flow, booking discussions, payments, cancellations and agreements are arranged directly between the visitor and property owner. A listing is not proof that a property has been independently inspected or verified.

## Public repository scope

This repository contains only product-facing documentation, diagrams and screenshots intentionally selected for publication. It does not contain:

- Flutter source code or private application modules;
- Firebase service-account credentials or configuration secrets;
- API keys, signing keystores, passwords or Play Console credentials;
- production database exports, user records, booking conversations or analytics logs;
- private owner contact details or exact private-property coordinates.

## Existing public legal documents

- [Privacy policy](https://github.com/Talket/farmhouse_booking/blob/main/privacy-policy.html)
- [Terms and conditions](https://github.com/Talket/farmhouse_booking/blob/main/terms-and-conditions.html)

## Screenshot handling

Only add real screenshots from the released app. Blur or remove personal information, private owner details, account identifiers and precise location details that are not intended for public display. Do not publish private or unpublished property listings without permission.
