Test Plan for EDAMAME Endpoint Security Platform

Overview: This test plan validates the EDAMAME platform end‑to‑end across:
- Workstation Protection — EDAMAME Security app (macOS, Windows).
- CI/CD Pipeline Protection — EDAMAME Posture in GitLab and GitHub.
- Administration & Zero‑Trust Access — EDAMAME Hub for policy, reporting, and conditional access integrations (GitLab IP allow lists, Netbird).

Coverage includes functional, performance, security, and usability validation. It verifies the privacy‑preserving, reporting‑only architecture (no MDM/remote device control), compliance mappings (SOC 2, ISO 27001), continuous audit‑ready posture attestations, and end‑to‑end conditional access enforcement across repos and VPN.

## References

- Leaders page: https://www.edamame.tech/leaders
- GitLab posture action: https://gitlab.com/edamametechnologies/edamame_posture_action
- Integrations documentation hub: https://github.com/edamametechnologies/integrations
- GitLab access control guide: https://github.com/edamametechnologies/integrations/wiki/Setting-Up-GitLab-for-Access-Control-Integration
- Netbird access control guide: https://github.com/edamametechnologies/integrations/wiki/Setting-Up-Netbird-for-Access-Control-Integration
 - EDAMAME GitHub organization: https://github.com/edamametechnologies/
 - EDAMAME Security app repository: https://github.com/edamametechnologies/edamame_security

## Conventions

- Numbering: Sections and tests follow hierarchical numbering (e.g., 1.1.1) for readability.
- Expected Outcome blocks state pass/fail criteria succinctly.

## Test Case Summary

| ID | Title | Area | Platforms | Criticality | Status | Link |
| --- | --- | --- | --- | --- | --- | --- |
| 1.1.1 | Installation and Onboarding (macOS) | Workstation | macOS | 3 | Pending | — |
| 1.1.2 | Installation and Onboarding (Windows) | Workstation | Windows | 3 | Pending | — |
| 1.1.3 | Security Benchmark Audit and Scoring | Workstation | macOS, Windows | 4 | Pending | — |
| 1.1.4 | One‑Click Remediation | Workstation | macOS, Windows | 5 | Pending | — |
| 1.1.5 | Network Scanning and Discovery | Workstation | macOS, Windows | 4 | Pending | — |
| 1.1.6 | Process‑Level Traffic Monitoring | Workstation | macOS, Windows | 4 | Pending | — |
| 1.1.7 | Digital Identity Breach Check | Workstation | macOS, Windows | 3 | Pending | — |
| 1.1.8 | Compliance Report Generation | Workstation | macOS, Windows | 4 | Pending | — |
| 2.1.1 | CLI Setup in GitLab CI Pipeline | CI/CD | GitLab runners | 4 | Pending | — |
| 2.1.1a | GitLab Posture Action Integration | CI/CD | GitLab runners | 4 | Pending | https://gitlab.com/edamametechnologies/edamame_posture_action |
| 2.1.1b | GitLab – Hub‑Connected Policy Enforcement | CI/CD | GitLab runners | 5 | Pending | — |
| 2.1.1c | GitLab – Local Posture Gate | CI/CD | GitLab runners | 5 | Pending | — |
| 2.1.2 | Cross‑Platform Runner Compatibility | CI/CD | Linux/Windows/macOS | 3 | Pending | — |
| 2.1.3 | Runner Hardening Policy Enforcement | CI/CD | GitLab runners | 5 | Pending | — |
| 2.1.4 | Egress Network Whitelist | CI/CD | GitLab runners | 5 | Pending | — |
| 2.2.1 | Build Time Overhead | CI/CD | GitLab/GitHub | 3 | Pending | — |
| 2.2.2 | Resource Usage on CI Runner | CI/CD | GitLab/GitHub | 3 | Pending | — |
| 2.3.1 | Detect Insecure Runner Configs | CI/CD | GitLab/GitHub | 4 | Pending | — |
| 2.3.2 | Supply Chain Attack Simulation | CI/CD | GitLab/GitHub | 5 | Pending | — |
| 2.3.3 | No Secrets Leak via EDAMAME | CI/CD | GitLab/GitHub | 5 | Pending | — |
| 2.4.1 | Ease of Integration and Docs | CI/CD | GitLab/GitHub | 3 | Pending | — |
| 2.4.2 | Developer Acceptance and Flow | CI/CD | GitLab/GitHub | 3 | Pending | — |
| 2.4.3 | Compatibility with CI Tools | CI/CD | GitLab/GitHub | 3 | Pending | — |
| 2.5.1 | GitHub – Hub‑Connected Policy Enforcement | CI/CD | GitHub Actions | 5 | Pending | https://github.com/edamametechnologies/edamame_posture_action |
| 2.5.2 | GitHub – Local Posture Gate | CI/CD | GitHub Actions | 5 | Pending | https://github.com/edamametechnologies/edamame_posture_action |
| 3.1.1 | Domain Registration & Onboarding | Hub | Web | 3 | Pending | — |
| 3.1.2 | Fleet Posture Visibility | Hub | Web | 4 | Pending | — |
| 3.1.3 | Central Policy Management | Hub | Web | 5 | Pending | — |
| 3.1.4 | Compliance Reporting & Audit | Hub | Web | 4 | Pending | — |
| 3.1.5 | Conditional Access Integration | Hub | Web | 5 | Pending | — |
| 3.1.5a | GitLab IP Allow List | Hub | Web/GitLab | 5 | Pending | https://github.com/edamametechnologies/integrations/wiki/Setting-Up-GitLab-for-Access-Control-Integration |
| 3.1.5b | Netbird Policy‑Based Access | Hub | Web/Netbird | 5 | Pending | https://github.com/edamametechnologies/integrations/wiki/Setting-Up-Netbird-for-Access-Control-Integration |
| 3.1.6 | Alerting and Notifications | Hub | Web | 4 | Pending | — |
| 3.2.1 | Dashboard Performance at Scale | Hub | Web | 3 | Pending | — |
| 3.2.2 | Integration Latency | Hub | Web | 4 | Pending | — |
| 3.2.3 | Hub Reliability & Failover | Hub | Web | 4 | Pending | — |
| 3.3.1 | Access Control and Roles | Hub | Web | 5 | Pending | — |
| 3.3.2 | Data Protection in Hub | Hub | Web | 5 | Pending | — |
| 3.3.3 | No Remote Command Execution | Hub | Web | 5 | Pending | — |
| 3.3.4 | Integration Security | Hub | Web | 5 | Pending | — |

