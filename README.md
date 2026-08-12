# awesome-ot-security
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
| [GICSP (Global Industrial Cyber Security Professional)](https://www.giac.org/certifications/global-industrial-cyber-security-professional-gicsp) | GIAC | The de facto entry-level, vendor-neutral OT/ICS cert. No mandatory prerequisite course, though SANS ICS410 is the standard prep path. |
| [GRID (GIAC Response and Industrial Defense)](https://www.giac.org/certifications/response-industrial-defense-grid) | GIAC | GRID certification holders understand how ICS-specific attacks inform mitigation strategies, and are ready to implement fundamental techniques such as network security monitoring (NSM), digital forensics and incident response (DFIR), and Active Defense approaches. |
| [GCIP (GIAC Critical Infrastructure Protection)](https://www.giac.org/certifications/critical-infrastructure-protection-gcip) | GIAC | GCIP certification holders understand the regulatory requirements of the North American Electric Reliability Corporation's Critical Infrastructure Protection standards (NERC CIP), and are equipped with practical implementation strategies. |
| [ISA/IEC 62443 Certificate Programs (Cybersecurity Fundamentals Specialist, Risk Assessment Specialist, Design/Implementation Specialist, Maintenance Specialist)](https://www.isa.org/certification/certificate-programs/isa-iec-62443-cybersecurity-certificate-program) | ISA/ISASecure | Standards-body certs tied directly to the IEC 62443 series; increasingly referenced in tender/RFP requirements. |
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
| [IC32: Using the ISA/IEC 62443 Standards to Secure Your Industrial Control Systems](https://www.isa.org/training/course-description/ic32) | ISA | IC32 is first course in the ISA/IEC 62443 Cybersecurity Certificate Program. Pass the exam to earn the ISA/IEC 62443 Cybersecurity Fundamentals Specialist certificate. |
| [IC33: Performing a Cybersecurity Risk Assessment](https://www.isa.org/training/course-description/ic33) | ISA | IC33 is the second course in the  ISA/IEC 62443 Cybersecurity Certificate Program. Pass the exam to earn the ISA/IEC 62443 Cybersecurity Risk Assessment Specialist certificate. |
| [IC34: Addressing Cybersecurity for the IACS Design & Implementation](https://www.isa.org/training/course-description/ic34) | ISA | IC34 is third course in the ISA/IEC 62443 Cybersecurity Certificate Program. Pass the exam to earn the ISA/IEC 62443 Cybersecurity Design Specialist Certificate designation. |
| [IC37: Managing Cybersecurity for the IACS Operations & Maintenance Phase](https://www.isa.org/training/course-description/ic37) | ISA | IC37 is fourth and final course in the ISA/IEC 62443 Cybersecurity Certificate Program. Pass the exam to earn the ISA/IEC 62443 Cybersecurity Maintenance Specialist Certificate designation. |
| [ISAGCA Microlearning Modules](https://isagca.org/training-education) | ISA | Free, short (5–10 min) modules covering ISA/IEC 62443 topics. |
| [EC-Council ICS/SCADA Cybersecurity](https://www.eccouncil.org/train-certify/ics-scada-cybersecurity/) | EC-Council | Course-plus-exam bundle. Foundational offense/defense concepts. Not equivalent in market weight to GICSP. |
| [Dragos Academy Training Courses](https://www.dragos.com/dragos-academy) | Dragos | On-demand training solution offering new and existing Dragos Platform customers resources necessary for successful adoption and operationalization of OT cybersecurity practices and the Dragos Platform technology. Courses can be taken at the convenience of the learner, or monthly in our virtual or in-person live training sessions. |
| [Fortiphyd Logic Training](https://learn.fortiphyd.com/) | Fortiphyd Logic | Hands-on offensive/defensive labs built by the creators of GRFICS. |


## University Courses
| Program | University | Country |
|---|---|---|
| [Industrial Cybersecurity Engineering Technology](https://www.isu.edu/industrialcybersecurity/) | Idaho State University | United States |
| [Graduate Certificate Programs: Industrial Control Systems Security](https://www.sans.edu/cyber-security-programs/graduate-certificate-industrial-control-systems-security/) | SANS Technology Institute | United States |
| [ONLINE M.S. In Cybersecurity](https://online.utulsa.edu/programs/graduate-degrees/cybersecurity/) | University of Tulsa | United States |
| [Graduate Certificate in Cybersecurity – Critical Infrastructure](https://www.tesu.edu/degrees-programs/certificates/graduate-cybersecurity-critical-infrastructure.php) | Thomas Edison State University | United States |
| [MSIT — Cyber Security (IT/OT concentration)](https://future.utsa.edu/programs/master/msit-cyber-security/) | University of Texas at San Antonio | United States |
| [MS in Applied Cybersecurity Engineering Technology](https://wwwcp.umes.edu/cset/master-of-science-in-cybersecurity-engineering-technology/) | University of Maryland Eastern Shore | United States |
| [Operational Technology and Industrial Control Systems Security](https://www.rgu.ac.uk/study/courses/operational-technology-and-industrial-control-systems-security) | Robert Gordon University | Scotland |
| [MSC Cyber Security](https://courses.uwe.ac.uk/I9001/cyber-security) | UWE Bristol | England |
| [Critical Infrastructure Cyber Security (SCADA) — Short Course](https://www.unsw.edu.au/canberra/study-with-us/short-courses/critical-infrastructure-cyber-security) | UNSW Canberra | Australia |
| [Critical Infrastructure and Control System Security](https://canberracyberhub.com.au/courses/critical-infrastructure-and-control-system-security) | UNSW Canberra | Australia |
| [PhD Research — Industrial Control Systems & SCADA Cyber Security](https://www.unsw.edu.au/canberra/our-research/phd-study-opportunities/industrial-control-systems-scada-cyber-security) | UNSW Canberra | Australia |
| [Online Professional Master's in OT – Industrial Cybersecurity](https://www.cci-es.org/en/masters-industrial-cybersecurity/) | Centro de Ciberseguridad Industrial (CCI) | Spain |
| [Singapore-ICS Cybersecurity 301 (SG-ICS301)](https://www.sutd.edu.sg/academy-course/singapore-industrial-control-systems-cybersecurity-301-sg-ics-301/programme-outline/) | SUTD | Singapore |
| [ICS (Industrial Control System) Cybersecurity Essentials](https://www.cet.np.edu.sg/stms_course/ics-industrial-control-system-cybersecurity-essentials) | Ngee Ann Polytechnic | Singapore |
| [Cybersecurity Industrial Control Systems for Engineers (CSIE – Energy)](https://www.cet.np.edu.sg/stms_course/cybersecurity-industrial-control-systems-for-engineers-csie-energy-classroom-asynchronous-e-learning/) | Ngee Ann Polytechnic | Singapore |


## Books



## Standards & Frameworks


## Protocols


## Labs, Simulators & Virtual PLCs


## Hardware to Buy


## Vendor Engineering Software


## Offensive Tooling
> Use tools with caution and carry out your own DD. I take no responsibility for the function, output, or results of these tools.

| Tool | Category | Note |
|---|---|---| 
| [SCADAVER](https://github.com/Whispergate/SCADAVER/blob/main/scripts/fetch_refs.py) | Exploitation Framework | Discovers, enumerates, and exploits devices across twelve industrial control protocols. Single binary with a terminal UI, bloodyAD-style CLI, and REST web interface. |


## Related Awesome Lists
| Title | Author | Description |
|---|---|---|
| [Awesome-ICS-Writeups](https://github.com/neutrinoguy/awesome-ics-writeups) | neutrinoguy | A collection of writeups related to ICS/SCADA hacking. |
| [Awesome-ICS-Malware](https://github.com/donadelden/awesome-ics-malware) | donadelden | A curated and updated1 list of awesome (and not-so-awesome) ICS malware. |
| [Awesome-Industrial-Protocols](https://github.com/Orange-Cyberdefense/awesome-industrial-protocols) | Orange-Cyberdefense | Compilation of industrial network protocols resources focusing on offensive security. |
| [Awesome-Industrial_Control-System-Security](https://github.com/hslatman/awesome-industrial-control-system-security) | hslatman | A curated list of resources related to Industrial Control System (ICS) security. |


















