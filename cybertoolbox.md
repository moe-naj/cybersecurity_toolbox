---
notion-url: https://app.notion.com/p/Cybersecurity-Toolbox-32de74c00d7f80adbfcecf0424b2b0e7
title: Cybersecurity Toolbox
date: '2026-03-24 15:08:00.000'
from_notion: https://app.notion.com/p/Cybersecurity-Toolbox-32de74c00d7f80adbfcecf0424b2b0e7
author: Moe
last_edited_time: '2026-08-14 04:11:00.000'
---
 | **Tool** | **Details** | 
 | ---- | ---- | 
 | **Active Directory** |  | 
 | ADRecon | Used to assess the security posture of Active Directory environments. It facilitates the identification of misconfigurations, privilege escalation paths, and potential attack vectors. | 
 | bloodyAD | A Python-based Active Directory manipulation/privilege-abuse tool that lets you read and write AD objects (group memberships, passwords, ACLs, etc.) directly over LDAP using a set of valid credentials and their existing AD permissions. | 
 | certipy-ad | A Python tool for enumerating and exploiting Active Directory Certificate Services (ADCS) misconfigurations (ESC1–ESC8, etc.) used to discover vulnerable certificate templates, enrollment rights, and abuse paths that can lead to privilege escalation (often straight to Domain Admin via certificate authentication). | 
 | Coercer | A Python tool that forces a Windows host to authenticate to an attacker-controlled listener by abusing multiple RPC protocols (PetitPotam-style MS-EFSRPC, PrinterBug, etc.), primarily for NTLM/Kerberos relay or hash capture. | 
 | Kerbrute | Go-based tool that abuses Kerberos pre-authentication to enumerate valid Active Directory usernames and perform password spraying/bruteforcing without triggering traditional account lockouts. | 
 | Nltest | A built-in Windows tool to query/troubleshoot Active Directory (DC discovery, trusts, forests, secure channels). Example usage: `nltest /dsgetdc:corp.local` and `nltest /sc_verify:corp.local`. | 
 | PingCastle | Provides a fast and comprehensive Active Directory health check and security assessment, helping identify misconfigurations, weak permissions, and potential attack paths. | 
 | **Android** |  | 
 | ALEAPP | Android Logs Events And Protobuf Parser (ALEAPP) is a forensic tool that extracts, parses, and presents Android system logs, events, and protobuf-encoded data to help investigators analyze user activity and system artifacts. | 
 | APK Studio | A GUI front-end for `apktool `that lets you decompile an APK to Smali/resources, edit it, and rebuild/resign it — read/write, unlike JADX's read-only decompilation. | 
 | **Binary** |  | 
 | binwalk | A firmware/binary analysis tool that scans a file for embedded file signatures, headers, and compressed/archived data to identify and extract hidden or nested content. | 
 | Capa | An open-source tool (by Mandiant) that identifies a binary’s likely capabilities/behaviors (e.g., persistence, injection, networking) by matching rules against the file. | 
 | CFF Explorer | Raw dump a resource inside an executable to disk for further analysis. If the dumped resource is a DLL, you can use dnSpy to disassemble it for analysis. | 
 | checksec | A command-line tool that reports common binary exploit mitigations (e.g., NX, PIE, RELRO, canary) for an executable; example: `checksec --file ./a.out`. | 
 | Cutter | A cross‑platform GUI front-end for radare2 used to disassemble/decompile and analyze binaries during reverse engineering. | 
 | Dedaub | A smart contract decompiler tool for Ethereum (EVM) bytecode that reconstructs higher-level logic from on‑chain/public contract bytecode (useful when source isn’t verified) to understand behavior, identify risky patterns, and aid audits/incident response. | 
 | Detect It Easy | Used for analyzing binary files to identify their compiler, packer, or cryptor. It provides detailed information about executable formats and supports multiple architectures and file types. | 
 | Floss | A malware/forensics tool that extracts and deobfuscates (including runtime-decoded) strings from executables to reveal hidden IOCs like URLs, file paths, and commands. Example: `floss malware.exe > floss_strings.txt` | 
 | Ghidra | A reverse engineering suite (from the NSA) used to disassemble, decompile, and analyze compiled binaries. | 
 | HxD | HxD is a lightweight Windows hex editor and disk/memory editor used to view, search, and modify raw bytes in files, drives, and RAM for forensic or reverse-engineering work. | 
 | IDA Pro | Interactive DisAssembler is a disassembler/decompiler that turns compiled binaries (like the malicious driver or payload here) back into readable assembly or pseudo-C — its main cyber use case is static reverse engineering: figuring out what a piece of malware or an exploit actually does without running it. | 
 | jadx | Dex to Java decompiler. Command line and GUI tools for producing Java source code from Android Dex and APK files. | 
 | JD-GUI | A standalone Windows GUI tool that decompiles Java `.class` files and `.jar` archives back into readable Java source code, letting you inspect the actual logic inside a Java library without needing the original source. | 
 | nm | A `binutils` command that lists symbols (functions/variables) from an object file or binary to help with reverse engineering/debugging; example: `nm -C ./a.out | head`. | 
 | Online Solidity Decompiler | A web-based tool that decompiles EVM bytecode (deployed Ethereum contracts) into a readable, Solidity-like representation for reverse engineering and analysis. | 
 | pe-bear | A static PE-file inspector/editor that lets you visually parse and navigate a binary's headers, sections, and data directories (imports, exports, TLS, resources, etc.) without executing it. | 
 | PEdump | A utility that parses and displays the internal structure of a Windows Portable Executable (PE) file — headers, sections, imports/exports, and resources — for static analysis of an executable. | 
 | Pev | `pev` is an open-source, cross-platform command-line toolkit for analyzing Windows PE (Portable Executable) files (now renamed/rebranded as the `readp`e project). | 
 | pyinstxtractor | Extracts embedded `.pyc`/`resources `from a PyInstaller-packed `.exe` for analysis; example: `python pyinstxtractor.py sample.exe`. | 
 | pylingual | Python decompiler that turns compiled `.pyc` (often extracted from malware/droppers) back into readable source; example: `pylingual -o out_dir dumped_module.pyc` . | 
 | r2 | A command-line reverse-engineering framework/disassembler/debugger for analyzing binaries; example: `r2 -A ./a.out`. | 
 | scdbg | A Windows shellcode analysis tool that emulates/traces shellcode to reveal its behavior (e.g., API calls, decoded strings, and IOCs) without running it on a real host. | 
 | UPX | Used to compress and decompress executable files, reducing their size without affecting functionality. It’s used for packing binaries and can also be used to unpack them for analysis. | 
 | **Cloud** |  | 
 | Pacu | An open‑source AWS exploitation framework (post‑compromise cloud pentest tool) that uses modular commands to enumerate an AWS environment and attempt privilege escalation, persistence, and data access using stolen/assumed AWS credentials. | 
 | TrailInspector | A utility for parsing and investigating AWS CloudTrail audit logs to reconstruct and analyze suspicious cloud API activity. | 
 | **Database** |  | 
 | DB Browser for SQLite | DB Browser for SQLite is a lightweight GUI tool DFIR analysts use to open and query SQLite databases (common in app/browser artifacts) to quickly inspect tables, run SQL, and extract evidence. | 
 | **Deobfuscation** |  | 
 | de4js | A browser-based JavaScript deobfuscator/beautifier used to unpack obfuscated JS extracted from a malicious PDF. | 
 | MinusOne | MinusOne is an online PowerShell deobfuscator that takes Base64‑encoded UTF‑16 input and outputs a deobfuscated script (submissions are saved to improve the tool). | 
 | **Disk** |  | 
 | Arsenal Image Mounter (AIM) | A Windows forensics tool that mounts disk images (e.g., E01/RAW/VHD/`dd`) as read-only virtual drives so you can analyze them like a live disk. | 
 | Autopsy | Autopsy is an open-source digital forensics platform (built on The Sleuth Kit) used to analyze disk images and file systems to recover artifacts and build a timeline of user/system activity. | 
 | dd | A low-level disk copy/imaging command that reads from a block device/file and writes a bit‑for‑bit output (commonly used to create forensic disk images). | 
 | FTK Imager | FTK Imager is a digital forensics tool used to quickly create forensic disk/memory images and preview/extract files and artifacts without altering the original evidence. AD1 is the `AccessData `FTK logical evidence container format. | 
 | KAPE | KAPE (Kroll Artifact Parser and Extractor) is a DFIR tool that quickly collects key forensic artifacts (and can optionally run parsers on them) from a Windows system or disk image for triage. | 
 | libewf | Open-source library and toolset for reading and writing EnCase Expert Witness Format (`E01`) forensic disk images on Linux. | 
 | UAC | An incident response and forensic tool for Unix-like systems (Linux, macOS, Solaris, AIX, etc.) that collects artifacts, logs, memory info, running processes, network connections, and more into a structured output directory. | 
 | Velociraptor | An open-source DFIR endpoint monitoring, live response, and forensic investigation platform by Rapid7 that uses a query language called VQL to collect, hunt, and analyze forensic artifacts across endpoints at scale. | 
 | **Document** |  | 
 | oletools | `oletools` is a Python toolkit for analyzing Microsoft Office documents and OLE files. It includes utilities like `olevba` (extract and deobfuscate VBA macros), `oledump` (inspect OLE streams), `mraptor` (detect suspicious macro patterns), and `oleobj` (extract embedded objects). It is commonly used for **static malware analysis** of malicious Office files. | 
 | pdfid | A quick PDF triage tool (Didier Stevens) that counts suspicious PDF keywords (e.g. `/JavaScript`, `/OpenAction`, `/AcroForm`) to flag a file as worth deeper analysis. | 
 | pdfparser | Didier Stevens tool that parses and dumps individual PDF objects/streams (including decompressing and decoding filters) for manual inspection. | 
 | PDFStreamDumper | Windows GUI tool for exploring PDF streams and objects with built-in JavaScript deobfuscation and shellcode analysis features. | 
 | peepdf | Python-based interactive PDF analysis framework that parses object structure, decodes streams, and can extract/analyze embedded JavaScript in one tool. | 
 | **Email** |  | 
 | 4n6 Outlook Forensics Analyzer | 4n6 (Forensiksoft Outlook Forensics) is an email forensics tool used to parse and analyze Outlook mailbox data (PST/OST/MSG) to investigate messages, headers, attachments, and user activity for incidents like phishing/BEC. | 
 | Sublime Security | Email security platform focused on detecting and responding to malicious or suspicious email using a detection engine and API-driven workflows (phishing, BEC, malware delivery). | 
 | **Filesystem** |  | 
 | e2fsck | A filesystem consistency-check and repair tool for ext2/ext3/ext4 filesystems that verifies and fixes metadata structures, including replaying a pending journal. | 
 | fls | A Sleuth Kit command that lists files and directories in a disk image (including deleted entries), typically by walking a filesystem or a specific directory inode. | 
 | icat | A Sleuth Kit command that extracts a file’s contents from a disk image (by inode/MFT entry), commonly used to recover and carve out deleted files for analysis. | 
 | istat | A Sleuth Kit command that displays a filesystem's low-level metadata (timestamps, attributes, MFT/inode details) for a specific file, read directly from a disk image. | 
 | MFTECmd | MFTECmd is an Eric Zimmerman DFIR command-line tool that parses the NTFS Master File Table (`$MFT`) to extract file and directory metadata/timestamps for forensic timeline analysis. Example command: `MFTECmd.exe -f "C:\Users\Administrator\Desktop\$MFT" --csv "C:\Users\Administrator\Desktop"` | 
 | MFT Explorer | MFT Explorer is a GUI forensics tool for parsing and browsing the NTFS Master File Table ($MFT) to inspect file metadata/timelines and identify resident $DATA (resident files) stored directly in MFT records. | 
 | NTFS Log Tracker | A forensic utility that parses the NTFS transaction log (`$LogFile`) and optionally USN Journal (`$UsnJrnl`) to reconstruct file system operations like create, delete, rename, and move. | 
 | **Filtering** |  | 
 | awk | Stream-processing tools to extract fields from text: `awk -F: '{print $1}' /etc/passwd` | 
 | grep | Search and filter lines matching a pattern, using a regular expression (regex): `grep -i "error" /var/log/syslog` | 
 | sed | Edit and transform text: `sed 's/foo/bar/g' file.txt` | 
 | sort | Reorder lines in lexicographic, key-based, or numeric order for organization or preparation for deduplication: `sort -u hosts.txt` | 
 | uniq | Collapse and count adjacent duplicate lines, often after `sort`: `sort file.txt | uniq -c` | 
 | **LLM** |  | 
 | garak | An open-source vulnerability scanner for LLMs that probes models for weaknesses like prompt injection, jailbreaks, data leakage, and other failure modes using automated adversarial test suites. | 
 | LLMmap | A fingerprinting technique that identifies which specific LLM (and version) is powering a black-box application by sending crafted probe queries and analyzing response patterns to match against known model signatures. | 
 | **Integrity** |  | 
 | aide | AIDE (Advanced Intrusion Detection Environment) is a Linux file integrity monitoring tool that builds a baseline of file attributes and re-checks the system to flag unexpected changes that may indicate tampering or compromise. | 
 | **Malware** |  | 
 | AutoIt Extractor | Decompiles or extracts scripts and resources from AutoIt-compiled executables. It helps reverse engineers inspect the original AutoIt code or embedded data within compiled `.exe` files. | 
 | chkrootkit | `chkrootkit `is a Linux command-line tool that scans a system for signs of rootkits by checking common binaries, processes, and known compromise indicators. | 
 | CMD Watcher | A lightweight malware-analysis tool that monitors for `cmd.exe` process creation, suspends it, extracts the full command line, and terminates the process. | 
 | FakeNet-NG | A Windows tool that simulates network services (DNS, HTTP, etc.) on an isolated analysis machine, tricking malware into "phoning home" so you can observe its C2 traffic and behavior without it ever reaching the real internet. | 
 | pe-sieve | Dump the malware’s process memory, revealing its actual payload by overcoming runtime obfuscation. Run a tool like Process Hacker to identify the process ID to pass to `pe-sieve`. Afterwards, analyze the components dumped using a tool such as Detect It Easy (DIE). | 
 | pestudio | A Windows PE malware triage tool that statically analyzes executables (imports, strings, sections, headers, indicators) to quickly spot suspicious traits without running the sample. | 
 | rkhunter | `rkhunter `(Rootkit Hunter) is a Linux security scanner that checks for rootkits and related threats by validating files, permissions, and system configuration against known suspicious patterns. | 
 | Triage | [Tria.ge](http://tria.ge/) (Triage) is a public malware sandbox analysis platform that detonates submitted files/hashes in an instrumented environment and reports behavioral indicators, tags, and family classification. URL: [https://tria.ge/s](https://tria.ge/s) | 
 | unpac.me | Allows security analysts to safely detonate and analyze packed or obfuscated malware samples in a sandbox environment, extracting the actual malicious code to understand its behavior and indicators without manual unpacking. | 
 | x96dbg | Broken into both `x32dbg `and `x64dbg` , an open-source, feature-rich Windows debugger (Olly-style UI) for live dynamic analysis of 32-/64-bit binaries. | 
 | **Memory** |  | 
 | AVML | A Linux memory acquisition tool that captures a live RAM image for forensic analysis. | 
 | DumpIt | A portable single-executable tool that captures a full snapshot of a live system's RAM to a file for offline forensic analysis. Creates a bit-for-bit copy of everything in physical memory, resulting in an output file that matches the system's RAM size exactly. | 
 | dwarf2json | Converts binary debug symbols (DWARF/PDB) into structured JSON so memory forensics frameworks like Volatility can map raw RAM bytes onto named kernel structures and types. | 
 | GuyMager | A Linux memory acquisition tool (a fork/variant of `LiME`) used to capture a live RAM dump for forensic analysis. | 
 | LiMe | LiME (Linux Memory Extractor) is a kernel module that acquires a live RAM dump from a running Linux system for forensic analysis (typically outputting to a file or over the network). | 
 | MemProcFS | MemProcFS is a convenient way of viewing physical memory as files in a virtual file system. It's not technically mounting a disk image — it's *synthesizing* a filesystem view from in-memory artifacts. So when you browse it, you're seeing: **Processes** reconstructed from `EPROCESS` linked lists, **Files** pulled from the Windows file cache and memory-mapped regions, **Registry hives** that Windows keeps partially in memory, **Network connections**, handles, DLLs — all from kernel data structures. | 
 | Volatility | A complete framework for analyzing disk images including memory, process, malware, regions, network, and other indicators from a dump file. | 
 | **Network** |  | 
 | BGP Tools | The service [bgp.tools](http://bgp.tools/) is used to query BGP routing data directly when WHOIS databases are slow, incomplete, or when you need to trace actual routing paths and find the real ASN announcing a prefix in a specific region, especially for identifying infrastructure that's being proxied or routed through different RIRs than expected. | 
 | Brim | A desktop GUI tool that visualizes and explores Zeek and Suricata data. | 
 | editcap | A Wireshark tool that edits packet capture files (PCAP/PCAPNG) without re-capturing—commonly to slice by time, trim packet ranges, remove duplicates, or convert formats. Example: `editcap -A "2026-05-28 14:00:00" -B "2026-05-28 14:10:00" input.pcapng output_10min.pcapng`. This is also used for Network Miner in case of license challenges. | 
 | netsh | A Windows command-line utility for viewing and configuring network settings (interfaces, IP, firewall, Wi‑Fi, routing, etc.). | 
 | NetworkMiner | NetworkMiner focuses on reconstruction and evidence extraction rather than deep packet inspection. It’s used by incident responders, DFIR analysts, and penetration testers for quick forensics. Use cases include: session reconstruction, file extraction, credential recovery, artifact review, host profiling and passive fingerprinting. | 
 | Snort | Network intrusion detection/prevention systems that analyze traffic for malicious patterns | 
 | Suricata | Network intrusion detection/prevention systems that analyze traffic for malicious patterns. Uses rule syntax compatible with Snort, enabling you to leverage existing community rule sets. | 
 | SuricataRunner | The launcher/wrapper component that starts and manages the Suricata IDS/IPS engine process (loading its config and rule set, then feeding it packet data — live from an interface or offline from a pcap). | 
 | TCPView | TCPView is a Windows Sysinternals GUI tool that shows, in real time, which processes have which network connections open on a machine. | 
 | UFW | A simple command-line interface for managing the Linux `iptables`/`nftables` firewall (commonly on Ubuntu). | 
 | Zeek | Network analysis framework that logs and understands network behavior. Related to Brim which explores its data. | 
 | Zui | The modern Brim desktop app. Main use cases: DFIR, high-volume packer capture analysis, threat hunting, data analytics, and workflow integration. | 
 | **OSINT** |  | 
 | AlienVault OTX | A crowd‑sourced threat intelligence platform where security teams and researchers share and consume IOCs (malicious IPs/domains/URLs/file hashes) plus context like rules and writeups, packaged as “pulses.” It’s used to enrich investigations and alerts, automate hunting/blocking via integrations and APIs with SIEM/SOAR/EDR tools, and follow emerging threats from trusted contributors. | 
 | crt.sh | A public Certificate Transparency search site used to find certificates (and often subdomains/hostnames) issued for a domain by querying CT logs. | 
 | Shodan | Shodan enables security teams to discover internet-facing devices and services across their organization or target scope, identifying vulnerable or misconfigured systems that could be exploited before attackers find them. Shodan is specifically designed to search for Internet-connected devices and systems. | 
 | WhatWeb | A web technology fingerprinting / reconnaissance tool used to identify CMS, frameworks, servers, JS libraries, and other components on a target site. | 
 | **Phishing** |  | 
 | Evilgnix | Evilginx2 is an open-source adversary-in-the-middle (AiTM) phishing framework that uses a reverse proxy to capture credentials and session cookies, enabling bypass of MFA in many web login flows. | 
 | GoPhish | GoPhish is an open-source phishing simulation and security awareness training platform for creating, sending, and tracking phishing campaigns. | 
 | **Process** |  | 
 | Process Monitor (ProcMon) | Multiple use cases to monitor Windows process activity in real-time, including: Process activity summary, File summary (including grouping by extension), Registry summary, Stack summary, Network summary, Cross-reference summary. | 
 | Process Explorer | A Windows system utility that helps you monitor and manage running processes, covering main use cases like: Monitoring & Troubleshooting, Identifying Unknown Processes, Finding Process Dependencies, Killing Unresponsive Programs, Security Investigation, Analyzing Process Relationships, and File Locking Issues. | 
 | **Recovery** |  | 
 | extundelete | A command-line utility that recovers deleted files from ext3/ext4 filesystems by parsing the filesystem's journal and inode metadata to reconstruct files whose data blocks haven't yet been overwritten. | 
 | **Registry** |  | 
 | RECmd | An Eric Zimmerman command-line tool that parses Windows Registry hive files and exports forensic artifacts (often to CSV/JSON) for quick triage.⁠⁠ Example: `RECmd.exe -d "config" --bn "Kroll_Batch.reb" --csv "C:\Users\Administrator\Desktop"` using this batch file (`.reb`) for broadest registry coverage. | 
 | RegSeek | RegSeek is a Windows registry search and analysis utility used by forensic analysts to quickly locate keys/values/artifacts across live or offline registry hives. | 
 | Registry Explorer | A GUI-based forensic registry viewer that supports loading offline hives, recovering deleted keys, and replaying transaction logs. | 
 | RegRipper | A command-line tool that parses Windows registry hive files and extracts specific keys/values into readable reports using pre-built Perl plugins, without needing a live Windows system to read them. | 
 | **Secrets** |  | 
 | john | An offline password-cracking tool that takes hashed credentials and attempts to recover the original plaintext by testing candidate passwords via wordlists, rules, or brute-force. | 
 | spaCy | A Python NLP library you can use to build/customize named-entity recognition to find and label PII in text (names, locations, orgs, IDs) for data discovery, redaction, and DLP workflows. | 
 | TruffleHog | An open-source secret-scanning tool used to find exposed credentials (API keys, tokens, passwords) in Git repositories and other artifact sources. It works by scanning commits and file contents for high-entropy strings and known secret patterns, and can validate findings. Common use cases include CI/CD “prevention” checks, incident response (finding leaked keys), and repo hygiene audits. | 
 | unshadow | Merges `/etc/passwd` and `/etc/shadow` into a single file combining each user's account info with their password hash, producing the format John the Ripper expects as input for offline password cracking. | 
 | WCE | Windows Credential Editor is a credential-dumping tool that extracts NTLM hashes, cleartext passwords, and Kerberos tickets directly from LSASS process memory on Windows. | 
 | **Timeline** |  | 
 | DCode | DCode is a DFIR utility (in the Eric Zimmerman tools) used to decode/convert timestamps (e.g., FILETIME/Unix/various Windows formats) into human-readable dates. | 
 | PECmd | PECmd is an Eric Zimmerman DFIR command-line tool that parses Windows Prefetch (`.pf`) files to extract program execution history and timestamps for forensic timeline analysis. | 
 | Plaso Framework | Plaso is a digital forensics timeline framework that extracts timestamps from many artifact types via parsers and normalizes them into a single "super timeline" for analysis. | 
 | Timeline Explorer | A tool to view CSV and Excel files with easy filtering, grouping, and sorting — the typical workflow is to first use EvtxECmd to parse all Windows event logs into one CSV, then load that CSV into Timeline Explorer for filtering and viewing. | 
 | **Vulnerabilities** |  | 
 | Bandit | An open-source static analysis (SAST) tool that scans Python code for common security issues (hardcoded secrets, insecure functions, weak crypto, risky subprocess usage) before it ships. | 
 | Trivy | An open-source vulnerability scanner for containers, container images, and infrastructure-as-code (plus SBOM and secrets scanning), used to catch known CVEs and misconfigurations before deploy. | 
 | **Windows** |  | 
 | Advanced Installer | A Windows GUI tool for building and editing MSI installer packages. In DFIR, it is a primary tool for opening malicious `.msi` files and inspecting its internal structure without executing it  | 
 | attrib | A Windows command that displays or changes file attributes (e.g., set Hidden with `attrib +h file.txt` or remove it with `attrib -h file.txt`). | 
 | dnSpy | A debugger and .NET assembly editor. It is used for decompiling and debugging .NET applications, which is particularly useful in reverse engineering .NET binaries to understand their functionality. | 
 | EvtxECmd | A tool that parses Windows Event Log (`.evtx`) files into structured, human-readable output (CSV, JSON, XML, or SQLite) for analysis. Basic usage:`EvtxECmd.exe -f "C:\Logs\Security.evtx" --csv "C:\Out" --csvf Security.csv` | 
 | JLECmd | An Eric Zimmerman’s command-line tool that parses Windows Jump List files (`AutomaticDestinations `and `CustomDestinations`) into readable CSV/JSON output. | 
 | lnkinfo | A Windows shortcut (.LNK) forensic analysis tool used to parse and extract metadata/artifacts from LNK files (e.g., target path, timestamps, volume/host details) for investigations. | 
 | LOLBAS | LOLBAS (Living Off The Land Binaries and Scripts) is a curated catalog of legitimate Windows binaries/scripts that attackers commonly abuse to “live off the land” for execution, discovery, and defense evasion. | 
 | LOLDrivers | LOLDrivers (Living Off the Land Drivers) are legitimate, cryptographically signed Windows drivers that attackers abuse to bypass security controls and disable antivirus tools. | 
 | NetExec (nxc) | The successor to `crackmapexec `and a multi-protocol (SMB, WinRM, LDAP, MSSQL, RDP, SSH, etc.) post-exploitation and lateral-movement tool for enumerating, authenticating against, and abusing Windows/Active Directory environments. | 
 | PowerShell ISE | PowerShell ISE (Integrated Scripting Environment) is a built-in Windows GUI application for writing, editing, and interactively running PowerShell scripts (`.ps1` files) and commands, including executing them line-by-line or in full, with a console pane showing live output. | 
 | wevtutil | Retrieve, manage, and configure Windows Event Logs and log publishers via the command line. | 