1. Workstation Protection – EDAMAME Security App (macOS & Windows)

Objective: Ensure the EDAMAME Security desktop application installs and runs on both macOS and Windows, providing continuous endpoint posture assessment and remediation without impacting user productivity
.

1.1 Functional Tests (Workstation App)

Test Case 1.1.1: Installation and Onboarding (macOS)
Steps:

Download the EDAMAME Security app for macOS from the official EDAMAME source.

Run the installer and complete setup on a Mac workstation.

Launch the app and perform initial onboarding (e.g. granting necessary permissions such as for network monitoring).
Expected Outcome:

The app installs without errors on macOS and starts successfully.

On first run, the app prompts for any required permissions.

The user is presented with an overview of their device’s security posture after onboarding.

No system instability or crashes occur during installation or first launch.

Test Case 1.1.2: Installation and Onboarding (Windows)
Steps:

Download the EDAMAME Security app installer for Windows from the official EDAMAME source.
Download the EDAMAME Helper installer for Windows from the official EDAMAME source.
Download NPCAP installer for Windows from the official source.

Run the installers on a Windows 10/11 workstation with default settings.

Launch the EDAMAME Security app and go through any welcome/setup screens.
Expected Outcome:

The installers completes successfully on Windows, and the application launches.

All necessary components are properly installed. 

No firewall or SmartScreen blocks are encountered; if they are, the app provides clear instructions to resolve them.

The application UI appears and shows initial security posture or dashboard.

Test Case 1.1.3: Security Benchmark Audit and Scoring
Steps:

Within the EDAMAME app, initiate a full security audit/scan of the system.

Allow the app to check OS settings, configurations, and compare against known standards (e.g. CIS Benchmarks).

After scan, review the security score or compliance status provided.
Expected Outcome:

The app completes a comprehensive scan of the workstation’s security posture (OS configuration, patches, etc.) in a reasonable time.

It reports a security score or compliance summary aligned with industry standards like CIS, SOC2, ISO27001...

Any failed checks or warnings are clearly listed (e.g. “Firewall disabled” or “Disk encryption off”).

The results are consistent across platforms: the same misconfiguration yields similar warnings on both Mac and Windows (ensuring the cross-platform assessment engine provides consistent evaluations
).

Test Case 1.1.4: One-Click Remediation of Issues
Steps:

Identify a reported issue from the audit (e.g. firewall disabled...).

Use the app’s one-click fix or guided remediation feature on that issue.

Confirm any system changes (if prompted, allow the app or its helper service to apply fixes).
Expected Outcome:

The app successfully fixes common security issues automatically without requiring deep security expertise from the user.

For example, clicking “Fix” on “Firewall off” should enable the firewall.

The app provides feedback (notification or updated status) that the issue was resolved.

Re-running the security audit reflects the change (the fixed issue no longer appears, and the security score improves accordingly).

If an issue cannot be auto-fixed (requires manual steps), the assistant should explain the risk and guide the user through steps
, maintaining a user-friendly approach.

Test Case 1.1.5: Network Scanning and Device Discovery
Steps:

Connect the workstation to a local network with a few other devices.

In the EDAMAME app, initiate a network scan feature.

Wait for scan results and review the list of discovered devices and any risk analysis.
Expected Outcome:

The app discovers devices on the local network (similar to an Nmap-style scan)
. It should list IP addresses or hostnames of devices in the same subnet.

For each discovered device, it may highlight potential risks (e.g. open ports or if a device is unknown/untrusted).

The AI assistant might provide analysis of whether any detected device could pose a threat.

This operation should not disrupt network performance noticeably while scanning.

If run on both macOS and Windows, both should yield comparable scanning capability. Ensure that required permissions (like ping/ARP or packet capture privileges) are correctly handled by the app on each OS.

Test Case 1.1.6: Process-Level Traffic Monitoring
Steps:

Open a few applications on the workstation that generate network traffic (e.g. web browser streaming video, or a command-line making API calls).

Enable EDAMAME’s traffic monitoring feature for a fixed duration (if available, e.g. “Monitor network for 5 minutes”).

After monitoring, inspect the traffic report in the app.
Expected Outcome:

The EDAMAME app captures outgoing network connections and identifies processes initiating them
. For example, it should show that chrome.exe connected to certain domains on Windows, or Safari on macOS, etc.

The monitoring leverages ML-based anomaly detection to flag unusual connections
. If a process makes a connection outside normal patterns (e.g. an SSH client connecting to an unfamiliar IP), the app should flag it.

The UI presents this in an understandable way (e.g. a graph or list of processes and connections).

No significant performance degradation occurs during monitoring (the system remains usable, verifying the low-overhead capture engine
).

The user can drill down into details for suspicious traffic, guided by the AI assistant to investigate further if needed.

Test Case 1.1.7: Digital Identity Breach Check
Steps:

Configure the app with a user’s email (if not already, perhaps during onboarding it asks for an email to monitor breaches).

Trigger the identity breach or credential check feature.

Wait for the app to report if the email appears in any known breach databases.
Expected Outcome:

The app integrates with HaveIBeenPwned (or a similar service) and informs the user whether their email or credentials have been part of known data breaches
.

If a breach is found, the AI assistant provides guidance, e.g. “Your email was found in a breach of XYZ site in 2023; consider changing your password”
.

If no breach is found, it confirms that the identity appears secure.

The feature should work on both OS platforms similarly, requiring internet access to fetch breach data.

Test Case 1.1.8: Compliance Report Generation
Steps:

After remediating issues, use the EDAMAME app’s option to generate a compliance report (e.g. for SOC2 or ISO27001).

Save or view the generated report.
Expected Outcome:

The app produces a tamper-proof compliance report that summarizes the device’s security posture
. It should indicate compliance with chosen standards (e.g. “ISO27001 compliance: PASSED” or list any remaining gaps).

The report is digitally signed or has a verification mechanism to prove its authenticity (per EDAMAME’s posture signature capabilities
).

The content includes key security settings/status (disk encryption, OS version, AV status, etc.) required by standards.

This is completed with a single click from the user’s perspective
, demonstrating ease of use for, say, a contractor proving their laptop meets client security requirements.

