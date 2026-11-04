### John Stansberry-Wall

I build AI agents and the integrations behind them.

This year I designed, built and tested an AI intake and booking system for clinics in Texas that handles both phone calls and text messages, and deployed it on a live phone line for demos with clinic owners. When a message is urgent or clinical, it hands the conversation to staff instead of answering. The core of it is the integration layer: a Cloudflare Worker that books appointments through a scheduling platform's GraphQL API, with a Durable Object holding each caller's session, HMAC-signed requests, and clean recovery when a time slot disappears mid-conversation. I tested it end to end in the vendor's sandbox.

I also studied how 20 Texas med spas answer a new-patient text. 11 never replied.

Both are written up here: **[nightowlsystems.ai/work](https://nightowlsystems.ai/work)**.

The operations back end is public: **[nightowl-control-plane](https://github.com/nightowl-systems/nightowl-control-plane)** takes the signed webhooks from the voice and SMS platforms, merges them into one audited timeline per contact, raises incidents, and has tests for the parts that matter: signature checks, tenant isolation, duplicate deliveries. The booking Worker is available on request.

B.B.A., Cyber Security and Business, UTSA · Texas · [LinkedIn](https://www.linkedin.com/in/johnwall01)
