# Riverz CRM

**Commerce-focused conversations and automation.**

[Engineering notes](ENGINEERING.md) · [Juan Rios](https://github.com/excelenciaempire) · [Upstream foundation](https://github.com/ArnasDon/wacrm)

Riverz CRM brings merchant context into customer conversations: products, prices, available media, delivery conditions, and the point where a human should take over.

![Actual Riverz CRM dashboard in its native light theme and English interface](assets/dashboard.png)

*Direct screenshot of the running CRM dashboard, November 3, 2026. Native light theme and English interface; activity belongs to a platform review workspace. [Capture details](SCREENSHOTS.md).*

## The problem

A useful commerce assistant needs more than fluent replies. It must preserve the selected product, use that merchant's actual offer, handle unknown information, and respect human intervention. Integration failures must also remain visible to the operator.

## How I build with AI

**All of my development work presented here was done with AI assistance.** I use AI throughout implementation, debugging and validation. I understand programming and software engineering fundamentals, and use them to define requirements, guide the tools, review changes and check how the software actually behaves. I take responsibility for technical decisions and results.

## My work

I develop the commerce-specific product behavior and extensions: merchant-scoped assistant guidance, product knowledge and media handling, sales and support workflows, bilingual experiences, and integration recovery.

The project builds on **wacrm**, an open-source WhatsApp CRM template by Arnas Donauskas. The shared inbox, contacts, pipelines, campaigns, and automation foundation come from that project; I do not claim authorship of the original template.

## Representative capabilities

- Merchant-specific catalog, offer, delivery, and payment knowledge.
- AI-assisted conversations with explicit human handoff.
- Product-image references and conversation context.
- Commerce and messaging integrations with recovery paths.
- Spanish and English product interfaces.

## Stack

**TypeScript · React · Next.js · Tailwind CSS · Supabase/PostgreSQL · WhatsApp Business API**

## Engineering focus

The hard part is maintaining the relationship between conversation state, business facts, and external actions. A payment receipt is not proof of a settled payment; a timeout is not permission to send a message twice.

See the [engineering notes](ENGINEERING.md) for the approach to conversation validation and integration recovery.

## Repository scope

This is a public case study. Application source, account configuration, conversations, and customer data remain private. A capability described here does not imply that every external provider is currently connected or certified end to end.

For professional inquiries, [contact me through the Riverz showcase](https://github.com/excelenciaempire/riverz-showcase/issues/new?title=Professional%20inquiry).

## Related adaptations

[Riverz Dealers and Riverz Ventas](VARIANTS.md) adapt the same CRM family to different business contexts. The case distinguishes the shared wacrm foundation, Riverz extensions and business-specific configuration.