Verify that the report does not expose sensitive personal data – it should focus on security configuration and compliance metrics (aligning with EDAMAME’s privacy-first approach).

1.2 Performance Tests (Workstation App)

Test Case 1.2.1: Resource Utilization During Scans
Steps:

Monitor system CPU and memory usage while EDAMAME Security performs a full system audit (as in test 1.1.3).

Measure the time taken for the scan to complete on typical hardware.
Expected Outcome:

The scanning process is efficient, leveraging EDAMAME’s optimized core (Rust-based engine) for asynchronous, resource-efficient operation
. CPU usage should remain moderate (e.g. spikes during intense checks but not maxed out for long durations) and memory footprint should be reasonable for an endpoint security tool.

The full audit completes in a timely manner (e.g. a couple of minutes for an average system).

The app’s presence (when idle, not actively scanning) should have minimal impact on system performance (no noticeable slowdown in developer workflows, verifying the “lightweight agent” claim
).

On both Mac and Windows, performance should be comparable; no obvious inefficiencies on one platform versus the other.

Test Case 1.2.2: Continuous Monitoring Overhead
Steps:

Leave the EDAMAME app running in the background for an extended period (e.g. a full workday).

Simulate normal developer activities (code editing, building, web browsing).

Observe system performance and any EDAMAME-triggered notifications or scans during that period.
Expected Outcome:

The app’s background posture checks or network monitoring cause no significant latency or interference with user activities (aligns with the promise of no compromise on productivity
).

If the app performs periodic re-scans or real-time protection, these should be almost unnoticeable to the user (e.g. running at low priority).

Memory usage should remain stable over time (no sustained memory leak).

Any scheduled tasks (like a daily compliance check or update) should be quick and possibly deferred when system is idle to avoid interrupting work.

1.3 Security Tests (Workstation App)

Test Case 1.3.1: Detection of Non-Compliance and Vulnerabilities
Steps:

Intentionally introduce known security weaknesses on a test machine (e.g., install an outdated browser with known vulnerabilities, disable antivirus, or leave SSH service running with default config).

Run EDAMAME Security’s audit.
Expected Outcome:

The app should flag known vulnerabilities or misconfigurations. For instance, it might warn about an outdated software version or a critical vulnerability in the OS environment
 (though that example was CI-focused, the underlying engine should similarly identify local vuln/misconfig).

For each issue, the app’s AI explanation should clearly describe the risk (e.g. “Outdated Chrome browser – contains known CVEs that could be exploited”).

EDAMAME’s threat detection scoring system should reflect these issues in a lower security score
.

If automatic remediation is possible (e.g. turning on a disabled security setting), the app offers it; if not (e.g. updating third-party software), it advises the user on steps.

Test Case 1.3.2: Privacy and Data Security
Steps:

Use network analysis tools to monitor what data EDAMAME Security transmits from the workstation while performing scans or reporting to the Hub (if connected).

Also inspect logs or settings for any data collection preferences.
Expected Outcome:

EDAMAME should uphold a privacy-first design, meaning it does not transmit sensitive personal files or allow remote control of the device
.

Data sent to EDAMAME Hub (if logged in) should be limited to posture metrics, compliance results, and necessary identifiers – no raw personal data or code is uploaded.

If the app is used standalone (not connected to Hub), it should not require cloud connectivity for core features (per local-only controls design
).

The “reporting-only” architecture is verified: for example, an admin on the EDAMAME Hub cannot remotely execute actions on the device, only view its posture
. Attempting any remote action (if such a feature is absent by design) should not be possible.

All communications should be encrypted (HTTPS or other secure channels) when the app contacts EDAMAME services (Hub or update servers).

Test Case 1.3.3: Endpoint Conditional Access Signals
Steps:

(If EDAMAME Hub integration is enabled) Mark the test workstation as “untrusted” by creating a policy in Hub that this device is non-compliant (e.g. by failing a check).

Attempt to access a protected resource from this workstation (for example, a code repository or VPN that is configured to use EDAMAME’s posture signals via Zero Trust integration).
Expected Outcome:

Because the device does not meet security posture requirements, access to the protected resource should be denied, demonstrating EDAMAME’s conditional access control working in practice
.

For instance, if integrated with GitHub or Netbird VPN as described, the attempt should be blocked until the device posture is corrected
.

The EDAMAME app should perhaps notify the user that their device is out of compliance for that resource (“Access to GitLab denied: endpoint security requirements not met”).

Once the user fixes the compliance issues and the app reports an improved posture, access should be restored, confirming dynamic posture-based access enforcement.

This test validates the Zero Trust integration pipeline end-to-end with the workstation agent.

1.4 Usability Tests (Workstation App)

Test Case 1.4.1: User Interface Clarity and Guidance
Steps:

Navigate through the EDAMAME app’s interface on both Mac and Windows. Visit sections like Dashboard, Scan Results, Network Monitor, Settings.

For each security finding or feature, note if guidance/tooltips are provided.
Expected Outcome:

The UI should be clean and developer-friendly, aligning with the developer-first design. Warnings and recommendations are explained in plain language by the AI assistant
.

No excessive technical jargon without explanation – e.g. if a CIS control is failing, it should describe it (like “Firewall disabled – this fails CIS Benchmark XYZ, which could expose your device to network threats”).

The navigation is intuitive: a developer can find the necessary info (compliance score, issue list, fix buttons) quickly.

Dark mode or customization (if offered) works correctly – not required by spec, but common for dev tools.

The app does not nag or annoy the user; notifications are meaningful and not too frequent, respecting the developer’s workflow (no “agent fatigue” as criticized in traditional MDMs
).

Test Case 1.4.2: Cross-Platform UX Consistency
Steps:

Use the EDAMAME app on macOS and on Windows side by side for similar tasks (running a scan, viewing a report, fixing an issue).

Compare the layout and feature availability.
Expected Outcome:

Both versions offer the same core features and a consistent user experience. Labels and menus might adapt to OS conventions (e.g. Windows might have a system tray icon, macOS a menu bar item), but overall workflow is the same.

Any differences (due to OS-specific capabilities) are minimal and well-justified. For instance, if the Mac app has an extra check for System Integrity Protection that Windows doesn’t need, it’s clearly noted.

The documentation or in-app hints for each platform cover those differences so the user is not confused.

The EDAMAME Helper’s presence on Mac/Windows is mostly invisible to the user except when elevation is needed (then a standard OS prompt appears asking to allow changes).

