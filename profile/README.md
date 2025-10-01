# Welcome to EDAMAME Technologies

EDAMAME ensures all machines accessing code, secrets, or sensitive test data are secured without the challenges of traditional Unified Endpoint Management. Empower every stakeholder—from contractors to developers—to safeguard the software development lifecycle without slowing down development.

## For Individual Developers

### EDAMAME Security: Free App

EDAMAME Security is your all-in-one tool to secure, understand, and prove your dev workstation—from OS to network. It delivers:

- **Security Benchmarks:** Assess against standards like [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks), SOC 2, and ISO 27001
- **AI Analysis:** Anonymized, holistic posture summaries and action plan using a frontier LLM
- **One-Click Remediation:** Automatically fix common security issues without requiring deep security expertise
- **Network Visibility:** Built-in network scanning (inspired by 'Nmap') and traffic monitoring (inspired by 'Wireshark'). Anonymized, RAG‑based analysis of device vulnerabilities and suspicious traffic sessions; ML‑based traffic anomaly detection
- **Digital Identity Management:** Integrated with [Have I Been Pwned](https://haveibeenpwned.com) for online identity management with AI analysis of security impact
- **Compliance Reports:** Generate tamper-proof reports to demonstrate security compliance to clients with a single click
- **Certified Compliance Report Generation:** Contractors required to prove their device meets baseline security requirements (SOC 2 or ISO 27001) can generate a compliance report with a single click.
- **Privacy-First Management:** Connects to our "no MDM" platform ([edamame.tech](https://www.edamame.tech)), enabling continuous reporting of security posture and integration with access control to implement Zero Trust for code, secrets, and test data access.

https://github.com/user-attachments/assets/72fb4115-ac79-4267-b79c-fba2a5dfed9e

See: [EDAMAME Security Public Repo](https://github.com/edamametechnologies/edamame_security)

### Security Without Undermining Productivity

- **CLI or GUI Interface:** Use the app interface or CLI commands (`edamame_posture score`, etc.) - they have equivalent functionality
- **Self-Directed Assessment:** Evaluate your workstation's security posture against industry standards independent of any central management
- **Local-Only Controls:** Enforce security policies without external dependencies or registration requirements
- **Developer Workflow Integration:** Add security gates to your personal CI/CD pipeline with exit-code-based controls

### EDAMAME Posture: Free CI/CD CLI

Protect your personal repositories and projects with powerful CI/CD security tools:

- **Available Tools:**
  - **CLI Tools:** For Windows, macOS, or Linux ([GitHub](https://github.com/edamametechnologies/edamame_posture_cli))
  - **GitHub Action:** Seamless GitHub integration ([GitHub](https://github.com/edamametechnologies/edamame_posture_action))
  - **GitLab Action:** Integration for GitLab CI/CD workflows ([GitLab](https://gitlab.com/edamametechnologies/edamame_posture_action))

#### Key Security Use Cases

1. **Runner Hardening & Validation**
   - Automatically scan for vulnerabilities and misconfigurations in your CI/CD environment
   - Enforce minimum security scores on runners before allowing builds to proceed
   - Apply automatic remediations to fix common security issues in ephemeral environments
   - Example: `edamame_posture check-policy 2.0 "encrypted disk disabled,critical vulnerability" "SOC-2"`

2. **Egress Traffic Control & Anomaly Detection**
   - Create whitelists based on normal build behavior to define allowed network connections
   - Detect and block suspicious outbound connections that could indicate supply chain attacks
   - Generate network audit trails for security verification and incident response
   - Example: `edamame_posture background-start-disconnected true github_ubuntu`

3. **Pipeline Security Gates**
   - Fail builds when security posture doesn't meet requirements, preventing insecure code deployment
   - Verify that code commits originated from properly secured environments
   - Ensure network traffic conforms to defined whitelists during the build process
   - Example: `edamame_posture get-sessions` (returns non-zero exit code if whitelist is violated)

Example GitHub Action for your personal repository:
```yaml
- name: Setup EDAMAME Posture
  uses: edamametechnologies/edamame_posture_action@v0
  with:
    network_scan: true
    auto_remediate: true
    edamame_minimum_score: 2.0
    custom_whitelists_path: ./.github/workflows/whitelist.json
    whitelist_conformance: true  # Fail pipeline if unauthorized network traffic detected
```

**Real-world scenario:** During a build, your runner makes unexpected connections to unknown IP addresses or domains. EDAMAME detects this unauthorized egress traffic, fails the pipeline, and provides detailed logs showing what connections violated your whitelist — potentially preventing a supply chain attack or data exfiltration incident.

**How EDAMAME detected CVE-2025-30066:** When the popular GitHub Action tj-actions/changed-files was compromised in March 2025, attackers modified it to leak CI/CD secrets by making unauthorized network calls to fetch a malicious payload from gist.githubusercontent.com. EDAMAME's network monitoring detected this exact attack pattern during our security testing. By capturing all packet-level traffic from the CI runner and enforcing strict network whitelists, EDAMAME immediately flagged the suspicious outbound connection that other tools missed. This Zero Trust approach to CI/CD networking effectively prevented the payload from being executed, protecting thousands of repositories from credential theft — demonstrating why comprehensive network visibility is essential for modern supply chain security.

- **Zero-Configuration Integration:** Add security gates to your personal repositories with minimal setup
- **Local Policy Enforcement:** Define and enforce security standards without requiring external registration or connectivity
- **Disconnected Network Monitoring:** Monitor and enforce network traffic whitelists in your CI/CD pipeline
- **Security Signatures:** Add cryptographically verifiable security posture signatures to your commits and releases
- **Automated Runner Hardening:** Automatically secure CI/CD runners and respond to security posture changes
- **Security Beyond Compliance:** Address network risks with automated audits and integrated network scanning

## For Development Teams & Enterprises

### EDAMAME Hub: Freemium SaaS

Enhance your organization's security posture with team-focused capabilities:

- **Cross-Team Standardization:** Enforce consistent security policies across all development teams
- **Security Visibility:** Monitor security posture across your entire device fleet
- **Policy Compliance Reporting:** Generate aggregated compliance reports for auditors
- **Conditional Access Controls:** Automatically restrict access to sensitive systems based on security posture
- **Centralized Policy Management:** Define policies in EDAMAME Hub that apply across all pipeline runs
- **Domain-Based Policy Checks:** Ensure adherence to organization-wide standards
- **Audit Trail:** Generate comprehensive audit trails of security posture across your build environments
- **Historical Verification:** Verify that code was committed from compliant environments
- **Tiered Security Controls:** Progress from local checks to domain-managed policies as your security needs mature

### Quickstart
Access the free plan of our SaaS service for enterprises, including a demo on a simulated domain: [EDAMAME Hub](https://hub.edamame.tech).
Create your domain, verify it, and onboard your users through the Onboarding tab.

https://github.com/user-attachments/assets/335298d0-9e26-4eb3-a388-f1ce6471822d

### User-up Security for Your SDLC

EDAMAME's "reporting-only" architecture prevents remote control of endpoints, reducing legal and privacy liabilities while building trust and shared responsibility:

- **Centralized Policy Management:** Define and enforce security requirements through [EDAMAME Hub](https://hub.edamame.tech)
- **Continuous Compliance:** Track security posture across the development lifecycle
- **No Admin Abuse:** Ideal for contractors and third parties who remain confident and cooperative
- **Zero Trust Access Control:** Conditionally grant access to code, secrets, and test data based on security posture

### Zero Trust Integration

EDAMAME integrates with your existing security infrastructure:

- Compatible with REST or GraphQL-supporting APIs for seamless integration
- Works with Identity Providers, Application Providers, and Network Access Control systems
- Only secure, recognized endpoints can access critical resources
- Learn more: [Integrations](https://github.com/edamametechnologies/integrations)

## EDAMAME Core (Closed Source)

EDAMAME Core is the central engine that powers both the EDAMAME Security application and the EDAMAME Posture CLI. While closed source, it provides the high‑performance primitives that underpin the platform:

- **Cross‑platform assessment engine**: Consistent posture evaluation across macOS, Windows, and Linux
- **Threat detection & scoring**: Policy‑driven findings compiled into a unified security score
- **System configuration analysis**: Deep OS checks with remediation orchestration
- **Network visibility**: LAN discovery, traffic monitoring, and session analysis
- **Intelligent advisory system**: Guided fixes with state tracking and progress monitoring
- **Privileged operations via Helper**: Secure separation for actions requiring elevated rights
- **Optimized runtime**: Async, resource‑efficient implementation for desktop and CI/CD environments
- **Service interface**: RPC surface consumed by the app and developer CLI

## Key Open Source Components

EDAMAME maintains several open source projects that power the platform and can be used independently:
- **[Threat Models](https://github.com/edamametechnologies/threatmodels)**: Public repository of security benchmarks, policies, whitelists/blacklists, and signatures used by the platform. See **[Threat Models Wiki](https://github.com/edamametechnologies/threatmodels/wiki)**.
- **[Flodbadd](https://github.com/edamametechnologies/flodbadd)**: Network visibility engine for packet capture, session analysis, whitelists/blacklists, and on‑device anomaly detection. An example tool using it is **[Flodviddar](https://github.com/edamametechnologies/flodviddar)**.
- **[Undeadlock](https://github.com/edamametechnologies/undeadlock)**: Low‑overhead diagnostics for async locks and maps to surface contention/deadlocks during development.
- **[Extended Isolation Forest](https://github.com/edamametechnologies/extended-isolation-forest)**: Our fork of the **[extended-isolation-forest Rust crate](https://github.com/nmandery/extended-isolation-forest)** used for egress traffic ML anomaly detection.

Our system helper is fully open source:
- **[EDAMAME Helper](https://github.com/edamametechnologies/edamame_helper)**: Privileged companion app that safely executes checks and remediation steps requiring elevated rights.

It relies on open source libraries:
- **[EDAMAME Models](https://github.com/edamametechnologies/edamame_models)**: Signature‑based cloud data model manager with custom overrides and thread‑safe access.
- **[EDAMAME Foundation](https://github.com/edamametechnologies/edamame_foundation)**: Core Rust library for posture assessment, threat models, secure helper IPC, scoring, and policy enforcement.

Our closed source EDAMAME Core (Rust) uses the following additional libraries:
- **[EDAMAME Backend](https://github.com/edamametechnologies/edamame_backend)**: Complete list of data structures used to communicate with the backend.

The CLI wrappers for edamame_core are fully open source:
- **[GitHub Action](https://github.com/edamametechnologies/edamame_posture_action)** / **[GitLab Action](https://gitlab.com/edamametechnologies/edamame_posture_action)**: CI/CD integrations to enforce posture and network controls in pipelines.
- **[EDAMAME CLI](https://github.com/edamametechnologies/edamame_cli)**: Developer‑friendly interface to EDAMAME core services with interactive RPC exploration.
- **[EDAMAME Posture CLI](https://github.com/edamametechnologies/edamame_posture_cli)**: Cross‑platform CLI to assess posture, remediate issues, enforce policies, and generate compliance reports.
