# One CRM foundation, several business workflows

Riverz CRM builds on [wacrm by Arnas Donauskas](https://github.com/ArnasDon/wacrm). My work extends that foundation with merchant-specific assistance, catalog knowledge, integration recovery, onboarding and human handoff. The following are domain adaptations of that CRM family, not independent CRM systems built from scratch.

| Workstream | Product context | Portfolio focus |
| --- | --- | --- |
| Riverz CRM | Ecommerce merchants and customer conversations | Product facts, current offers, images, coverage, explicit order intent and support escalation |
| Riverz Dealers | Automotive sales | Adapting the shared conversation and lead workflow to vehicle-specific context |
| Riverz Ventas | Selling the software service | A separate business configuration and sales context rather than reusing a merchant's catalog |

## Reusable behavior, separate business facts

Intent handling, human handoff, uncertain-send recovery and contact restrictions can be shared. Catalogs, prices, shipping rules, identities and credentials must stay in the correct business context. A correct sentence with another merchant's facts is still an incorrect result.

## Evidence and limits

The private repositories include these workstreams and regression material. They are not published here as independently launched products, verified customer deployments or measured sales results. No customer messages, vehicle-client records or account credentials are included.

[Main case](README.md) · [Engineering](ENGINEERING.md)
