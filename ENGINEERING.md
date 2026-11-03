# Engineering notes

## Foundation and extensions

Riverz CRM uses the open-source [wacrm](https://github.com/ArnasDon/wacrm) foundation. This case study focuses on the commerce-specific work added around that foundation: assistant behavior, merchant knowledge, channel and store integrations, onboarding, and operational recovery.

## Merchant context is part of correctness

Each merchant has its own catalog, current offer, shipping coverage, payment methods, and support policies. Reusing conversational behavior should not copy one merchant's facts into another merchant's account.

The shared assistant behavior covers intent, product selection, unanswered questions, explicit closing, and escalation. Business facts remain account-specific.

## Validate complete conversations

A response can look correct in isolation while the whole interaction fails. Useful scenarios include a buyer asking for more images, changing quantity, asking about compatibility, reporting an existing order, requesting a human, or asking not to be contacted.

The private project includes regression coverage and a preview workflow for these behaviors. Test scenarios should not create real orders or send unsolicited messages to customers.

## External actions and uncertain outcomes

An external timeout can leave the result unknown. A message send therefore needs a stable identity and a recovery path rather than an unconditional retry. Human intervention and contact restrictions must remain part of the decision to send.

Integration status has a similar problem: clearing an error message does not establish a healthy connection. Successful reads, persisted state, and failure recovery need to agree. Concurrent token or connection updates should not overwrite each other with stale snapshots.

## Evidence boundaries

The case study describes implemented behavior and documented engineering constraints. It does not publish customer conversations, conversion claims, or blanket availability guarantees for external services.

## Discuss in an interview

I can walk through merchant isolation, conversation-level testing, recovery after an uncertain send, and extending an existing open-source foundation without confusing upstream work with my own contributions.
