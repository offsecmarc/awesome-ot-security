# awesome-ot-security
Training, certifications, labs, protocols, and tooling for OT/ICS penetration testing and security assessments. Work In Progress.

## Contents
 
- [Start Here](#start-here)
- [Foundational Knowledge](#foundational-knowledge)
- [Certifications](#certifications)
- [Training Courses](#training-courses)
- [University Courses](#university-courses)
- [Books](#books)
- [Youtube Channels](#youtube-channels)
- [Professionals](#professionals)
- [Standards & Frameworks](#standards--frameworks)
- [Protocols](#protocols)
- [Labs, Simulators & Virtual PLCs](#labs-simulators--virtual-plcs)
- [Hardware to Buy](#hardware-to-buy)
- [Vendor Engineering Software](#vendor-engineering-software)
- [Tooling](#tooling)
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
| [HKSM ICS/OT Courses](https://hksmnow.com/#ics-ot-courses) | HK School of Management and Technology | Introductory and fundamentals courses for beginners in ICS/OT. |


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

| Book | Author(s) | Notes |
|---|---|---|
| Industrial Network Security: Securing Critical Infrastructure Networks for Smart Grid, SCADA, and Other Industrial Control Systems | Eric D. Knapp (and Joel Thomas Langill in later editions) | The standard reference text, now in multiple editions. Vendor-neutral overview of ICS/SCADA architecture and defense-in-depth. |
| Hacking Exposed Industrial Control Systems: ICS and SCADA Security Secrets & Solutions | Clint Bodungen, Bryan Singer, Aaron Shbeeb, Kyle Wilhoit, Jacob Hilt | Offense-oriented, closest in tone to a pentesting field guide. Covers real attack methodologies and exploitation techniques against ICS/SCADA. |
| Practical Industrial Cybersecurity: ICS, Industry 4.0, and IIoT | Charles J. Brooks, Philip A. Craig Jr. | Frequently cited as a GICSP self-study companion. Covers IIoT and Industry 4.0 convergence. |
| Cybersecurity for Industrial Control Systems: SCADA, DCS, PLC, HMI, and SIS | Tyson Macaulay, Bryan L. Singer | Covers ICS threat landscape, risk assessment methodology, and IT-vs-OT security requirement differences. |
| Industrial Automation and Control System Security Principles: Protecting the Critical Infrastructure | Ronald L. Krutz | Broad principles-level text on protecting critical infrastructure control systems. |
| Cyber-security of SCADA and Other Industrial Control Systems | Edward J. M. Colbert, Alexander Kott (eds.) | Academic/reference-style anthology covering ICS threats, attacks, metrics, risk, situational awareness, and intrusion detection. |
| Applied Cyber Security and the Smart Grid | Eric D. Knapp, Raj Samani | Power-sector specific — smart grid architecture and security. |
| Engineering-Grade OT Security: A Manager's Guide | Andrew Ginter | OT security framed from a managerial/engineering-risk perspective rather than a pure technical angle. |
| Implementing IEC 62443 – A Pragmatic Approach to Cybersecurity | Michael D. Medoff, Patrick C. O'Brien | Practical, standards-focused guide to applying the IEC 62443 series. |
| Countdown to Zero Day: Stuxnet and the Launch of the World's First Digital Weapon | Kim Zetter | Narrative history of Stuxnet. Good context-building on the field's defining case study; not a technical manual. |
| Sandworm: A New Era of Cyberwar and the Hunt for the Kremlin's Most Dangerous Hackers | Andy Greenberg | Narrative account of state-sponsored ICS/critical-infrastructure attacks (Industroyer, NotPetya, and the Sandworm group). Strong for building non-technical stakeholder buy-in on OT risk. |
| Protecting Industrial Control Systems from Electronic Threats | Joseph Weiss | One of the earliest dedicated ICS security texts; historical grounding on the field's foundational risk concerns. |
| Cyber Attacks on Critical Infrastructures: A Collection of Expert Perspectives | Robert Radvanovsky, Jacob Brodsky (eds.) | Community-anthology collection of articles from a wide range of ICS security practitioners and perspectives. |
| Industrial Cybersecurity (2nd Edition) | Pascal Ackerman | Each edition is a substantial, hands-on volume; practical resource for monitoring cybersecurity posture in ICS environments. |
| Industrial Cybersecurity: Case Studies and Best Practices | Steve Mustard | Real-world case studies from an engineering point of view; good intro grounded in practitioner experience. |
| Countering Cyber Sabotage: Introducing Consequence-Driven, Cyber-Informed Engineering (CCE) | Andrew A. Bochman, Sarah Freeman | Applies engineering principles to protect OT/ICS from cyber sabotage; introduces the CCE methodology. |


## YouTube Channels

| Channel | Type | Description |
|---|---|---|
| [@utilsec](https://www.youtube.com/@utilsec) | Individual Contributor | Getting-started guidance and practical advice for breaking into OT/ICS cybersecurity. |
| [@RickCenOT](https://www.youtube.com/@RickCenOT) | Individual Contributor | OT/ICS hardware hacking and pentesting, covering SCADA, PLC, and IIoT device security. |
| [@ZakharBernhardt](https://www.youtube.com/@ZakharBernhardt) | Individual Contributor | Home of Labshock, a virtual OT/ICS lab for hands-on practice. |
| [@icsotsecurity](https://www.youtube.com/@icsotsecurity) | Individual Contributor | Manjunath's channel on industrial automation and OT/ICS/SCADA security, with a strong ISA/IEC 62443 focus. |
| [@Cursed_Controls](https://www.youtube.com/@Cursed_Controls) | Individual Contributor | Industrial maintenance, PLCs, VFDs, and motor controls. Raw, hands-on electrical/automation content, not a safety tutorial. |
| [@S4Events](https://www.youtube.com/@S4Events) | Conference | Talks from S4, the largest annual ICS/OT security conference. |
| [@ICSVillage](https://www.youtube.com/@ICSVillage) | Conference | DEF CON's ICS Village. Critical infrastructure security education, plus the Hack the Planet podcast. |
| [@HoustonSecurityConference](https://www.youtube.com/@HoustonSecurityConference) | Conference | Includes OT.SEC.CON presentations on operational technology security. |
| [@CS2AI](https://www.youtube.com/@CS2AI) | Association | Recordings from (CS)²AI, the global nonprofit association for OT/ICS security professionals. |
| [@OTSecurityProfessionals](https://www.youtube.com/@OTSecurityProfessionals) | Association | Community-driven OT security content from the OT Sec Professionals group. |
| [@SANSICSSecurity](https://www.youtube.com/@SANSICSSecurity) | Training Company | SANS' official ICS/OT training content from their instructor lineup. |
| [@OPSWATAcademy](https://www.youtube.com/@OPSWATAcademy) | Training Company | OPSWAT's training platform covering IT and OT cybersecurity fundamentals. |
| [@PrOTectITAll](https://www.youtube.com/@PrOTectITAll) | Podcast | Aaron Crow's podcast on the intersection of OT, IT, and compliance. |
| [@ICSArabiaPodcast](https://www.youtube.com/@ICSArabiaPodcast) | Podcast | Sulaiman Alhasawi's ICS/OT security podcast, in English and Arabic. |
| [@BitesandBytesPodcast](https://www.youtube.com/@BitesandBytesPodcast) | Podcast | Kristin Demoranville's podcast on cybersecurity in the food & agriculture sector. |
| [@LMTX](https://www.youtube.com/@LMTX) | Individual Contributor | Lukasz Malinowski on IoT/IIoT/OT, aimed at helping SMBs build enterprise-grade solutions. |
| [@DragosInc](https://www.youtube.com/@DragosInc) | Vendor | Dragos' ICS/OT threat research and platform content. |
| [@WaterfallSecuritySolutions](https://www.youtube.com/@WaterfallSecuritySolutions) | Vendor | Waterfall Security's content and podcast on cyber-physical OT protection. |
| [@Claroty20](https://www.youtube.com/@Claroty20) | Vendor | Claroty's OT/IoT security research and podcast episodes. |
| [@xIoTSecurity](https://www.youtube.com/@xIoTSecurity) | Vendor | Phosphorus' content and podcast on xIoT/OT device security. |
| [@NozomiNetworks](https://www.youtube.com/@NozomiNetworks) | Vendor | Nozomi Networks' OT/IoT security content, including talks from Marty Edwards. |
| [@InsaneCyberInc](https://www.youtube.com/@InsaneCyberInc) | Vendor | Dan Gunter and team on OT/ICS cyber defense. |
| [@CISAgov](https://www.youtube.com/@CISAgov) | Government/Regulator | CISA's official channel. Training pointers and critical infrastructure security content. |
| [@SimplyCyber](https://www.youtube.com/@SimplyCyber) | Training Company | General cyber career/training channel now covering OT/ICS with Don Wagner and Tom VanNorman. |
| [@PancakesCon](https://www.youtube.com/@PancakesCon) | Conference | Lesley Carhart's annual, low-pressure cybersecurity con with a fun twist. |
| [@USCSB](https://www.youtube.com/@USCSB) | Government/Regulator | US Chemical Safety Board. Detailed investigation videos on industrial plant incidents and what went wrong. |
| [@RealPars](https://www.youtube.com/@realpars) | Training Company | Industrial automation and PLC programming fundamentals across Siemens, Allen-Bradley, and other platforms. Not security-focused, but a strong prerequisite for understanding what you're attacking. |
| [@plcprofessor](https://www.youtube.com/@plcprofessor) | Individual Contributor | Free, classroom-built lecture and hands-on lab series on PLC fundamentals (RSLogix/Studio 5000), aimed at electricians and engineers new to control systems. |


## Professionals
| Name | Bio |
|---|---|
| [Aaron C. Crow](https://linkedin.com/in/aaronccrow) | Hosts the PrOTect IT All podcast, focused on OT/ICS security conversations. |
| [Adam Bromiley](https://www.linkedin.com/in/adambromiley/) | OT and embedded security consultant at Pen Test Partners |
| [Alana Murray](https://www.linkedin.com/in/alana-murray-065a64297) | Works in OT/ICS security at Halifax Water, a Canadian utility. |
| [Andrew Ginter](https://www.linkedin.com/in/andrewginter/) | VP of Industrial Security at Waterfall Security. Author of "Engineering-Grade OT Security." |
| [Anna Ribeiro](https://www.linkedin.com/in/anna-ribeiro-59a82264/) | Journalist and editor at Industrial Cyber, covering OT/ICS security news. |
| [Bryan Singer](https://www.linkedin.com/in/bryan-l-singer/) | OT security leader at Accenture. Co-author of "Hacking Exposed Industrial Control Systems." |
| [Bryson Bort](https://www.linkedin.com/in/brysonbort/) | Founder of ICS Village and SCYTHE. Prominent OT security advocate and speaker. |
| [Chris Sistrunk](https://www.linkedin.com/in/chrissistrunk/) | OT security expert at Mandiant. Well known ICS incident response voice. |
| [Clint Bodungen](https://www.linkedin.com/in/clintb/) | Founder of ThreatGEN. Co-author of "Hacking Exposed Industrial Control Systems." |
| [Dale Peterson](https://linkedin.com/in/dale-peterson-s4) | Founder of S4 Events and Digital Bond. Longtime ICS security thought leader. |
| [Dan Gunter](https://www.linkedin.com/in/dan-gunter/) | Works at Insane Cyber, focused on OT/ICS threat detection. |
| [Dan Ricci](https://www.linkedin.com/in/danricci14/) | Runs the ICS Advisory Project, tracking ICS vulnerability advisories. |
| [Danielle Jablanski](https://www.linkedin.com/in/daniellejjablanski/) | OT security professional at SVG (Southern Company). |
| [David Batz](https://www.linkedin.com/in/davidbatz/) | Works on grid security at Edison Electric Institute. |
| [Dawn Cappelli](https://www.linkedin.com/in/dawn-cappelli-cissp-a329505/) | OT/ICS security leader at Dragos, formerly built Rockwell Automation's threat program. |
| [Dean Parsons](https://www.linkedin.com/in/dean-parsons-cybersecurity/) | Founder of ICS Defense Force. SANS instructor for ICS security training. |
| [Derek Harp](https://linkedin.com/in/derekharp) | Founder of CS2AI (Control System Cyber Security Association International). |
| [Don C. Weber](https://linkedin.com/in/cutaway) | Founder of Cutaway Security. SANS instructor in ICS/OT penetration testing. |
| [Eric Knapp](https://www.linkedin.com/in/ericdknapp/) | OT security expert at OPSWAT. Author of "Industrial Network Security." |
| [Emma Stewart](https://www.linkedin.com/in/emma-m-stewart/) | OT/ICS security researcher at Idaho National Laboratory. |
| [Jason Christopher](https://linkedin.com/in/jdchristopher) | Works with EIP and SANS on ICS/OT security and grid resilience. |
| [Jason Dely](https://www.linkedin.com/in/jasonjdely/) | OT security expert at NetRise. SANS instructor. |
| [Joe Langill](https://www.linkedin.com/in/joel-langill-scadahacker/) | Expert, consultant, and author in the OT/ICS domain. |
| [Joe Marshall](https://www.linkedin.com/in/joeics/) | OT security lead at Cisco, focused on industrial network defense. |
| [Joe Slowik](https://www.linkedin.com/in/joe-slowik/) | Threat intelligence expert at MITRE, focused on ICS-targeting adversaries. |
| [John Kingsley](https://www.linkedin.com/in/sjkingsley/) | OT security professional at Hitachi Energy. |
| [Jonathan Pollet](https://www.linkedin.com/in/jonathanpollet/) | OT/ICS security consultant and researcher, with a background spanning industrial risk assessment and penetration testing. |
| [Jonathon Gordon](https://www.linkedin.com/in/jonathongordon/) | Industry analyst at Takepoint Research, covering industrial cybersecurity. |
| [Justin Searle](https://www.linkedin.com/in/meeas/) | OT security expert at InGuardians. SANS instructor. |
| [Kate Johnson](https://www.linkedin.com/in/kate-johnson-12954941/) | Works in OT security at Consumers Energy. |
| [Kevin Kumpf](https://www.linkedin.com/in/kevin-kumpf-b5021412/) | Works at Hard Hat Cybersecurity, focused on OT risk management. |
| [Kristin King](https://www.linkedin.com/in/kingmkristin/) | Founder of AnzenOT. Hosts the Bites & Bytes podcast on food and agriculture OT security. |
| [Lesley Carhart](https://www.linkedin.com/in/lcarhart/) | Director of Incident Response at Dragos. Well known ICS security speaker and writer. |
| [Manjunath Hiregange](https://www.linkedin.com/in/manjunathhiregange/) | OT security professional at GE Vernova. |
| [Marcel Rick-Cen](https://www.linkedin.com/in/marcelrickcen/) | OT security lead at Henkel. |
| [Mark Fabro](https://www.linkedin.com/in/mark-fabro-a4319321/) | Longtime OT/ICS security consultant and researcher, recognized as one of the field's founding practitioners. |
| [Mark Hyman](https://www.linkedin.com/in/mark-hyman-gtm/) | Talent and go to market specialist connecting professionals with OT/IoT cybersecurity roles. |
| [Marty Edwards](https://www.linkedin.com/in/icsmartyedwards/) | OT security executive, associated with SiriusPPT. Former ICS-CERT director. |
| [Michelle Balderson](https://www.linkedin.com/in/michelle-balderson-34498a13/) | OT security professional at ISSQUARED. |
| [Mike Holcomb](https://linkedin.com/in/mikeholcomb) | Runs UtilSec and mikeholcomb.com, focused on OT/ICS education. |
| [Oren Niskin](https://www.linkedin.com/in/orenniskin/) | OT security professional at Guidepoint. |
| [Pascal Ackerman](https://www.linkedin.com/in/pascal-ackerman-036a867b/) | Principal at 1898 & Co. Author of "Industrial Cybersecurity." |
| [Patrick Miller](https://www.linkedin.com/in/millerpatrickc/) | CEO of Ampyx Cyber (formerly Ampere Industrial Security). |
| [Paul Shaver](https://www.linkedin.com/in/pbshaver/) | OT security consultant at Mandiant. |
| [Paul Smith](https://www.linkedin.com/in/paul-smith-cyber/) | OT security professional at Honeywell. |
| [Ric Derbyshire](https://www.linkedin.com/in/ricderby/) | Principal Security Researcher, OT & Critical Infrastructure at Orange Cyberdefense. |
| [Robert M. Lee](https://linkedin.com/in/robmichaellee) | CEO and founder of Dragos. SANS instructor and leading ICS threat intelligence figure. |
| [Roya Gordon](https://www.linkedin.com/in/roya-gordon-ciso/) | OT security researcher and advisor. |
| [Saltanat Mashirova](https://www.linkedin.com/in/saltanat-mashirova-b88bba193/) | OT security professional at CPX. |
| [Sam Thom](https://www.linkedin.com/in/blackfell/) | Hardware and Operational Technology security consultant at Pen Test Partners |
| [Sasha Mullins Lassiter](https://www.linkedin.com/in/chromecowgirl/) | OT security professional at Dragos. |
| [Shiv Kataria](https://www.linkedin.com/in/shivkataria/) | OT security professional at Siemens. |
| [Sinclair Koelemij](https://www.linkedin.com/in/sihoko/) | Runs Cyber-Physical Risk consultancy. |
| [Stuart King](https://www.linkedin.com/in/stu8king/) | Founder and CTO of AnzenOT. |
| [Sulaiman Alhasawi](https://www.linkedin.com/in/alhasawi/) | Founder of ICSRank/ZeronTek. Hosts ICS Arabia podcast. |
| [Talib Usmani](https://www.linkedin.com/in/talib-usmani/) | OT security professional at Honeywell. |
| [Tim Conway](https://www.linkedin.com/in/tim-conway-sans/) | SANS Institute instructor and ICS curriculum lead. |
| [Tony Turner](https://www.linkedin.com/in/tonyturnercissp/) | VP Product at Frenos. SANS instructor for supply chain security. |
| [Thomas VanNorman](https://www.linkedin.com/in/thomasvannorman/) | Works with ICS Village. |
| [Yury Kozlov](https://linkedin.com/in/yury-kozlov) | OT Controls engineering manager at Greater Toronto Airports, shares trainig courses. |
| [Zakhar Bernhardt](https://www.linkedin.com/in/zakharb/) | Founder and CEO of Labshock Security. Creator of an OT focused SIEM platform. |


## Standards & Frameworks


## Protocols


## Labs, Simulators & Virtual PLCs


## Hardware to Buy


## Vendor Engineering Software


## Tooling
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


> This work is licensed under [CC BY 4.0.](https://creativecommons.org/licenses/by/4.0/legalcode.txt)















