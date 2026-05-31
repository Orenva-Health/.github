# Orenva Health

**EU-sovereign clinical documentation AI for UK and German private practice.**

Every other ambient scribe sends your patient's voice to OpenAI's
servers in the United States. Orenva runs entirely on EU-hosted
infrastructure with EU-hosted models. Your consultation never leaves
the EU.

---

### What we're building

A web application at **app.orenvahealth.com** that records a
consultation, structures it into a clinical note via EU-hosted AI,
and lets the clinician edit, sign-off, and export — to clipboard,
PDF, or directly to their EMR.

The stack is engineered around data sovereignty as a first-class
commitment:

- **Audio storage** — Supabase London region
- **Speech-to-text** — Whisper Large v3 on Hetzner GPU in Frankfurt
- **LLM structuring** — Mistral Large 2 via Mistral's Paris API
- **Application** — Vercel London region (`lhr1`)
- **Corporate email** — Tuta (Germany)
- **Error monitoring** — Sentry EU (`de.sentry.io`)
- **Product analytics** — PostHog EU host

No US data dependencies. No OpenAI. No Anthropic-US. End-to-end EU.

### Compliance posture

- UK GDPR + EU GDPR + DPDP Act 2023 aligned
- MHRA + EU MDR mapping (Class I medical device — structuring, not
  decision support)
- NHS DSPT + DTAC framework readiness
- ISO 27001 — in progress
- SOC 2 ready, formal attestation roadmap

Full policy pack at [Orenva-Compliance](https://github.com/Orenva-Health/Orenva-Compliance) (private).

### For clinicians

When the product launches you'll be able to:

- Sign up at [app.orenvahealth.com](https://app.orenvahealth.com)
  with your work email (no password — magic link)
- 14-day free trial · then £119/month individual or £99/seat for
  practices of 5+
- Cancel anytime · export all data anytime · DSAR-grade deletion

### For investors

Information at [investors.orenvahealth.com](https://investors.orenvahealth.com).
Email [admin@orenvahealth.com](mailto:admin@orenvahealth.com) for portal access.

### For security researchers

We follow [RFC 9116](https://www.rfc-editor.org/rfc/rfc9116). Disclosure
contact and PGP key at
[orenvahealth.com/.well-known/security.txt](https://orenvahealth.com/.well-known/security.txt).

### Team

- **Geet Patil** — CEO
- **Jordan Gilbert** — CTO

UK Limited Company incorporating shortly.

### Repositories

- [Orenva](https://github.com/Orenva-Health/Orenva) — application code, marketing site, clinician app, investor portal
- [Orenva-Compliance](https://github.com/Orenva-Health/Orenva-Compliance) — SOC 2-aligned policy pack (private)
