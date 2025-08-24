# SILKdrop

SILKdrop is an open-source, advanced post-exploitation data exfiltration proof-of-concept built in Rust. Designed for authorized red team and security research activities, SILKdrop leverages stealthy, fileless, and Living-Off-The-Land (LOTL) techniques to emulate fully undetectable (FUD) exfiltration attacks against modern EDR and SOC teams.

---

## DISCLAIMER & ETHICAL USE

> FOR AUTHORIZED SECURITY TESTING AND EDUCATION ONLY
>
> SILKdrop is strictly intended for use by professional penetration testers, red teamers, or researchers operating under explicit, written authorization from the owners of the targeted systems.
>
> - Never use this tool for unauthorized, unethical, or illegal activities.
> - Any form of malicious or non-consensual use is strictly prohibited and may be unlawful.
> - The author ([cbmw](https://github.com/cbmw)) and contributors assume no liability for damages or consequences resulting from misuse.
> - By downloading, cloning, or contributing, you acknowledge all responsibility for ethical, legal, and safe usage.  
> - If you do not understand or accept these terms, do not use SILKdrop.
>
> Always consult with stakeholders, define your scope in writing, and follow responsible disclosure practices. If you find detection gaps, report them responsibly.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Ethical Commitment](#ethical-commitment)
- [Post-Exploitation Guidance](#post-exploitation-guidance)
- [Installation](#installation)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)
- [Legal Notice](#legal-notice)

---

## Overview

SILKdrop simulates advanced threat actor tactics by exfiltrating data covertly via built-in, trusted system tools and memory-resident payloads. This provides valuable insight into detection blind spots and helps blue teams fine-tune their monitoring and response.

Strictly for research, education, and authorized adversary simulation.

---

## Features

- Fileless Operation: No data written to disk, minimizing forensic footprint.
- LOTL / LOLBins: Utilizes only OS-native binaries for exfiltration.
- EDR/SOC Evasion: Designed to test and challenge advanced defense mechanisms.
- Modular Exfil Vectors: Supports extensibility for multiple stealth channels (HTTP, DNS, SMB, etc.).
- High OPSEC: Unusual patterns minimized for realism and stealth.
- Rust Core: Modern, safe systems programming for robust, reliable execution.

---

## Ethical Commitment

- Focus: Empower defenders and red teams to identify, test, and close exfiltration blind spots—not for real-world data theft or harm.
- Scope: Use ONLY during authorized engagements, adversary simulations, or academic research with full written permission.
- Data Handling: All simulated or exfiltrated artifacts must be sanitized, logged, and destroyed per engagement and privacy requirements.
- Disclosure: Promptly report any vulnerabilities or detection gaps you uncover through responsible channels.

---

## Post-Exploitation Guidance

SILKdrop is to be used strictly in post-exploitation phases:
- Deploy only after gaining lawful access as part of an authorized assessment.
- Exfiltrate only simulation data or pre-cleared artifacts as per engagement rules.
- Share all results with the target SOC/blue team for defensive improvement.
- Do not persist, propagate, or remain after assessment—leave the environment as you found it.
- Log and document all activity for transparency and audit.

Examples of correct use:
- Simulating credential or sensitive file exfiltration as part of a purple/red team exercise.
- Helping blue teams track stealthy exfiltration and enhance detection capability.
- Conducting academic research or tool analysis under clear ethical oversight.

---

## Installation

Prerequisite: Latest Rust toolchain

curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
Clone and build

git clone https://github.com/CBMW/SilkDrop.git
cd SilkDrop
cargo build --release

text

---

## Usage

Always operate within your approved engagement scope. Run on authorized infrastructure only.

Example (after gaining validated access)

./silkdrop --mode lotl --vector dns --target "C:\SensitiveData"
./silkdrop --exfil http --cmd "whoami"

text

See `--help` for detailed usage and all available exfiltration vectors.

---

## Contributing

Contributions are welcome! Please ensure all PRs/documentation adhere to the above ethical guidelines.  
Suggest improvements, new detection-resistant modules, or enhanced blue team use cases.

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.

---

## Legal Notice

SILKdrop is developed for security professionals working responsibly, lawfully, and transparently.  
Misuse for unauthorized access, exfiltration, or criminal activity is strictly forbidden and may be reported to relevant authorities.  
All use is at your own risk.

---

Developed and maintained by [cbmw](https://github.com/cbmw), inspired by open-source best practices and the ethical security community.
