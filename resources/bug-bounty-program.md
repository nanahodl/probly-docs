---
description: >-
  Report security vulnerabilities affecting Probly through our responsible
  disclosure program.
---

# Bug Bounty Program

_Last updated: July 10, 2026_

## 1. Purpose

Probly protects user accounts, funds, trading activity, market integrity, and platform availability.

This program supports responsible security research and disclosure. It covers Probly-owned applications, APIs, backend services, authentication, wallet login, account systems, trading, execution, settlement, synchronization, and market resolution.

## 2. Reporting channel

Submit vulnerability reports to [security@probly.com](mailto:security@probly.com).

Include a clear vulnerability description, affected asset, reproduction steps, impact analysis, and relevant evidence. Evidence may include screenshots, videos, logs, or a proof of concept.

Do not disclose, share, or discuss vulnerability details before written approval. Probly must complete remediation before approving disclosure.

## 3. Scope

The following assets and areas are in scope:

* `*.probly.com`
* Probly-owned web applications, APIs, and backend services
* Authentication, wallet-login, account-linking, and session-management flows
* Trading, orders, positions, balances, rewards, payouts, settlement, market resolution, and state synchronization
* Integrations that directly affect Probly users, accounts, trades, balances, payouts, or market state
* Other assets Probly explicitly adds to this program

Administrative and internal functionality is in scope for reporting only. Do not actively attack, bypass, or abuse admin systems, employee accounts, internal controls, or enterprise identity systems.

If you discover unauthorized internal or admin access, stop testing immediately. Report it to [security@probly.com](mailto:security@probly.com).

Contact us before testing if an asset's scope is unclear.

## 4. Severity classification

Probly may use industry classifications, including the Bugcrowd Vulnerability Rating Taxonomy. Final severity depends on demonstrated impact, exploitability, affected users and assets, business impact, and report quality.

<table><thead><tr><th width="109.828125">Priority</th><th>Severity</th><th width="467.2578125">Maximum reward</th></tr></thead><tbody><tr><td>P1</td><td>Critical</td><td>Up to 100,000 USDC/USDT</td></tr><tr><td>P2</td><td>High</td><td>Up to 20,000 USDC/USDT</td></tr><tr><td>P3</td><td>Medium</td><td>Up to 3,000 USDC/USDT</td></tr><tr><td>P4</td><td>Low</td><td>No guaranteed cash reward. Probly may reward or acknowledge at its discretion.</td></tr></tbody></table>

Issues affecting funds, accounts, authentication, wallet login, trading, settlement, payouts, balances, synchronization, or administrative permissions may receive higher ratings. The demonstrated impact must justify the rating.

Reports may be downgraded or ineligible when impact is limited. This includes unrealistic conditions, insufficient proof, scanner-only output, or researcher-only impact.

## 5. Rewards

Probly may pay rewards in USDC or USDT. Probly determines the payment asset.

Rewards depend on final severity, demonstrated impact, exploitability, affected users and assets, business impact, duplicate status, and report quality.

P1–P3 rewards are maximums, not guarantees. Probly determines each final reward at its sole discretion.

P4 issues may not receive a cash reward. Probly may provide a reward, acknowledgement, or other recognition.

Informational, duplicate, known, out-of-scope, best-practice, and scanner-only reports are not eligible. Probly may decline valid reports with low, unclear, impractical, or irrelevant impact.

## 6. Probly-specific impact areas

These areas receive particular consideration:

* Unauthorized account access or modification
* Flaws in authentication, wallet login, account linking, or sessions
* Unauthorized orders, cancellations, position changes, or trading authority
* Unauthorized balance, reward, payout, or settlement changes
* Errors affecting trading, execution, settlement, synchronization, or integrations
* Unfair trading advantages or financial loss
* Unauthorized market outcome, status, resolution, or payout changes
* Sensitive data exposure affecting accounts, funds, trading, or permissions
* Unauthorized administrative or internal access affecting Probly systems
* Availability failures affecting critical platform functions

## 7. Severity guidelines

### P1 — Critical

P1 issues can cause severe harm, direct financial loss, widespread account compromise, or major production compromise.

Examples include:

* Theft, loss, withdrawal, transfer, or manipulation of user funds
* Full account takeover without user interaction
* Large-scale account compromise through authentication or wallet-login flaws
* Unauthorized third-party orders, cancellations, positions, settlement actions, or market resolution
* High-risk admin access affecting balances, orders, payouts, settlement, or market state
* Remote code execution on production systems
* Production access exposing session tokens, internal credentials, or sensitive information
* Widespread incorrect trades, positions, balances, payouts, or market states
* Long-term outages affecting login, trading, orders, settlement, or payouts

### P2 — High

P2 issues cause significant harm but have limited scale or require additional conditions.

Examples include:

* Unauthorized access to another user's orders, positions, profile, or trading data
* Account takeover requiring meaningful user interaction
* Limited account risk through authentication, wallet-login, linking, or session flaws
* Limited-impact admin or internal access
* Administrative permission or authorization bypass with clear security impact
* Limited exposure of session tokens, internal credentials, or sensitive information
* Stored XSS performing authenticated actions or accessing sensitive data
* Authentication or authorization bypass affecting important functionality
* Limited incorrect trading, balances, payouts, or unfair trading advantage
* Security issues materially harming market integrity or user trust

### P3 — Medium

P3 issues have meaningful impact but limited exploitability, scope, or financial effect.

Examples include:

* IDOR affecting non-critical user data
* Reflected XSS with demonstrated impact
* CSRF affecting non-critical state-changing actions
* Limited-impact API authorization flaws
* Moderate authentication, wallet-login, linking, or session issues
* Data-integrity errors affecting market or price displays
* Limited trading, execution, settlement, or synchronization consistency issues
* Rate-limit bypass with demonstrated business or security impact
* Open redirects with realistic phishing or account-security impact

