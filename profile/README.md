# Welcome to EDAMAME Technologies

## What Do We Do?
EDAMAME ensures all machines accessing code, secrets, or sensitive test data are secured without the challenges of traditional Unified Endpoint Management. Empower every stakeholder—from contractors to developers—to safeguard the software development lifecycle without slowing down development.

## For Users: EDAMAME Security
EDAMAME Security is the Flutter-based GUI version of our Rust-based security core. Here's what it encompasses:

- **Security Benchmarks:** Utilizes standards such as [CIS Benchmarks](https://www.cisecurity.org/cis-benchmarks), SOC2, and ISO27001.
- **Digital Identity Management:** Integrated with [HaveIBeenPwned.com](https://HaveIBeenPwned.com) for online identity management.
- **Network Scanning for Everyone:** Inspired by 'nmap', we've made network scanning accessible to all.
- **Egress Network Monitoring:** Inspired by 'Wireshark', we offer a simple visualization of outgoing traffic with Layer 7 (L7) classification.
- **Certified Compliance Report Generation:** Contractors required to prove their device meets baseline security requirements (SOC2 or ISO27001) can generate a compliance report with a single click.
- **Privacy-First Management:** Connects to our "no MDM" platform ([edamame.tech](https://www.edamame.tech)), enabling continuous reporting of security posture and integration with access control to implement Zero Trust for code, secrets, and test data access.

## Download the Application

### macOS
- Install the full app installer from EDAMAME: [Download](https://edamame.s3.eu-west-1.amazonaws.com/windows/edamame-latest.msix)
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
- Access the freely available beta of our SaaS service for enterprises, including a demo on a simulated domain: [EDAMAME Hub](https://hub.edamame.tech).
- Create your domain, verify it, and onboard your users through the Onboarding tab.

## For Developers: EDAMAME Posture
When managing access to source code, our solution uniquely allows you to:

- Inspect and harden every SDLC device—from edge to cloud, employees to contractors.
- Enforce security and compliance through Zero Trust, complementing existing security stacks.
- Enhance security for developers without compromising productivity.

Our CLI tool ([GitHub](https://github.com/edamametechnologies/edamame_posture_cli)), GitHub Action ([GitHub](https://github.com/edamametechnologies/edamame_posture_action)), or GitLab Action ([GitLab](https://gitlab.com/edamametechnologies/edamame_posture_action)) are ideal for hardening and checking the security of CI/CD runners or test machines (Linux, Windows, macOS).

## Access Control Integrations
- Learn how to integrate your Conditional Access system with EDAMAME: [Integrations](https://github.com/edamametechnologies/integrations).

## Resources
- [Threat Models Wiki](https://github.com/edamametechnologies/threatmodels/wiki)
- [YouTube Channel](https://www.youtube.com/@edamametech)