Test Case 1.4.3: Self-Service and Autonomy
Steps:

Attempt common tasks without admin intervention: e.g. developer installs the app on their own, fixes issues, and generates a report for their manager.

Gauge if any point requires contacting IT or reading heavy documentation.
Expected Outcome:

A developer (even a contractor or freelancer) can use EDAMAME Security independently to meet security requirements
.

The self-service onboarding is straightforward; ideally, the app or the Hub provides a quickstart such that within 5–10 minutes, the user’s device is under monitoring
.

No need for the user to have special privileges beyond their normal workstation admin rights to set it up.

The process to link the device to an organization’s EDAMAME Hub (if applicable) is clearly guided in-app (e.g. entering an invite code or logging in to the Hub through the app).

2. CI/CD Pipeline Protection – EDAMAME Posture CLI (GitLab CI)

Objective: Validate that the EDAMAME Posture CLI can be integrated into CI pipelines (with focus on GitLab CI) to enforce security posture checks on CI/CD runners, without causing significant build delays or complexity
. Ensure it can detect insecure runner configurations, monitor network traffic during builds, and fail pipelines when policies are violated
.

2.1 Functional Tests (CI/CD CLI)

Test Case 2.1.1: CLI Setup in GitLab CI Pipeline
Steps:

Add EDAMAME Posture to a GitLab CI pipeline. For example, in a .gitlab-ci.yml, include a job that downloads the EDAMAME CLI (or use the provided GitLab CI template/integration
).

Use a simple pipeline that runs edamame_posture commands (such as a posture check) on a Linux runner.

Trigger the pipeline run.
Expected Outcome:

The EDAMAME CLI can be fetched or installed easily in the GitLab CI environment. This could be via a one-liner (e.g. curl and run script) or using the official EDAMAME GitLab Action
 – test both methods if possible.

The CLI executes on the runner (Linux by default). It should run without errors, outputting the security posture results of that runner. For instance, it might print a security score or list of checks performed on the CI runner environment.

The integration does not require excessive configuration – minimal setup yields a working posture scan, supporting the claim of zero-configuration integration for security gates
.

Pipeline log shows EDAMAME’s output clearly (e.g. “All checks passed. Score 2.5/3.0” or “Non-compliance: Disk not encrypted”).

Test Case 2.1.1a: GitLab Posture Action Integration (edamame_posture_action)
Steps:

Include the official EDAMAME GitLab posture action in a test project’s .gitlab-ci.yml using the published template or include mechanism described in the project
https://gitlab.com/edamametechnologies/edamame_posture_action
.

Configure a job (e.g., security_posture) that runs early in the pipeline to verify runner security posture, optionally enabling network monitoring according to the action’s README.

Run the pipeline on a representative Linux runner.
Expected Outcome:

The posture action installs and runs with minimal configuration and surfaces a clear pass/fail in job logs.

When policy thresholds are set (minimum score or no critical findings), a non-compliant runner causes the job to fail with an actionable message.

Action outputs (artifacts or console logs) are concise and suitable for gating subsequent stages.

Test Case 2.1.1b: GitLab – Hub‑Connected Policy Enforcement
Steps:

Run EDAMAME Posture in connected mode by passing Hub credentials via CI variables and requiring compliance against an org policy. Use the posture action or CLI wrapper.

Expected Outcome:

The job connects to the Hub, enforces the specified policy, and fails when the runner is not compliant with the org baseline.

Test Case 2.1.1c: GitLab – Local Posture Gate
Steps:

Run EDAMAME Posture without Hub credentials to validate local-only checks and optional network monitoring; enforce a minimum score.

Expected Outcome:

The job runs without Hub connectivity, evaluates local posture, and gates the pipeline based on minimum score or findings.

Test Case 2.1.2: Cross-Platform Runner Compatibility
Steps:

Repeat a simple EDAMAME posture check job on different GitLab runners: one Linux, one Windows, one macOS (if runners for all are available).

Use the same configuration/command for each and compare outcomes.
Expected Outcome:

The CLI supports all major OS in CI. On each runner, it should execute appropriately: e.g. on Windows runner, possibly as a PowerShell step calling the .exe or binary; on macOS, via shell.

All runs complete successfully, demonstrating the CLI’s cross-platform design
.

The results are consistent in format. If the different OS runners have different posture issues (likely, since each OS has unique configs), EDAMAME CLI should surface those. For example, it might flag if the Windows runner’s RDP is enabled or Linux runner’s firewall is off, etc.

Any OS-specific edge cases (like requiring Administrator on Windows runner for certain checks) are handled gracefully or documented. The pipeline should not hang or fail due to OS differences.

Test Case 2.1.3: Runner Hardening Policy Enforcement
Steps:

Define a minimum security policy for the CI runner using EDAMAME CLI options (e.g. require a minimum security score of 2.0 and no critical findings).

Configure the pipeline to run this policy check at the start of build jobs.
Make sure auto-remediation is configured (auto_remediate: true in a GitHub/GitLab Action as example
), verify that it logs what it fixed and proceeds or rechecks.

Run the pipeline on a runner that is intentionally misconfigured.
Expected Outcome:

The EDAMAME CLI harden the runner, fixing misconfigured elements. The pipeline passes the policy checks.
The pipeline continues normally. This ensures that builds only proceed on secure, compliant runners
 – verifying the gating functionality.

Test Case 2.1.4: Egress Network Traffic Whitelist
Steps:

Create a network whitelist JSON defining allowed domains/IPs for build processes (for example, only the package repository and known APIs).

Configure EDAMAME CLI in the pipeline to monitor network traffic during the build and enforce this whitelist (e.g. using edamame_posture background-start … and a whitelist file, or the action parameters whitelist_conformance: true with a provided whitelist
).

In the build, include a step that deliberately tries to reach an unauthorized endpoint (simulate a malicious or unexpected connection). For instance, curl http://malicious.example.com from the build script.
Expected Outcome:

EDAMAME’s CLI should detect the unauthorized network egress attempt and flag it, causing the pipeline to fail
.

The pipeline logs should include details of the violation, such as the destination that was not whitelisted, demonstrating EDAMAME’s network audit trail capability
. E.g., NonConforming connection to malicious.example.com”

This test confirms EDAMAME’s anomaly detection for supply chain attacks.

Allowed connections (e.g. fetching dependencies from known hosts) should pass normally, so that builds aren’t broken by legitimate traffic – EDAMAME should only flag the out-of-policy traffic.