### P4 — Low

P4 issues have limited practical exploitability or provide defense in depth.

Examples include:

* Minor non-sensitive information disclosure
* Security-header misconfiguration with limited demonstrated impact
* Low-impact UI injection
* Broken external links with limited security impact
* Low-impact misconfiguration without account compromise or sensitive-data exposure

## 8. In-scope vulnerability categories

Relevant categories include:

* Account takeover and authentication bypass
* Authentication, wallet-login, account-linking, and session-management flaws
* API authentication and authorization flaws
* IDOR affecting accounts, orders, positions, balances, rewards, payouts, or private information
* Unauthorized trading actions and accounting logic errors
* Market-resolution, market-status, settlement, payout, and state-synchronization flaws
* Trading-request, settlement-request, or state-update integrity flaws
* Admin access-control or permission bypasses
* Sensitive data exposure with clear security impact
* Remote code execution or impactful server-side request forgery
* Stored or reflected XSS with demonstrated security impact
* CSRF with demonstrated state-changing impact
* Availability issues affecting critical functionality without disruptive testing

## 9. Market integrity issues

Probly may consider market integrity reports with a specific implementation flaw. The flaw must create material risk to users or platform correctness.

Examples include:

* Incorrectly displayed market rules, status, or resolution criteria
* A mismatch between displayed outcomes and settlement logic
* Incorrect payout, position, balance, or settlement displays
* Unauthorized changes to market status, results, or resolution data
* Materially incorrect trading, balance, settlement, or payout information

Outcome disagreements, trading losses, odds movement, and prediction accuracy are not security issues. Reports must demonstrate a specific Probly implementation flaw.

## 10. Out of scope

The following are generally out of scope:

* Informational findings without demonstrated security impact
* Scanner-only reports or best-practice recommendations without exploitability
* Missing headers, self-XSS, or clickjacking without a sensitive action
* Open redirects or CORS issues without demonstrated security impact
* SPF, DKIM, DMARC, enumeration, or rate-limit reports without material impact
* Public on-chain data or publicly queryable wallet information
* Unexploited third-party vulnerabilities or third-party service issues
* Employee, device, email, office, internal, or identity-system attacks
* Staging, test, development, or demo issues without production impact
* UI, spelling, grammar, translation, or content issues
* Market disagreements, odds movement, losses, liquidity, or outcome disputes
* Issues requiring compromised devices, malware, malicious extensions, or physical access
* Social engineering, phishing, physical attacks, or attacks on people or support channels
* Denial-of-service, stress testing, load testing, spam, scraping, or high-volume automation
* Highly unrealistic conditions, duplicates, known issues, or premature public disclosures

Third-party issues qualify only when a Probly implementation flaw directly affects Probly users or systems.

## 11. Testing rules

Researchers must:

* Use only accounts they own or may explicitly use
* Avoid accessing, modifying, deleting, or exfiltrating others' data
* Avoid degrading, interrupting, or damaging Probly services
* Avoid denial-of-service, stress tests, spam, scraping, and high-volume automation
* Avoid real trades, financial loss, market disruption, or unwanted third-party activity
* Never seek trading advantage, market manipulation, financial gain, or user harm
* Never attack, bypass, brute-force, phish, or abuse employee or internal systems
* Stop immediately after discovering sensitive data, unauthorized access, or high-impact issues
* Keep all vulnerability details confidential until written disclosure approval

If you find an admin entry point, API, function, or bypass path, stop testing. Do not browse, operate, export, modify, or delete internal data.

Violations may result in reward ineligibility and removal from the program.

## 12. Report requirements

A valid report includes:

* A clear vulnerability description
* The affected asset, endpoint, page, or feature
* Step-by-step reproduction instructions
* Relevant screenshots, video, logs, or proof of concept
* A clear security-impact explanation
* Required test account information
* The affected environment
* Suggested remediation, where available

Reports without sufficient reproduction detail or impact may be ineligible or receive lower severity. Probly may request additional evidence for high-impact reports.

Do not continue testing where it increases risk to users, funds, markets, or availability.

## 13. Duplicate reports

Probly generally rewards the first valid report with enough detail to reproduce and assess the issue.

Duplicate reports are not eligible. Probly may make an exception for a materially different impact or exploit path.

## 14. Eligibility

To qualify for a reward, you must:

* Be the first to report an unknown vulnerability
* Report directly through the approved channel
* Provide enough information to reproduce and fix the issue
* Follow this policy and applicable laws
* Avoid public disclosure before authorization
* Avoid exploitation, data exfiltration, disruption, trading advantage, and market manipulation

Employees, contractors, vendors, and affected-code contributors may be ineligible.

## 15. Safe harbor

Probly will not pursue legal action against good-faith researchers who follow this policy. Researchers must avoid harm and promptly report vulnerabilities through the approved channel.

Safe harbor excludes extortion, threats, data theft, privacy violations, service disruption, social engineering, physical attacks, trading advantage, market manipulation, and personal financial gain.

## 16. Disclosure

Keep vulnerability details confidential until Probly completes remediation and gives written approval.

Premature public disclosure, third-party sharing, social media posts, or publicity may make a report ineligible.

## 17. No employment or service relationship

This policy creates no employment, contractor, agency, partnership, or service-provider relationship.

Participation is voluntary. Researchers may not represent Probly or test outside this policy's scope and rules.

Reviewing a report, assigning severity, or providing a reward creates no ongoing obligation, contract, or guaranteed payment.

## 18. Program changes

Probly may modify, pause, or terminate this program at any time.

Probly determines reward amounts, scope, severity, eligibility, and final payout decisions at its sole discretion.
