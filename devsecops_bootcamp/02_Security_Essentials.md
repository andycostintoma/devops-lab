# 02 – Security Essentials

## Scope of Security Knowledge
- DevSecOps requires broad-but-practical security literacy: enough to secure pipelines, infra, cloud, and platforms without becoming a full-time security specialist.
- Security = defending against malicious actors at every touchpoint (physical buildings, employee devices, cloud APIs, Kubernetes control planes).
- Specialized security careers (app sec, infra sec, cyber) go deeper; DevSecOps engineers need the distilled essentials to embed controls everywhere software ships.

## Why Security Matters
- Breaches cost trillions; examples include Capital One/AWS, T-Mobile, LinkedIn, Adobe—each paid massive fines or suffered reputational damage.
- Large orgs are juicy targets because they hold millions of valuable records; regulation enforces protection (banks, healthcare/HIPAA, GDPR, PCI).
- Governments impose compliance + audits; failure = lawsuits, fines, mandatory remediation budgets (e.g., T-Mobile’s $350M payout + $150M security spend).
- Investing up front is cheaper than breach response; but defenders must secure every entry point while attackers only need one.

## Security Posture & Measurement
- *Security posture* = current state of protection across apps + infra; you need visibility into every entry point to know what’s exposed.
- DevSecOps pipelines continuously assess posture (scans, policy-as-code) so teams see open “doors/windows” before attackers do.

## Defense-in-Depth Mindset
- Mirror physical security layers (guards, vaults) with digital layers (access controls, network segmentation, logging).
- Secure every vector: user devices, employee credentials, servers, databases, cloud accounts, IoT/printers.
- Layered controls limit blast radius: fence ⇨ locked doors ⇨ safes; analog in tech = firewalls ⇨ IAM ⇨ encrypted data ⇨ logging.
- Principle of least privilege applies to people *and* services (Jenkins, pods, front-end containers only get the access they need).

## Common Attack Categories (Lecture + Handout)
- **Social Engineering/Phishing:** humans are entry points (Twitter 2020, Yahoo phishing). Craft personalized lures, intercept DNS, or fake support calls to gain corporate access.
- **Cross-Site Scripting (XSS):** malicious JS executes in the browser via unvalidated input (e.g., comments). Often escalates into **Client-Side Request Forgery (CSRF)** by stealing cookies/sessions.
- **Server-Side Request Forgery (SSRF):** attacker forces backend services to call internal resources (storage, metadata endpoints) bypassing firewalls/VPNs.
- **SQL Injection:** unsanitized queries expose/manipulate/delete DB data; root cause in Heartland breach example.
- **Software Supply Chain:** vulnerable/malicious libraries or auto-updaters (e.g., Equifax/Apache Struts). Track CVEs, verify sources, enforce integrity checks.
- **Brute Force & Weak Auth:** reused/weak passwords, no MFA, brittle recovery flows (LastPass master password caution).
- **Denial of Service:** botnets flood services, exhausting bandwidth/connections so legit requests fail.
- **Vendor/3rd-Party Abuse:** attackers compromise SaaS/cloud vendors (Stripe, S3, password managers) and pivot into your environment.

## Vendor & Third-Party Risk
- Your security equals the weakest vendor’s security. SaaS providers, payment gateways, cloud platforms—if they’re breached, you are too.
- Validate vendors, monitor their CVEs, and have contingency plans.
- Supply-chain issues include: downloading binaries via `curl | sh` from unverified URLs, auto-updaters without signature checks, plugins maintained by unknown actors.

## OWASP & Top Ten Risks (PDF Highlights)
- OWASP Top Ten = reference list of critical web-app risks updated regularly; every org should adopt it.
- OWASP community (governments, companies, volunteers) produces open-source tools, training, and standards; DevSecOps teams use OWASP as baseline guidance.
- Eight top-ten items come from incident data; two come from practitioner surveys to capture emerging threats not yet widespread.
- Top risks & examples:
  1. **Broken Access Control** – violating least privilege, bypassing checks, exposure of unauthorized data.
  2. **Cryptographic Failures** – weak/no encryption, insecure protocols, hard-coded secrets.
  3. **Injection** – JS/SQL/NoSQL/template injection via unsanitized input; always validate & assume malicious input.
  4. **Insecure Design** – missing threat modeling, poor credential/permission handling, insecure reference architectures.
  5. **Security Misconfiguration** – open ports, default creds, debug features left on; can occur at any layer.
  6. **Vulnerable & Outdated Components** – no inventory/patching for libs; same risk as custom code.
  7. **Identification & Authentication Failures** – weak passwords, no MFA, session not invalidated, poor recovery flows.
  8. **Software & Data Integrity Failures** – unverified plugins, unsigned auto-updates, weak signatures.
  9. **Security Logging & Monitoring Failures** – without telemetry you’re blind and breaches persist.
 10. **Server-Side Request Forgery (SSRF)** – apps fetch remote resources without validating URLs; attackers port-scan, hit metadata, reach protected resources.

## Layered Security (Defense in Depth)
- Combine access management, network segmentation, application controls, logging + monitoring.
- Goal: compromise in one layer must not grant full-system access; always contain blast radius.
- Map the house analogy: perimeter (firewalls), front door (user auth), inner rooms (service auth), safes (encryption + vaults), cameras (logging), alarms (monitoring/alerting).

## Logging, Monitoring & Alerting
- Logging = record every important event (logins, failed attempts, admin actions, money movement, infra changes).
- Monitoring = analyze logs for unusual patterns (40 failed logins, sudden spikes, access outside policy).
- Alerting = notify + trigger incident response quickly; without telemetry you’re “blind and deaf” and breaches persist for months (children’s health provider incident ran 7+ years).
- Post-incident forensics require logs to trace attacker path and fix root causes.

## Compliance Foundations
- Industries force security via laws (HIPAA, PCI, GDPR). Compliance = documented controls + audits + enforcement.
- Security incidents often trigger lawsuits + regulatory reviews; DevSecOps automates evidence collection and control enforcement (compliance-as-code later in course).

## Key Takeaways for DevSecOps Engineers
- Understand threat landscape (phishing, XSS, SSRF, SQLi, CVEs, DoS, supply chain) to appreciate “why” behind automated checks.
- DevSecOps introduces continuous monitoring, scanning, and remediation into DevOps pipelines so issues never reach production.
- Stay updated on vulnerabilities, enforce secure coding, validate libraries, and automate policy enforcement early in the SDLC.
- Measure + communicate security posture continuously; use OWASP guides + layered controls to prove improvements and prioritize remediation.