2.2 Performance Tests (CI/CD CLI)

Test Case 2.2.1: Build Time Overhead
Steps:

Measure the duration of a standard CI pipeline without EDAMAME in it (baseline).

Then measure the same pipeline with EDAMAME posture checks enabled (as in tests above).

Compare the timings for the security check steps and overall pipeline.
Expected Outcome:

The EDAMAME posture check step runs very quickly, on the order of a small number of minutes at most. It should “run as swiftly as your tests”, not significantly lengthening CI time
.

There is no need for booting special VMs or containers for these checks (it runs in the existing runner context), which saves time
.

The overall pipeline with EDAMAME should remain within acceptable duration for CI; any added time is justified by security, and ideally parallelizable or optimized.

If the pipeline is configured to auto-remediate issues, check that such remediation (if any occurred) didn’t add excessive delays. For example, installing a missing update could add time, but that should be a one-time cost and logged.

Confirm that even under heavy load (multiple concurrent pipelines), the EDAMAME checks don’t create bottlenecks (each runner handles its own posture check without needing a slow centralized query).

Test Case 2.2.2: Resource Usage on CI Runner
Steps:

During a pipeline run with EDAMAME, monitor the CI runner’s CPU/memory (this might involve accessing runner metrics or logging resource usage in the job).

Particularly observe the period when EDAMAME CLI is performing a scan or monitoring traffic.
Expected Outcome:

EDAMAME’s CLI is designed for CI/CD efficiency, so it should consume limited resources. CPU may spike briefly for scans, but it should not exceed a reasonable fraction (e.g. one core for a short time). Memory usage should be modest (the EDAMAME core is optimized and asynchronous
).

The runner should not time out or slow to a crawl due to the security checks. If our pipeline includes heavy tasks, ensure those still get enough CPU – EDAMAME should yield appropriately once its tasks are done.

If multiple jobs on the same runner use EDAMAME concurrently, verify that there’s no conflict (the tool likely runs in isolated processes per job; ensure no port or file conflicts).

The network monitoring component should not significantly throttle network speeds; it’s mostly observing packets (if using eBPF/pCap, it should be efficient
).

2.3 Security Tests (CI/CD CLI)

Test Case 2.3.1: Detection of Insecure Runner Configurations
Steps:

Prepare a CI runner with several security issues: e.g., an outdated OS image, missing critical patches, unnecessary services running, etc. (If using a Docker executor, use an image intentionally configured poorly.)

Run EDAMAME posture scan on this runner at pipeline start.
Expected Outcome:

EDAMAME should identify the misconfigurations on the runner, similar to how it would on a dev machine.

It should assign a lower security score to such a runner and ideally prevent the pipeline from proceeding if those are out of policy
. This test doubles down on the runner hardening scenario by enumerating real issues.

Ensure it catches a variety of issues.

Test Case 2.3.2: Supply Chain Attack Simulation
Steps:

Simulate a scenario similar to the one described by EDAMAME (the compromised GitHub Action case
) in a controlled manner. For instance, include in the pipeline a step that tries to fetch a script from an external gist or site unexpectedly (mimicking malicious behavior).

Ensure EDAMAME’s network monitoring is active during this.
Expected Outcome:

EDAMAME should detect this abnormal egress call. If the whitelist is configured, it will flag it as in test 2.1.4. If not explicitly whitelisted, EDAMAME’s anomaly detection should still flag it as unusual (a build rarely needs to fetch from that domain).

The pipeline fails or at least logs a high-severity warning, preventing the malicious step from causing harm. This shows EDAMAME provides zero-trust networking in CI/CD – nothing goes out unless allowed
.

Check that EDAMAME logs the context: which process or command triggered the connection, and to where, so developers can investigate. This information is crucial for incident response (and EDAMAME advertises detailed logs for such events
).

Test Case 2.3.3: No Secrets Leak via EDAMAME
Steps:

Examine the pipeline environment and outputs to ensure EDAMAME does not inadvertently log sensitive information (like secret env vars).

Run pipelines with EDAMAME in both verbose and normal modes to see what is logged.
Expected Outcome:

EDAMAME CLI should be careful about not exposing secrets. For instance, if it monitors environment variables or network payloads for scanning, it should not print them out in logs.

The posture report might include filenames or config names but not actual secret values.

Any data sent to EDAMAME Hub from the pipeline (if using an enterprise setup) should be posture metadata, not code or secrets. This aligns with EDAMAME’s focus on posture and compliance rather than content.

Essentially, using EDAMAME in CI should not introduce new security risks; verify this by reviewing all outputs and transmissions.

2.4 Usability Tests (CI/CD CLI)

Test Case 2.4.1: Ease of Integration and Documentation
Steps:

Follow EDAMAME’s official guide or README for adding the CLI to GitLab (and possibly GitHub for comparison).

Note any difficulties in understanding or implementing the instructions.
Expected Outcome:

The documentation (e.g. the README in edamame_posture_cli repo or the website’s CI/CD section) provides clear instructions. For GitLab, perhaps a snippet or a reference to the GitLab Action is given
.

Our integration steps should match the guide, and any parameters (like edamame_minimum_score, network_scan: true) are explained in the docs.

If we had to guess or troubleshoot, that indicates documentation could be improved. Ideally, no trial-and-error is needed beyond copying recommended configs – fulfilling “security shouldn’t be harder than lints” mantra
.

The CLI outputs should be developer-friendly. If a posture check fails, the message should clearly state why, not just “exit code 1”. For instance, “Security posture failed: Unencrypted disk” should be visible to help devs quickly address the issue.

Test Case 2.4.2: Developer Acceptance and Pipeline Flow
Steps:

Conduct a run where the EDAMAME check passes and the pipeline succeeds normally.

Then conduct a run where EDAMAME fails the pipeline (e.g., due to an issue).

Gather feedback from a developer’s perspective: how do these outcomes feel within the development workflow?
Expected Outcome:

When EDAMAME passes, it should feel like a normal pipeline run – maybe just an extra line or two of logging, but no friction (it truly behaves like just another lint/test step). This confirms no productivity trade-offs as claimed
.

When EDAMAME fails the pipeline, the reason is clearly communicated so the developer isn’t frustrated by a mysterious failure. They should be able to find the cause (via log or EDAMAME report) and know how to fix it (perhaps by running EDAMAME Security on their dev machine to see what’s wrong).

