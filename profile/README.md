# Welcome to EDAMAME Technologies

**The trust layer for AI agents and the machines they run on.** Trust is proven by both security posture and runtime behavior, on workstations, CI/CD runners and any server running AI agents, cloud or self-hosted.

EDAMAME continuously verifies each machine's security posture and what each AI agent actually does, then binds access to code, secrets, production and critical company resources to that proof. Developers keep moving, leaders get proof, and the workstations, runners and AI agents behind delivery stay protected without MDM/UEM lockdown or remote device control.

**Watch:** [the 30-second trailer](https://youtu.be/uCH1o07rPcA) · [AI agent attacks caught from outside the agent, the 13-minute demo](https://youtu.be/oTv7t_aw26c) · [every video, by product, in the Demo Center](https://www.edamame.tech/demo-center?utm_source=github&utm_medium=referral&utm_campaign=github-readme)

## Products

EDAMAME uses one trust layer across developers, CI/CD and AI agents, with specific product surfaces for workstations, CI/CD and AI agent infrastructure, and fleet visibility:

| Product | Form Factor | Target Environment |
|---------|-------------|-------------------|
| **[EDAMAME Security](https://github.com/edamametechnologies/edamame_security)** | Desktop/mobile app | Workstations, personal devices, and the AI agents running on them |
| **[EDAMAME Posture](https://github.com/edamametechnologies/edamame_posture_cli)** | CLI | CI/CD runners and any server running AI agents, cloud or self-hosted |
| **[EDAMAME Hub](https://hub.edamame.tech)** | SaaS dashboard | Fleet visibility, AI governance, posture proof, compliance evidence, and posture-based access |
| **[EDAMAME Portal](https://portal.edamame.tech)** | Account portal | Authentication, account access, and managed LLM subscription |

### AI-Powered Security

EDAMAME Security and EDAMAME Posture share the same core intelligence and operate autonomously:

```
OBSERVE  →  Continuous monitoring of threats, network, traffic, and identity
ANALYZE  →  LLM-powered analysis with risk scoring and pattern recognition
DECIDE   →  auto_resolve (safe actions) or escalate (risky actions needing review)
ACT      →  Remediate threats, dismiss false positives, update whitelists
REPORT   →  Slack notifications, Hub dashboards, compliance reports
```

**Key Principle**: Human-in-the-loop safety. Risky decisions are escalated and all actions are reversible.

Detection itself is deterministic and runs on the device with no LLM; a model is optional and adds explanations, the review of findings and the Assistant's fixes (see [what needs an LLM and what does not](https://github.com/edamametechnologies/edamame_security#deterministic-by-design-what-needs-an-llm-and-what-does-not)).

### EDAMAME Portal & Shared LLM Subscription

EDAMAME Security and EDAMAME Posture can use **EDAMAME's managed LLM service** through the [EDAMAME Portal](https://portal.edamame.tech), eliminating the need for separate API keys:

| Feature | Description |
|---------|-------------|
| **Unified Account** | Single login for both Security and Posture |
| **Managed LLM** | No third-party API keys needed |
| **Usage Dashboard** | Track LLM usage across all your devices and pipelines |
| **Subscription Tiers** | Free tier included; paid plans for higher limits |
| **API Keys** | Generate keys for headless/CI environments |

**Authentication:**
- **EDAMAME Security (GUI)**: OAuth sign-in through EDAMAME Portal
- **EDAMAME Posture (CLI)**: API key via `EDAMAME_LLM_API_KEY` environment variable

**Alternative Providers**: Both products also support Claude (Anthropic), OpenAI, and Ollama (local) if you prefer bring-your-own LLM.

**Documentation:** [EDAMAME Portal README](https://github.com/edamametechnologies/edamame_portal) | [Portal Wiki](https://github.com/edamametechnologies/edamame_portal/wiki)

## For Individual Developers

### EDAMAME Security: Free

EDAMAME Security is your all-in-one tool to secure, understand, and prove your workstation and the AI agents on it, from OS to network. It delivers:

- **Security Benchmarks:** Assess against standards like [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks), SOC 2, and ISO 27001
- **AI agent visibility:** the AI agents on the machine (Cursor, Claude Code, Claude Desktop, OpenClaw, Codex, Hermes), what they can reach, and whether they do what they declared: intent divergence and attack-pattern detection, with no plugin installed
- **AI Assistant and protection:** one Protection switch turns on the Assistant, attack pattern detection and intent divergence detection together. The Assistant triages security issues at one of two levels, **Review** (it recommends, you confirm) or **Auto** (it fixes safe issues and escalates the rest), and every fix can be undone. Supports multiple LLM providers:
  - **EDAMAME Portal LLM** - Managed AI service with OAuth authentication via EDAMAME Portal; free and paying tiers (see [portal.edamame.tech](https://portal.edamame.tech)); zero API key management
  - **Claude (Anthropic)** - Detailed reasoning and nuanced security decisions (API key required)
  - **OpenAI (GPT)** - Fast responses and general-purpose analysis (API key required)
  - **Ollama (Local)** - Privacy-focused, runs entirely on your machine (no cloud dependency)
  - **MCP Server** - Localhost Model Context Protocol (MCP) server (desktop builds) with per-client pairing or PSK authentication, giving external AI tools 52 read-oriented tools
  - **Detections and AI History** - Detections lists every attack-pattern and divergence finding; AI History lists the Assistant's actions, with filters, Confirm pending / Undo all, the reasoning of each action and deep links to the related security views
- **One-Click Remediation:** Automatically fix common security issues without requiring deep security expertise
- **Network Visibility:** Built-in network scanning (inspired by 'Nmap') and traffic monitoring (inspired by 'Wireshark'). Anonymized, RAG-based analysis of device vulnerabilities and suspicious traffic sessions; ML-based traffic anomaly detection
- **Digital Identity Management:** Integrated with [Have I Been Pwned](https://haveibeenpwned.com) for online identity management with AI analysis of security impact
- **Signed Compliance Reports:** Contractors required to prove their device meets baseline security requirements (SOC 2 or ISO 27001) can generate a signed compliance report with a single click.
- **Privacy-first management:** Connects to our no-MDM platform ([edamame.tech](https://www.edamame.tech)), enabling continuous reporting of security posture and integration with access control to implement Zero Trust for code, secrets, and test data access.


<a href="https://youtu.be/AfYh3FlyryM"><img src="https://img.youtube.com/vi/AfYh3FlyryM/maxresdefault.jpg" alt="Watch the EDAMAME Security walkthrough: from first launch to a trusted machine" width="640"></a>

[EDAMAME Security walkthrough: from first launch to a trusted machine](https://youtu.be/AfYh3FlyryM) · one video per feature in the [EDAMAME Security playlist](https://www.youtube.com/playlist?list=PLacoWebxaum4)

**Documentation:** [EDAMAME Security README](https://github.com/edamametechnologies/edamame_security) | [Security Wiki](https://github.com/edamametechnologies/edamame_security/wiki)

### Security Without Undermining Productivity

- **CLI or GUI Interface:** Use the app interface or CLI commands (`edamame_posture get-score`, etc.) - they have equivalent functionality
- **Self-Directed Assessment:** Evaluate your workstation's security posture against industry standards independent of any central management
- **Local-Only Controls:** Enforce security policies without external dependencies or registration requirements
- **Developer Workflow Integration:** Add security gates to your personal CI/CD pipeline and AI agent infrastructure with exit-code-based controls

### EDAMAME Posture: Free CLI

Protect your CI/CD runners, any server running AI agents (cloud or self-hosted), and personal repositories with powerful security tools:

- **Available Tools:**
  - **CLI (EDAMAME Posture):** For Windows, macOS, or Linux ([GitHub](https://github.com/edamametechnologies/edamame_posture_cli))
  - **GitHub Action (EDAMAME Posture GitHub Action):** Seamless GitHub integration ([GitHub](https://github.com/edamametechnologies/edamame_posture_action))
  - **GitLab Action:** Integration for GitLab CI/CD workflows ([GitLab](https://gitlab.com/edamametechnologies/edamame_posture_action))

- **Installation Methods:**
  - **Linux quick install**: `curl --proto '=https' --tlsv1.2 -sSf https://raw.githubusercontent.com/edamametechnologies/edamame_posture/main/install.sh | sh`
  - Supports configuration arguments for automated setup with AI Assistant
  - Example: `| sh -s -- --user USER --domain DOMAIN --pin PIN --claude-api-key KEY --agentic-mode auto`
  - **Linux**: APT repository (Debian/Ubuntu/Raspbian), Alpine APK, or direct binary download
  - **macOS**: Homebrew (`brew install --cask edamametechnologies/tap/edamame-posture`) or direct binary download
  - **Windows**: Chocolatey (`choco install edamame-posture`) or direct binary download

#### Key Security Use Cases

1. **Runner and AI Agent Host Hardening**
  - Automatically scan for vulnerabilities and misconfigurations in your CI/CD and AI agent environments
  - Enforce minimum security scores on runners before allowing builds to proceed
  - Apply automatic remediations to fix common security issues in ephemeral environments
  - Let AI agents participate in runtime monitoring via [MCP integration](https://www.edamame.tech/agents)
  - Example: `edamame_posture check-policy 2.0 "encrypted disk disabled,critical vulnerability" "SOC 2"`

2. **Egress traffic control & anomaly detection**
  - Create whitelists based on normal build behavior to define allowed network connections
  - Detect and block suspicious outbound connections that could indicate supply chain attacks
  - Generate network audit trails for security verification and incident response
  - Example: `edamame_posture background-start-disconnected --network-scan --packet-capture --whitelist github_ubuntu`

3. **Pipeline Security Gates**
  - Fail builds when security posture doesn't meet requirements, preventing insecure code deployment
  - Verify that code commits originated from properly secured environments
  - Ensure network traffic conforms to defined whitelists during the build process
  - Example: `edamame_posture get-sessions` (returns non-zero exit code if whitelist is violated)

Example GitHub Action for your personal repository:
```yaml
- name: Setup EDAMAME Posture
  uses: edamametechnologies/edamame_posture_action@v1
  with:
    network_scan: true
    packet_capture: true
    auto_remediate: true
    edamame_minimum_score: 2.0
    custom_whitelists_path: ./.github/workflows/whitelist.json
    set_custom_whitelists: true

# Later, at workflow end:
- name: Verify network activity
  uses: edamametechnologies/edamame_posture_action@v1
  with:
    dump_sessions_log: true
    exit_on_whitelist_exceptions: true  # Fail pipeline if unauthorized network traffic is detected
```

Watch: [Gate a GitHub Actions build on its runner's posture, its egress and attacks](https://youtu.be/rwHbr6JwHp8) · [An API key for EDAMAME Posture in your CI/CD](https://youtu.be/c7XXrqBRAKE)

**Real-world scenario:** During a build, your runner makes unexpected connections to unknown IP addresses or domains. EDAMAME detects this unauthorized egress traffic, fails the pipeline, and provides detailed logs showing what connections violated your whitelist — potentially preventing a supply chain attack or data exfiltration incident.

**How EDAMAME detected CVE-2025-30066:** When the popular GitHub Action tj-actions/changed-files was compromised in March 2025, attackers modified it to leak CI/CD secrets by making unauthorized network calls to fetch a malicious payload from gist.githubusercontent.com. EDAMAME's network monitoring detected this exact attack pattern during our security testing. By capturing all packet-level traffic from the CI runner and enforcing strict network whitelists, EDAMAME immediately flagged the suspicious outbound connection that other tools missed. This Zero Trust approach to CI/CD networking effectively prevented the payload from being executed, protecting thousands of repositories from credential theft — demonstrating why comprehensive network visibility is essential for modern supply chain security.

- **Zero-Configuration Integration:** Add security gates to your personal repositories with minimal setup
- **Local Policy Enforcement:** Define and enforce security standards without requiring external registration or connectivity
- **Disconnected Network Monitoring:** Monitor and enforce network traffic whitelists in your CI/CD pipeline
- **Security Signatures:** Add cryptographically verifiable security posture signatures to your commits and releases
- **Automated Runner & Agent Hardening:** Automatically secure CI/CD runners and AI agent servers, and respond to security posture changes
- **Security Beyond Compliance:** Address network risks with automated audits and integrated network scanning

#### Securing AI Agents

AI agents like Cursor, Claude Code, Claude Desktop, OpenClaw, OpenAI Codex, and Hermes execute shell commands, access credentials, install packages, and modify system configurations autonomously. They are among the most privileged processes on your workstation or server. EDAMAME Posture provides two complementary integration paths:

**Path 1: Harden the Server Running Your Agent**

Deploy EDAMAME Posture CLI on the server or workstation hosting your AI agent—the same way you would secure a self-hosted CI/CD runner:
- Continuous posture monitoring and scoring
- Automated hardening with agentic remediation (`--agentic-mode auto`)
- L7 traffic analysis and LAN scanning
- Human-in-the-loop escalation via Slack

**Path 2: Let the Agent Watch Itself (MCP)**

Connect your AI agent to EDAMAME Posture via [Model Context Protocol (MCP)](https://github.com/edamametechnologies/edamame_core_api). The agent queries real-time security signals and cross-references its declared intent against actual system behavior:
- **Two-plane security**: Correlate what the agent says it is doing with what the machine actually does
- **Traffic divergence detection**: Flag when the agent's actual network behavior doesn't match its stated actions
- **Posture drift alerts**: Surface before/after evidence when firewall state, remote access, or endpoint protection changes unexpectedly
- **Self-monitoring**: The agent continuously validates its own environment remains secure

## For Development Teams & Enterprises

### EDAMAME Hub: Free, Business and Enterprise plans

Enhance your organization's security posture with team-focused capabilities:

- **Cross-Team Standardization:** Enforce consistent security policies across all development teams
- **Security Visibility:** Monitor security posture across your entire device fleet
- **AI Governance:** See the AI agents across the fleet and the MCP servers they reach, allow the ones you approve, and map failing AI checks to OWASP Agentic, OWASP LLM, MITRE ATLAS and ISO/IEC 42001
- **Managed Configuration:** Set the EDAMAME app and EDAMAME Posture settings for the whole team; the Hub manages EDAMAME's own settings, never the device, and each person accepts the configuration
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

**Documentation:** [EDAMAME Hub README](https://github.com/edamametechnologies/edamame_hub) | [Hub Wiki](https://github.com/edamametechnologies/edamame_hub/wiki)

<a href="https://youtu.be/-URqsN_ZFuo"><img src="https://img.youtube.com/vi/-URqsN_ZFuo/maxresdefault.jpg" alt="Watch the EDAMAME Hub walkthrough: your fleet's posture and AI agents in one place" width="640"></a>

[EDAMAME Hub walkthrough: your fleet's posture and AI agents in one place](https://youtu.be/-URqsN_ZFuo) · [AI governance](https://youtu.be/qH0jquHwPNw) · [Zero Trust conditional access](https://youtu.be/4acoytI6v-U) · [SOC 2 and ISO 27001 evidence without MDM](https://youtu.be/BxjwoYJHzlQ) · [Managed configuration](https://youtu.be/Q3_HJ36lHlQ) · [Team onboarding](https://youtu.be/OK2BmJj1m8g) · all in the [EDAMAME Hub playlist](https://www.youtube.com/playlist?list=PLFHRv2443cm4)

### Fleet Deployment Through Your MDM

Already running an MDM? Use it as the delivery channel: [auto_provisioning](https://github.com/edamametechnologies/auto_provisioning) has scripts, configuration profiles and guides (Intune, ConfigMgr, Jamf, Kandji, Mosyle, Workspace ONE, Ansible) that install EDAMAME Posture or the EDAMAME Security app with Hub enrollment and LLM settings preconfigured. The MDM only delivers and configures EDAMAME; EDAMAME itself never takes control of the device.

### User-up Security for the AI Coding Era

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

EDAMAME Core is the central engine that powers both EDAMAME Security and EDAMAME Posture. While closed source, it provides the high-performance primitives that underpin the Trust Layer:

- **Cross-platform assessment engine**: Consistent posture evaluation across macOS, Windows, and Linux
- **Threat detection & scoring**: Policy-driven findings compiled into a unified security score
- **System configuration analysis**: Deep OS checks with remediation orchestration
- **Network visibility**: LAN discovery, traffic monitoring, and session analysis
- **Intelligent advisory system**: Guided fixes with state tracking and progress monitoring
- **Privileged operations via Helper**: Secure separation for actions requiring elevated rights
- **Optimized runtime**: Async, resource-efficient implementation for desktop, CI/CD, and AI agent environments
- **Service interface**: RPC surface consumed by the app and developer CLI

See **[EDAMAME Core API](https://github.com/edamametechnologies/edamame_core_api)** for the full public API documentation covering architecture, 150+ RPC methods, event system, gRPC and MCP interfaces, feature flags, and multi-platform support.

**OEM Licensing**: EDAMAME Core is available for OEM integration into third-party products. Contact [EDAMAME Technologies](https://www.edamame.tech) for licensing inquiries.

## Agent Runtime Security

EDAMAME Security monitors AI agents **automatically**: its host-side transcript observer runs two-plane divergence detection against any supported agent the moment it is discovered on disk, with **no plugin installed**, and a compromised agent cannot pause or silence it. The named integrations below are **optional and additive**; they extend that coverage off-host (remote, SSH, container, CI, VM) and add in-agent onboarding and read-only posture and verdict views.

Watch: [Did your AI agent do what it said? Divergence](https://youtu.be/lDenRwA_8dY) · [What can your AI agents reach? Exposure](https://youtu.be/nyZ-QQLXsy8) · attacks on AI agents, replayed by the Attack Simulator and caught from outside the agent, in the [Attack Simulator playlist](https://www.youtube.com/playlist?list=PLO8OBTXPWuyc)


| Repository | Description |
|------------|-------------|
| **[Cursor integration](https://github.com/edamametechnologies/edamame_cursor)** | Optional Cursor IDE integration; install paths in the repo README. Adds off-host coverage plus in-agent posture and divergence verdicts; the host-side observer already monitors an on-disk Cursor with no plugin installed. |
| **[Claude Code integration](https://github.com/edamametechnologies/edamame_claude_code)** | Optional Claude Code integration; install paths in the repo README. Adds off-host coverage plus in-agent posture and divergence verdicts; the host-side observer already monitors an on-disk Claude Code with no plugin installed. |
| **[Claude Desktop integration](https://github.com/edamametechnologies/edamame_claude_desktop)** | Optional Claude Desktop integration (Code-in-Desktop and Cowork modes). Install via EDAMAME Security or `edamame-posture install-agent-plugin claude_desktop`. Adds off-host coverage plus in-agent posture and divergence verdicts; the host-side observer already monitors an on-disk Claude Desktop with no plugin installed. |
| **[OpenClaw integration](https://github.com/edamametechnologies/edamame_openclaw)** | Optional MCP plugin and skills for OpenClaw. See the repo README for the MCP plugin, skills and Lima VM provisioning. Adds off-host / VM coverage and in-agent posture through the OpenClaw runtime; the host-side observer already monitors on-disk OpenClaw installs with no plugin installed. |
| **[Codex integration](https://github.com/edamametechnologies/edamame_codex)** | Optional OpenAI Codex CLI integration. Install via EDAMAME Security or `edamame-posture install-agent-plugin codex`. Adds off-host coverage plus in-agent posture and divergence verdicts; the host-side observer already monitors an on-disk Codex CLI with no plugin installed. |
| **[Hermes integration](https://github.com/edamametechnologies/edamame_hermes)** | Optional Nous Research Hermes Agent integration. Install via EDAMAME Security or `edamame-posture install-agent-plugin hermes`. Adds off-host coverage (including the SQLite+FTS5 store) plus in-agent posture and divergence verdicts; the host-side observer already monitors on-disk Hermes installs with no plugin installed. |
| **[Agent Security (Research)](https://github.com/edamametechnologies/agent_security)** | Research paper and publication artifacts for *"Runtime Security for Agentic Systems: A Practical Two-Plane Approach"* (arXiv preprint, forthcoming). |

## Key Open Source Components

EDAMAME maintains several open source projects that power the platform and can be used independently:
- **Agent integrations** (Cursor, Claude Code, Claude Desktop, OpenClaw, Codex, Hermes): Optional, open source packages that extend EDAMAME's host-side observer off-host and add in-agent onboarding and read-only posture and verdict views. The observer itself monitors on-disk agents with no plugin installed. See [Agent Runtime Security](#agent-runtime-security) above for repos and install paths.
- **[Threat Models](https://github.com/edamametechnologies/threatmodels)**: Public repository of security benchmarks, policies, whitelists/blacklists, and signatures used by the platform. See **[Threat Models Wiki](https://github.com/edamametechnologies/threatmodels/wiki)**.
- **[Flodbadd](https://github.com/edamametechnologies/flodbadd)**: Network visibility engine for packet capture, session analysis, whitelists/blacklists, and on-device anomaly detection. An example tool using it is **[Flodviddar](https://github.com/edamametechnologies/flodviddar)**.
- **[Undeadlock](https://github.com/edamametechnologies/undeadlock)**: Low-overhead diagnostics for async locks and maps to surface contention/deadlocks during development.
- **[Extended Isolation Forest](https://github.com/edamametechnologies/extended-isolation-forest)**: Our fork of the **[extended-isolation-forest Rust crate](https://github.com/nmandery/extended-isolation-forest)** used for egress traffic ML anomaly detection.

Our system helper is fully open source:
- **[EDAMAME Helper](https://github.com/edamametechnologies/edamame_helper)**: Privileged companion app that safely executes checks and remediation steps requiring elevated rights.

It relies on open source libraries:
- **[EDAMAME Models](https://github.com/edamametechnologies/threatmodels-rs)**: Signature-based cloud data model manager with custom overrides and thread-safe access.
- **[EDAMAME Foundation](https://github.com/edamametechnologies/edamame_foundation)**: Core Rust library for posture assessment, threat models, secure helper IPC, scoring, and policy enforcement.

Our closed source EDAMAME Core (Rust) -- see **[EDAMAME Core API](https://github.com/edamametechnologies/edamame_core_api)** for public API documentation -- uses the following additional libraries:
- **[EDAMAME Backend](https://github.com/edamametechnologies/edamame_backend)**: Complete list of data structures used to communicate with the backend.

The CLI wrappers for edamame_core are fully open source:
- **[GitHub Action](https://github.com/edamametechnologies/edamame_posture_action)** / **[GitLab Action](https://gitlab.com/edamametechnologies/edamame_posture_action)**: CI/CD integrations to enforce posture and network controls in pipelines.
- **[EDAMAME CLI](https://github.com/edamametechnologies/edamame_cli)**: Developer-friendly interface to EDAMAME core services with interactive RPC exploration. Available via APT (Debian/Ubuntu), APK (Alpine), Homebrew (macOS), Chocolatey (Windows), or direct binary download.
- **[EDAMAME Posture](https://github.com/edamametechnologies/edamame_posture_cli)**: Cross-platform CLI to assess posture, remediate issues, enforce policies, and generate compliance reports. Available via APT (Debian/Ubuntu), APK (Alpine), Homebrew (macOS), Chocolatey (Windows), or direct binary download.
