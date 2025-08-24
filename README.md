SILKdrop

SILKdrop is an open-source, post-exploitation exfiltration PoC for ethical red teamers and defenders. It is designed to simulate highly advanced Living-Off-The-Land (LOTL), fileless, and fully undetectable (FUD) data exfiltration against live, modern EDR/SOC teams.
Disclaimer & Ethical Use

    WARNING: ETHICAL, AUTHORIZED USE ONLY

    SILKdrop is provided strictly for use in legal, authorized penetration testing and red team engagements by security professionals.
    Never operate this tool without explicit, written consent from the owner of the systems being tested.

        Unauthorized use of SILKdrop is illegal and unethical.

        Malicious, criminal, or offensive use is strictly prohibited.

        The authors and contributors (cbmw) assume no responsibility for misuse, damages, or consequences arising from use outside of ethical boundaries.

        By using, cloning, or contributing to SILKdrop, you accept these terms and all relevant laws/regulations.

        If you are in doubt, do not use the tool.

    Always respect legal frameworks and the rights of organizations. When in doubt, seek written approval and operate transparently. If you discover detection gaps or vulnerabilities, follow responsible disclosure.

Table of Contents

    Overview

    Features

    Ethical Commitment

    Post-Exploitation Use & Guidance

    Installation

    Usage

    Contributing

    License

    Legal Notice

Overview

SILKdrop, built in Rust, aims to test and improve modern detection capabilities through the simulation and research of data exfiltration via native, fileless, and LOLBins approaches.
This tool supports defenders in raising their detection/barriers while empowering red teamers to demonstrate real-world risk and improve security posture.
Features

    Fileless Exfiltration: Transfer data in-memory with no on-disk footprint.

    LOTL/LOLBins: Uses only built-in, trusted binaries/utilities for stealth.

    EDR/SOC Evasion: Intentionally challenges detection depth using modern evasion patterns.

    Exfiltration Vectors: Modular, extensible (HTTP, DNS, SMB, etc.).

    OPSEC-Focused: Minimal abnormal signs, designed to simulate serious adversary TTPs.

    Written in Rust: Memory safety and performance with low false-positive risk.

Ethical Commitment

    SILKdrop’s intent is education, simulation, and defense—not for abuse.

    Use only in approved PEN engagements, red vs blue exercises, adversary simulation, or academic research.

    Data must never be exfiltrated to unauthorized parties, and all results should be handled, stored, and destroyed per engagement contract and regulatory laws.

    All operations must be disclosed to and agreed with stakeholders pre-engagement.

    Vulnerability or gap discovery should be reported responsibly; contact the affected vendor or defender if you discover critical issues.

Post-Exploitation Use & Guidance

SILKdrop is a post-exploitation tool:

    Use only after gaining legitimate access/foothold during an authorized test.

    Demonstrates stealth exfiltration (creds, IP, simulated data) to help SOC teams recognize blind spots and improve detection capabilities.

    All sensitive exfiltrated artifacts should be sanitized, logged in your report, treated as confidential, and destroyed upon assessment completion (proof of deletion strongly recommended).

    Run only with clear scope and boundaries, as described in your engagement documentation.

    Reminders for Engagements:

        Always define the scope, rules of engagement, and expected outcomes before running SILKdrop.

        Never use real client data for demo/practice outside a legitimate engagement.

        Do not maintain persistence or propagate; operate with minimal impact and respect to operational integrity.

Installation

bash
# Prerequisite: Rust stable toolchain
curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh

# Clone and build
git clone https://github.com/cbmw/SILKdrop.git
cd SILKdrop
cargo build --release

Usage

Run with appropriate switches (after compromise, on an authorized host):

bash
./silkdrop --mode lotl --vector dns --target "C:\\SensitiveData" 
./silkdrop --exfil http --cmd "whoami"

Consult --help for options and operation modes.
Contributing

Contributions welcome. All pull requests must adhere to the ethical standards above. Improvements should be clearly justified for detection research, defense, or security education.
License

Distributed under MIT License (see LICENSE).
Legal Notice

SILKdrop is for security professionals working lawfully within the terms of written authorization, NDAs, and all applicable laws.
Misuse for unauthorized access, data exfiltration, or any illegal purpose is strictly forbidden and will result in denied support and potential reporting to relevant authorities.
Use at your own risk.

Developed and maintained by [cbmw], inspired by the open-source and professional security testing community.