The team’s adoption of EDAMAME in CI should be smooth: if someone accidentally misconfigures it (e.g. wrong CLI path), the errors are clear to debug.

Also, verify that disabling or bypassing EDAMAME for a specific pipeline (if needed in emergencies) is possible and documented, to not block deployments – and that this requires conscious action (so devs can’t easily ignore it without approval).

Test Case 2.4.3: Compatibility with Existing CI Tools
Steps:

Use EDAMAME CLI in a pipeline that also has other common CI tools (linters, test frameworks, maybe another security scanner) to see if there is any conflict.

Run the full pipeline with all tools.
Expected Outcome:

EDAMAME should play nicely with other tools; since it’s just a CLI step, it should not interfere with, say, code analysis tools or container scanning that might also be present.

It does not open ports or start services that persist beyond its own execution, so no leftover processes.

If using Docker-in-Docker or similar, EDAMAME’s network monitoring should still work (if not, note if documentation suggests limitations).

The addition of EDAMAME doesn’t require re-architecting the pipeline – it’s an unobtrusive addition that complements existing DevSecOps tools
.

2.5 GitHub Actions – EDAMAME Posture

Test Case 2.5.1: GitHub – Hub‑Connected Policy Enforcement
Steps:

Use the official EDAMAME GitHub Action to start the posture process connected to Hub and enforce a policy.

Expected Outcome:

Workflow connects to Hub, enforces the org policy, and fails on non-compliance with a clear message.

Test Case 2.5.2: GitHub – Local Posture Gate
Steps:

Run in disconnected mode with local policy checks and network scanning; enforce minimum score and optional whitelist conformance.

Expected Outcome:

Workflow runs without Hub connectivity, monitors egress, enforces minimum score, and fails on whitelist exceptions if configured.

3. Administration & Monitoring – EDAMAME Hub Dashboard

Objective: Verify that the EDAMAME Hub SaaS platform allows security administrators and team leads to gain visibility into all enrolled devices and CI pipelines, enforce policies centrally, and integrate with identity or access management systems. Ensure administrative features work without invading endpoint privacy, in line with “user-up security” principles
.

3.1 Functional Tests (Hub & Admin)

Test Case 3.1.1: Domain Registration and Team Onboarding
Steps:

Sign up for EDAMAME Hub (use the free plan or a test enterprise domain)
.

Create an organization domain (e.g. example.edamame.tech) and verify ownership if required (could involve an email verification or DNS record in a real scenario).

Add users to the domain: invite a few test users (developers) via the Hub’s onboarding interface.
Expected Outcome:

The Hub account is created successfully and a new domain is set up within minutes, confirming the self-service portal capability
.

Domain verification steps (if any) are clear and easy.

Invited users receive emails or links to connect their EDAMAME Security app to the Hub. As an admin, we can see pending invitations and their status.

Once a user installs EDAMAME Security and signs in to link to the domain, their device appears on the Hub dashboard. The device entry shows at least the device name, OS, and initial security posture (score or compliance status).

No admin privileges on the user’s machine were needed beyond the user running the app and accepting the invite – reflecting that even contractors can onboard easily without IT support.

Test Case 3.1.2: Fleet Posture Visibility
Steps:

On the Hub dashboard, view the list of all enrolled endpoints (developer laptops, etc.) and CI/CD nodes (if any reporting in).

Drill down into a single device’s details.
Expected Outcome:

The Hub provides a fleet-wide view of security posture
: a summary might show how many devices are compliant vs non-compliant, average security scores, etc.

Each device entry can be opened to see detailed posture findings reported by the EDAMAME app on that device. For example, admin can see if John’s Mac is missing a patch or if a CI runner failed a check – but without remote control of those devices
.

The data is updated continuously or at least regularly (e.g. if a user fixes an issue and their app sends an updated status, the Hub reflects this). This shows continuous compliance tracking
.

Sensitive personal data is abstracted – e.g., the admin might see “Personal device of Alice – Compliant” but not be able to dig into personal files. The information provided is strictly security posture and compliance-related, aligning with No Admin Abuse (reporting-only data)
.

Test Case 3.1.3: Central Policy Definition and Deployment
Steps:

In the Hub, navigate to the policy management section.

Create a security policy for the organization (for instance: “All devices must have disk encryption enabled and pass SOC2 baseline checks”). There may be preset standards (CIS, SOC2, etc.) or custom rules to configure.

Save and apply this policy to all devices/domain.
Expected Outcome:

The Hub allows definition of organization-wide policies – e.g., select from templates like SOC2 or define custom rules. This matches the Centralized Policy Management feature
.

Once applied, all enrolled endpoints and pipelines automatically inherit this policy. The Hub might push a notification to devices or mark those devices as non-compliant if they currently violate the new policy.

For example, if the policy requires disk encryption and some devices don’t have it, those devices should now show a non-compliant status in the dashboard.

On the user side, the EDAMAME app could inform them of the new requirement (if the design allows user visibility). Regardless, the admin can see which devices are out of policy instantly.

The process of distributing the policy is seamless – no manual reconfiguration on each device, proving the value of a central Hub.

Test Case 3.1.4: Compliance Reporting and Audit Trails
Steps:

Use the Hub’s reporting feature to generate an aggregated compliance report covering all devices and pipelines in the domain for a given period.

Also, access the audit logs/trails of posture changes (e.g. when a device went from non-compliant to compliant after an update).
Expected Outcome:

The aggregated report compiles data across the fleet, useful for auditors. It should show overall compliance percentage, and possibly list devices that are exceptions. This aligns with Policy Compliance Reporting for auditors
.

The audit trail feature logs events like “Device X enabled firewall at 10:30, moving into compliance” or “Policy updated by Admin Y on date Z” – giving traceability
.

Historical posture of a given device can be viewed (to verify, for example, that code was committed from a compliant device last week – Historical Verification
).

Ensure these logs include CI pipelines as well.

Test Case 3.1.5: Conditional Access Integration (IdP/Repo/VPN)
Steps:

In the Hub or Integrations section, configure an integration with an Identity Provider (e.g. Azure AD Entra ID Conditional Access or Google Context-Aware Access) or directly with a resource like GitHub/GitLab.

Set a rule such that only devices in Compliant state in EDAMAME can access a particular application (like a Git repository or a VPN resource).

