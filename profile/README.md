# Welcome to EDAMAME Technologies

## What Do We Do?
EDAMAME ensures all machines accessing code, secrets, or sensitive test data are secured without the challenges of traditional Unified Endpoint Management. Empower every stakeholder—from contractors to developers—to safeguard the software development lifecycle without slowing down development.

## For Users: EDAMAME Security
EDAMAME Security is your all-in-one tool to secure, understand and prove your dev workstation—from OS to network. It delivers compliance audits, network analysis, and vulnerability insights, all while seamlessly integrating with your workflows and OS.

EDAMAME Security is the Flutter-based GUI for our Rust-based security core. Here's what it encompasses:

- **Security Benchmarks:** Utilizes standards such as [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks), SOC2, and ISO27001.
- **Digital Identity Management:** Integrated with [HaveIBeenPwned.com](https://HaveIBeenPwned.com) for online identity management.
- **Network Scanning for Everyone:** Inspired by 'nmap', we've made network scanning accessible to all.
- **Egress Network Monitoring:** Inspired by 'Wireshark', we offer a simple visualization of outgoing traffic with Layer 7 (L7) classification.
- **Certified Compliance Report Generation:** Contractors required to prove their device meets baseline security requirements (SOC2 or ISO27001) can generate a compliance report with a single click.
- **Privacy-First Management:** Connects to our "no MDM" platform ([edamame.tech](https://www.edamame.tech)), enabling continuous reporting of security posture and integration with access control to implement Zero Trust for code, secrets, and test data access.



https://github.com/user-attachments/assets/3ee7a538-0240-4ae7-a715-3a3593445d73



## Download the Application

### macOS
- Install the full app installer from [EDAMAME](https://edamame.s3.eu-west-1.amazonaws.com/windows/edamame-latest.pkg).
- Or install the app from the [Mac App Store](https://apps.apple.com/app/edamame-security/id1636777324) and then install the open-source system helper from [GitHub](https://github.com/edamametechnologies/edamame_helper/releases) to enable advanced system access and remediations.

### Windows
1. Install the app from [EDAMAME](https://edamame.s3.eu-west-1.amazonaws.com/windows/edamame-latest.msix) or the [Microsoft Store](https://www.microsoft.com/store/apps/9N399LMTKQLQ).
2. Install the open-source system helper from [GitHub](https://github.com/edamametechnologies/edamame_helper/releases) to enable advanced system access and remediations.
3. Install [npcap](https://npcap.com/#download), the packet capture library from the Nmap team, to unlock the traffic capture feature.

### iOS
- Install the app from the [App Store](https://apps.apple.com/app/edamame-security-mobile/id6448937722).

### Android/ChromeOS
- Install the app from the [Google Play Store](https://play.google.com/store/apps/details?id=com.edamametech.edamame).

### Linux
We provide a GPG-signed APT repository for `.deb` packages, ensuring secure and verified installation. Follow these steps:

1. **Import the EDAMAME GPG public key**:
   ```bash
   wget -O - https://edamame.s3.eu-west-1.amazonaws.com/repo/public.key | sudo gpg --dearmor -o /usr/share/keyrings/edamame.gpg
   ```

2. **Add the EDAMAME repository**:
   ```bash
   echo "deb [arch=amd64 signed-by=/usr/share/keyrings/edamame.gpg] https://edamame.s3.eu-west-1.amazonaws.com/repo stable main" | sudo tee /etc/apt/sources.list.d/edamame.list
   ```
   *(Replace `arch=amd64` with your system architecture if needed, e.g., `arm64`, `i386`.)*

3. **Install EDAMAME Security**:
   ```bash
   sudo apt update
   sudo apt install edamame-security
   ```

## For Administrators: EDAMAME Hub
Ensure all machines accessing code, secrets, or sensitive test data are secured without the challenges of traditional Unified Endpoint Management. Empower every stakeholder—from contractors to developers—to safeguard the software development lifecycle without slowing down development.

- Access the free plan of our SaaS service for enterprises, including a demo on a simulated domain: [EDAMAME Hub](https://hub.edamame.tech).
- Create your domain, verify it, and onboard your users through the Onboarding tab.



https://github.com/user-attachments/assets/335298d0-9e26-4eb3-a388-f1ce6471822d



## For Developers: EDAMAME Posture
Integrate EDAMAME's CLI tools for Windows, macOS or Linux ([GitHub](https://github.com/edamametechnologies/edamame_posture_cli)), GitHub Action ([GitHub](https://github.com/edamametechnologies/edamame_posture_action)), or GitLab Action ([GitLab](https://gitlab.com/edamametechnologies/edamame_posture_action)) into your CI/CD.

- **Ultra Easy Deployment:** Utilize our self-service portal for effortless setup, and seamlessly integrate with your CI/CD pipeline using our portable CLI tool and GitHub Action. Experience quick and efficient deployment, ensuring your development process is secure and optimized with minimal effort.

- **Automated Hardening:** This solution automatically hardens your CI/CD runners and dynamically detects and responds to security posture changes throughout the runner lifecycle. Ensure continuous protection and compliance without manual intervention, keeping your development process secure at every stage.

- **Advanced Threat Model:** Not only does it evaluate the security posture of your operating system, but it also performs federated LAN scanning to verify network segmentation and captures traffic for a network audit trailer of the runner communications. This dual-layered approach ensures comprehensive protection, identifying and mitigating vulnerabilities across both your system and network infrastructure.

## Access Control Integrations
EDAMAME ensures that only devices running its platform—and meeting stringent security and compliance standards—gain access to vital resources such as code repositories, secrets, and test data. By continuously verifying endpoint security at the OS, network, and configuration levels, it enforces Zero Trust principles, granting entry exclusively to secure, trusted devices.

Thanks to EDAMAME's versatile access control integration engine, it's simple to configure and customize for your unique environment. Compatible with virtually any REST or GraphQL-supporting API, it seamlessly integrates with existing Zero Trust architectures and access control solutions, including Identity Providers, Application Providers, and Network Access Control systems such as firewalls and VPNs.

- Learn how to integrate your Conditional Access system with EDAMAME: [Integrations](https://github.com/edamametechnologies/integrations).

## Resources
- [Threat Models Wiki](https://github.com/edamametechnologies/threatmodels/wiki)
