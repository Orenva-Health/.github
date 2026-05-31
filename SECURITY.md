# Security policy — Orenva Health

Thank you for helping keep Orenva and the clinicians and patients
who use it safe.

This is the **organisation-wide default** security policy for every
repository under [Orenva-Health](https://github.com/Orenva-Health).
Where an individual repository has its own `SECURITY.md` (for
example, the [Orenva](https://github.com/Orenva-Health/Orenva)
product repo), that policy takes precedence for matters specific
to that repo.

## Reporting a vulnerability

**Please do not open a public issue for security vulnerabilities.**

Email **`security@orenvahealth.com`** with:

- A clear description of the issue and its potential impact
- Steps to reproduce (proof of concept, screenshots, or short
  video) — minimum: the exact request / payload that demonstrates
  the issue
- The repository, environment, or product surface you tested
- Your contact details so we can follow up

If the issue is sensitive enough that you want encryption, request
our PGP key in your first email and we will respond with a key
fingerprint within 24 hours.

## Our response

We respond to all security reports. The clock starts when the email
arrives:

| Severity | First acknowledgement | Initial assessment | Target fix or mitigation |
|---|---|---|---|
| **Critical** — active exploitation, RCE, mass PHI exposure | Within 1 business hour | Within 4 business hours | Within 24 hours |
| **High** — auth bypass, individual PHI exposure, persistent XSS | Within 4 business hours | Within 1 business day | Within 7 days |
| **Medium** — limited PHI exposure, stored XSS on auth pages, CSRF on sensitive flows | Within 1 business day | Within 3 business days | Within 30 days |
| **Low** — information disclosure, rate-limit gaps, configuration issues | Within 2 business days | Within 5 business days | Within 90 days |

Business hours: 09:00–18:00 UK time, Mon–Fri excluding public
holidays. Outside business hours we still aim to acknowledge
critical reports within a few hours.

These timelines mirror our internal Incident Response policy.

## Scope

**In scope** for every Orenva-Health repository:

- Code, configuration, and infrastructure-as-code in the repository
- Documentation that materially affects users' security posture
  (e.g. setup instructions, threat modelling docs)
- Vulnerabilities that arise from how the repository integrates
  with third-party services

**Out of scope**:

- Denial-of-service attacks
- Social engineering of Orenva staff
- Physical attacks
- Issues in third-party services (Vercel, Supabase, Cloudflare,
  Mistral, etc.) — please report these directly to the relevant
  vendor; if the issue is in how Orenva integrates with them, that
  *is* in scope
- Best-practice recommendations without an exploitable vulnerability
- Findings from automated scanners without a reproducible exploit
- Self-XSS, missing rate limits on pages without authentication,
  HTTP fingerprinting

## Safe harbor

We will not pursue or support legal action against security
researchers who:

- Make a good-faith effort to comply with this policy
- Stop testing once they have demonstrated a vulnerability
- Avoid privacy violations, the destruction or modification of data,
  and any interruption or degradation of our services
- Test only against your own accounts or accounts that you have
  explicit permission from the account holder to test against
- Do not disclose the vulnerability publicly until we have agreed
  it is fixed and you have agreed the disclosure timeline (typical
  embargo: 90 days from initial report, or earlier with mutual
  agreement)

## Patient and clinician data

Orenva processes clinical data subject to UK GDPR, EU GDPR (DSGVO),
and the UK Data Protection Act 2018.

If your research surfaces real patient or clinician data:

- **Stop testing immediately**
- **Do not download, copy, or distribute the data**
- Email `security@orenvahealth.com` with the smallest possible
  description that allows us to reproduce — typically the URL or
  request path and your account context, not the data itself
- We will treat any incidental contact with real personal data as a
  reportable incident under our Incident Response policy and will
  not pursue you for incidental access made in compliance with
  this policy

## Recognition

We do not yet run a paid bug bounty. We credit researchers who
report valid vulnerabilities in our security advisories and on a
forthcoming "Acknowledgements" page on our site, unless you ask to
remain anonymous. A paid program is on our roadmap once production
traffic justifies it.

## Disclosures

When a vulnerability is fixed, we publish a GitHub Security Advisory
on the affected repository. Coordinated disclosure happens after the
fix is deployed to production.

---

Thank you again.

— Jordan Gilbert (CTO) and Geet Patil (CEO), Orenva Health UK Ltd