From a test device, attempt access to that application both when the device is compliant and when it’s non-compliant (simulate by toggling a security setting off to break compliance).
Expected Outcome:

EDAMAME Hub should be able to send posture signals to the IdP or resource in real-time (compatible via REST/GraphQL APIs as needed
).

When the device is compliant, the IdP allows login/access normally. When non-compliant, the IdP denies access with a message (if configured, e.g. “Access denied: device does not meet security requirements”).

For example, if integrated with GitHub: pushing code or accessing a private repo from an insecure device should be flagged
. Our test device, when flagged non-compliant, might receive an HTTP 403 or see a portal message indicating posture requirements.

If integrated with a VPN (Netbird): the device should be unable to connect to certain network segments until it complies
.

The Hub’s integration engine should allow fairly easy setup for these rules (mappings of EDAMAME posture status to IdP claims or similar). No heavy custom coding should be required, confirming the “versatile access control integration” claim
.

Verify that turning the device back to compliant (e.g., re-enabling that security setting and rescanning) triggers an update and subsequently access is restored, ideally in near-real-time.

Test Case 3.1.5a: GitLab Conditional Access via IP Allow List
Steps:

Follow the GitLab access control guide
https://github.com/edamametechnologies/integrations/wiki/Setting-Up-GitLab-for-Access-Control-Integration
 to connect your GitLab group to EDAMAME Hub and enable IP allow list management from the Hub’s policies.

Create a Hub policy that restricts repository access to devices marked Compliant and to IPs published by the Hub.

From a compliant device running EDAMAME Security, attempt to clone/pull from GitLab; then repeat from a deliberately non-compliant device.
Expected Outcome:

When compliant, access succeeds from IPs published by the Hub; when non-compliant, access is denied (GitLab enforces allow list/policy) until posture is corrected.

Hub audit logs reflect policy evaluation events; GitLab settings reflect updated IP ranges as documented in the guide.

Test Case 3.1.5b: Netbird Integration — Policy-Based Access Control
Steps:

Follow the Netbird setup guide
https://github.com/edamametechnologies/integrations/wiki/Setting-Up-Netbird-for-Access-Control-Integration
 to create a dedicated group (e.g., "edamame-secure") and API token.

In EDAMAME Hub, add a Netbird integration with the token, then define a policy that grants network access only to Compliant devices. Link that policy to the Netbird conditional access.

Enroll two test devices in Netbird: one compliant (meets EDAMAME posture) and one non-compliant (violate a required control).

Attempt to reach a protected subnet/resource over Netbird from both devices.
Expected Outcome:

Compliant device can reach the protected resource; non-compliant device is blocked or routed away per policy.

Hub shows near-real-time posture changes and corresponding Netbird group/route updates; reversing the non-compliance restores access promptly.

Test Case 3.1.6: Alerting and Notifications
Steps:

Intentionally cause a security incident or policy violation (e.g., a device becomes non-compliant or a pipeline fails due to security) in the EDAMAME environment.

Check if the Hub sends out alerts/notifications to admins or relevant users.
Expected Outcome:

The Hub should provide timely alerts for critical events. For example, if a device falls out of compliance, the admin might receive an email or see a dashboard alert. If a pipeline is blocked due to a security issue, perhaps both the developer and admin are notified.

The content of notifications should be actionable (“Device X has disabled antivirus, please remediate or revoke access”) and not overly noisy for minor issues.

If multiple integrations exist, verify where the alert shows up (e.g., integrated SIEM or chatops channel if set). EDAMAME may allow webhook or API access to feed alerts into other systems – if so, test that those hooks send the expected data.

Ensure that acknowledging or resolving an alert in the Hub is possible (mark as resolved once handled), to keep the admin workflow clear.

3.2 Performance Tests (Hub & Admin)

Test Case 3.2.1: Dashboard Performance with Scale
Steps:

Simulate having a large number of devices (if possible, by onboarding many dummy devices or using a demo environment that mimics scale).

Load the dashboard and various pages (devices list, reports) and measure load times.
Expected Outcome:

The Hub should handle dozens or hundreds of devices without slowdowns. Page load times should remain within a few seconds for listing, filtering, or searching devices.

Graphs or charts (if any showing posture trends) should render correctly even with large data sets.

Backend processing (like generating the compliance report across 100+ devices) should still complete reasonably (perhaps with an asynchronous job but notified when ready).

No timeouts or browser hangs should occur at realistic scales for small to mid-size companies (for enterprise scale, if we cannot test thousands, ensure at least the design claims to support it – likely yes, since they target enterprise usage).

Test Case 3.2.2: Integration Latency
Steps:

Measure the time between a device’s posture change and that change reflecting in an integrated system. For example, how quickly after a device becomes non-compliant does the IdP get updated to block access.

Also measure the latency for Hub UI to reflect device status changes (from the moment device fixes an issue to the dashboard updating).
Expected Outcome:

Posture changes are propagated quickly, ideally in real-time or near-real-time. If a developer fixes something and their app reports in, the Hub should update within seconds.

Conditional access integrations likely rely on short polling or callbacks; it should be quick enough that there isn’t a large window where a non-compliant device still has access. (E.g., < minute).

The Hub’s design likely uses cryptographic attestations and continuous reporting
, so this test ensures that continuous flow is indeed happening without undue delay.

If the system employs any caching, ensure that compliance revocation isn’t delayed (security-critical). For example, a device falling out of compliance might immediately trigger a token revocation or similar.

3.3 Security Tests (Hub & Admin)

Test Case 3.3.1: Access Control and Roles
Steps:

Create multiple user roles in the EDAMAME Hub (if supported): e.g. an org admin, a team manager, a read-only auditor.

Verify each role’s access: for instance, an auditor might view reports but not change policies; a team manager sees only their team’s devices.
Expected Outcome:

The Hub should enforce role-based access control (RBAC) so that sensitive actions (like changing policies or removing devices) are restricted to authorized admins.

Lower-privileged users cannot access or alter data outside their scope. For example, a developer user might only see their own device’s status on the Hub (if at all) but not others’.

Attempting an unauthorized action (say, a read-only user trying to toggle a policy) should be blocked and possibly logged.

This ensures the Hub itself doesn’t become a security weakness – only trusted admins can make high-impact changes.

Test Case 3.3.2: Data Protection in Hub
Steps:

Inspect how data is stored or transmitted in the Hub (this might involve using the browser dev tools to see network calls, ensuring they are HTTPS, etc.).

