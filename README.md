# OT-Resources
Training, certifications, labs, protocols, and tooling for OT/ICS penetration testing and security assessments.

## Contents
 
- [Start Here](#start-here)
- [Foundational Knowledge](#foundational-knowledge)
- [Certifications](#certifications)
- [Training Courses](#training-courses)
- [University Courses](#university-courses)
- [Books](#books)
- [Standards & Frameworks](#standards--frameworks)
- [Protocols](#protocols)
- [Labs, Simulators & Virtual PLCs](#labs-simulators--virtual-plcs)
- [Hardware to Buy](#hardware-to-buy)
- [Vendor Engineering Software](#vendor-engineering-software)
- [Offensive Tooling](#offensive-tooling)
- [Defensive / Monitoring Tooling](#defensive--monitoring-tooling)
- [CTFs, Ranges & Competitions](#ctfs-ranges--competitions)
- [Datasets, PCAPs & Malware Samples](#datasets-pcaps--malware-samples)
- [Threat Intelligence & Malware Research](#threat-intelligence--malware-research)
- [Vulnerability Research & Advisories](#vulnerability-research--advisories)
- [Communities, Conferences & People to Follow](#communities-conferences--people-to-follow)
- [Related Awesome Lists](#related-awesome-lists)
- [Contributing](#contributing)
---

## Start Here

A short on-ramp for someone coming from a pure IT/web/AD pentesting background:
 
1. Learn the vocabulary and architecture (Purdue Model, PLC/RTU/HMI/SCADA/DCS distinctions, IT vs OT priorities — availability over confidentiality).
2. Learn one protocol properly (Modbus is the easiest entry point) before trying to learn all of them.
3. Stand up a free simulator (OpenPLC + a HMI, or GRFICS) and attack it yourself before touching real hardware.
4. Pick up cheap real hardware (a Raspberry Pi running OpenPLC, or a second-hand Siemens Logo!/S7-1200) once the simulated environment feels comfortable.
5. Layer on a vendor-neutral cert (GICSP) once you have hands-on time, not before.


## Foundational Knowledge


## Certifications

| Certification | Body | Notes |
|---|---|---|
| [GICSP](https://www.giac.org/certifications/global-industrial-cyber-security-professional-gicsp) (Global Industrial Cyber Security Professional) | GIAC | The de facto entry-level, vendor-neutral OT/ICS cert. No mandatory prerequisite course, though SANS ICS410 is the standard prep path. |
| [GRID](https://www.giac.org/certifications/response-industrial-defense-grid) (GIAC Response and Industrial Defense) | GIAC | GRID certification holders understand how ICS-specific attacks inform mitigation strategies, and are ready to implement fundamental techniques such as network security monitoring (NSM), digital forensics and incident response (DFIR), and Active Defense approaches. |
| [GCIP](https://www.giac.org/certifications/critical-infrastructure-protection-gcip) (GIAC Critical Infrastructure Protection) | GIAC | GCIP certification holders understand the regulatory requirements of the North American Electric Reliability Corporation's Critical Infrastructure Protection standards (NERC CIP), and are equipped with practical implementation strategies. |
| [ISA/IEC 62443 Certificate Programs](https://www.isa.org/certification/certificate-programs/isa-iec-62443-cybersecurity-certificate-program) (Cybersecurity Fundamentals Specialist, Risk Assessment Specialist, Design/Implementation Specialist, Maintenance Specialist) | ISA/ISASecure | Standards-body certs tied directly to the IEC 62443 series; increasingly referenced in tender/RFP requirements. |
| [CompTIA SecOT+](https://www.comptia.org/en-us/certifications/secot/) | CompTIA | CompTIA SecOT+ validates your skills to secure and manage operational technology (OT) systems in manufacturing and critical infrastructure. Launches in December 2026. |


## Training Courses

| Course | Body | Notes
|---|---|---|
| [CISA (Cybersecurity and Infrastructure Security Agency)](https://www.cisa.gov/resources-tools/programs/ics-training-available-through-cisa) | CISA | CISA offers free industrial control systems (ICS) cybersecurity training to protect against cyberattacks on critical infrastructure, such as power grids and water treatment facilities. CISA’s ICS training is globally recognized for its relevance and is available virtually around the world. |
| [ICS310: ICS Cybersecurity Foundations](https://www.sans.org/cyber-security-courses/ics-cybersecurity-foundations) | SANS | Entry-level, self-paced, 1-day equivalent. No certification attached — pure foundations for those with zero ICS/OT background. |
| [ICS410: ICS/SCADA Security Essentials](https://www.sans.org/cyber-security-courses/ics-scada-cyber-security-essentials) | SANS | The standard on-ramp course. Prep path for the GICSP certification. Includes a PLC kit students keep. |
| [ICS418: ICS Security Essentials for Leaders](https://www.sans.org/cyber-security-courses/ics-security-essentials-leaders) | SANS | Management/leadership-focused, not technical hands-on. No certification attached. |
| [ICS456: Essentials for NERC Critical Infrastructure Protection](https://www.sans.org/cyber-security-courses/essentials-for-nerc-critical-infrastructure-protection) | SANS | NERC CIP compliance focus, power/utilities sector. Prep path for the GCIP certification. |
| [ICS515: ICS Visibility, Detection, and Response](https://www.sans.org/cyber-security-courses/ics-visibility-detection-response) | SANS | Active defense/threat-hunting/incident-response focus. Prep path for the GRID certification. |
| [ICS612: ICS Cybersecurity In-Depth](https://www.sans.org/cyber-security-courses/ics-cyber-security-in-depth) | SANS | Advanced, hands-on, simulated OT environment across the full Purdue stack. No certification attached currently. |
| [ICS613: ICS/OT Penetration Testing & Assessments](https://www.sans.org/cyber-security-courses/ics-ot-penetration-testing-assessments) | SANS | Most directly relevant SANS course for offensive work — safe assessment methodology, protocol analysis, ICS Cyber Kill Chain-aligned attack scenarios. No certification attached currently. |

## University Courses
