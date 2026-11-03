# Riverz CRM engineering

## Extending wacrm

The [wacrm](https://github.com/ArnasDon/wacrm) foundation supplies the core CRM. My extensions focus on commerce assistance, merchant knowledge, onboarding, integrations and recovery.

## Account-specific facts

Shared conversation behavior handles product selection, unanswered questions, order intent, escalation and contact restrictions. Catalogs, offers, coverage and payment conditions remain specific to each merchant.

## Conversation-level checks

The private project includes scenarios for images, quantity changes, compatibility, existing orders, complaints and human handoff. Testing a single fluent response cannot establish that the complete buying or support flow works.

## Uncertain external actions

A timeout may leave a send outcome unknown. Stable send identities and reconciliation help avoid duplicates. Connection updates also need to preserve newer state when requests overlap. A provider-specific connection needs its own verification.

[Overview](README.md) · [Related adaptations](VARIANTS.md)