If possible, review the Hub’s privacy settings or policies for data retention.
Expected Outcome:

All communications between the EDAMAME agents/CLI and the Hub are encrypted (HTTPS API calls). No sensitive data (like plaintext credentials or secrets) is visible in transit or in the browser.

The Hub likely stores device posture data in a cloud database. Verify that sensitive fields (if any) are not present in the client side; the browser should not receive anything beyond needed info for display.

Check if the Hub UI provides options to delete device data or if devices can be offboarded (important for GDPR or when a contractor leaves). The admin should be able to remove a device and its data if needed.

Also, if available, test two-factor authentication for Hub admin login (security of the admin account). EDAMAME Hub should integrate with SSO or at least offer 2FA to protect the portal.

Finally, confirm that EDAMAME Hub’s own security posture is maintained (this may be out-of-scope to test ourselves, but any visible indicators like certificates, CSP in the web app, etc., should be noted).

Test Case 3.3.3: No Remote Command Execution
Steps:

As an admin, search the Hub for any feature that allows sending a command or controlling a device (for instance, some MDMs allow wiping a device or installing software remotely).

If any such feature exists, attempt to use it on a test device. If not, note that.
Expected Outcome:

EDAMAME’s philosophy is “reporting-only” with zero remote control
, so the Hub should not offer any remote execution capabilities on endpoints.

In our test, we should find that the Hub allows viewing and policy setting, but not actions like “lock device” or “run script on device.” There might be an option to request the device to rescan or sync, which is benign.

This is actually a positive security feature (reduces risk of abuse). If we do not find any remote control, it matches expectations. If any remote action exists (perhaps something like sending a notification to the user device), ensure it’s limited and cannot be misused (and requires user consent if applicable).

By confirming no unauthorized remote control, we verify EDAMAME’s suitability for scenarios with contractors and BYOD, where overreach is a concern
.

Test Case 3.3.4: Integration Security
Steps:

Examine the tokens/credentials used for any configured integrations (IdPs, etc.) in the Hub settings.

Ensure that adding an integration does not expose credentials to unauthorized parties.
Expected Outcome:

The Hub likely requires API keys or OAuth tokens to integrate with systems like GitHub or Netbird. These should be stored securely. We should not be able to retrieve the full token via the UI after it’s entered (it might be partially masked, indicating it’s encrypted at rest).

If the Hub uses webhooks or endpoints, verify they are protected (e.g., have secret tokens in the URL or signature verification).

No integration should weaken the security posture; e.g., granting EDAMAME integration rights on GitHub should be scoped to what’s needed (checking device claims) and not full repo access beyond necessity.

If multiple integrations are set, ensure isolation (a compromise in one integration’s credentials shouldn’t affect others; but this is more of design – at least check UI separation and any cross-integration references).

3.4 Usability Tests (Hub & Admin)

Test Case 3.4.1: Admin Dashboard Usability
Steps:

As a security admin user, navigate through the EDAMAME Hub’s main sections: Overview, Devices, Policies, Integrations, Reports, etc.

Assess whether the layout and information presented meet the needs of quickly understanding security posture.
Expected Outcome:

The Overview page (if present) should give a succinct summary (e.g., “X% devices compliant, Y issues open, Z recent alerts”). This helps an admin grasp the situation at a glance.

The UI should be uncluttered and use visual cues (green/yellow/red status) for device compliance, reflecting EDAMAME’s goal to empower without overwhelming.

Navigating to detailed views is straightforward (e.g., clicking a device name opens its profile). There should be filtering options (by team, by compliance state) to find information quickly in larger environments.

The wording in the admin UI is clear – e.g., it might avoid overly technical language so that even a less technical manager could understand (“Disk Encryption Off on Alice’s Laptop” is clear, vs. “FileVault status = false”).

No significant bugs like misaligned elements or broken links in the interface.

Test Case 3.4.2: Policy Management UX
Steps:

Use the policy editor UI to change a policy (for instance, add a requirement or toggle a setting).

Save and then perhaps revert a change.
Expected Outcome:

It should be easy to adjust policies via the Hub. If they allow using a query or DSL (Domain Specific Language) or just checkboxes for common rules, that interface should be intuitive.

Mistakes in policy configuration should be minimized by the design (e.g., if you require “OS = Windows” in a policy mistakenly, it warns if applied to all devices including Macs).

Changing a policy should prompt confirmation if it’s going to mark many devices non-compliant, possibly with a preview of impact. This helps admins avoid misconfiguration that could lock everyone out inadvertently.

The ability to “rollback” or edit policies is important (similar to how EDAMAME app offers rollback for system changes
). If we save a bad policy, we should be able to disable or delete it easily.

Test Case 3.4.3: Support and Guidance for Admins
Steps:

Explore any help tooltips, documentation links, or AI assistant features available in the Hub for admins.

If an AI assistant is present, ask it a question or follow its recommendations.
Expected Outcome:

EDAMAME might extend its AI assistant to the admin side (if not, at least provide static guidance). For instance, if many devices fail a certain check, the platform might suggest “Consider updating your policy or sending a company-wide fix.”

Check for an in-app knowledge base or links to EDAMAME documentation. For example, a link to “Integrations” docs
 or a “Learn more” about Zero Trust might be present. These should open relevant, up-to-date docs.

If we encounter an unclear metric or term on the dashboard, hovering or clicking a help icon should explain it. E.g., “Security Score 2.5 – this is a weighted score of findings, higher is better” should be explained (if such scoring is shown).

The presence of these aids confirms EDAMAME’s focus on practical guidance for users at all levels, not just throwing data at them.

Test Case 3.4.4: Multi-Platform Admin Access
Steps:

Access the EDAMAME Hub using different browsers and devices (e.g., Chrome on Windows, Safari on Mac, maybe a tablet browser).

Perform basic actions (view dashboards, acknowledge an alert, etc.) on each.
Expected Outcome:

The web interface should be consistent across modern browsers. Chrome, Firefox, Safari, Edge should all display the Hub correctly.

No functionality is lost on any particular browser. (If there is a mobile-responsive design or separate app, ensure the critical monitoring features are available there as well.)

This is relevant for usability since on-call admins might need to quickly check the dashboard from different devices. The experience should remain user-friendly and secure (e.g., session management works properly on all).

All interactions (buttons, drop-downs) behave as expected, indicating a well-tested web app.