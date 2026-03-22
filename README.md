<div align="center">

<!-- ANIMATED HEADER -->
<img src="https://capsule-render.vercel.app/api?type=waving&color=00ff41&height=200&section=header&text=FIXTT&fontSize=80&fontColor=000000&animation=fadeIn&fontAlignY=38&desc=Advanced+Open+Source+Intelligence+Framework&descAlignY=60&descSize=18&descColor=000000" width="100%"/>

<!-- TYPING ANIMATION -->
<a href="https://git.io/typing-svg">
  <img src="https://readme-typing-svg.demolab.com?font=Share+Tech+Mono&size=22&pause=1000&color=00FF41&center=true&vCenter=true&width=600&lines=OSINT+Framework+%7C+20%2B+Modules;IP+%C2%B7+Email+%C2%B7+DNS+%C2%B7+Dark+Web;Red+Team+%7C+Bug+Bounty+%7C+CTF;Ethical+Hacking+Only+%E2%80%94+Stay+Legal" alt="Typing SVG" />
</a>

<br/><br/>

<!-- BADGES -->
![Python](https://img.shields.io/badge/Python-3.8%2B-00ff41?style=for-the-badge&logo=python&logoColor=00ff41&labelColor=0d1117)
![Platform](https://img.shields.io/badge/Linux%20%7C%20Termux%20%7C%20macOS-supported-00ff41?style=for-the-badge&logo=linux&logoColor=00ff41&labelColor=0d1117)
![Version](https://img.shields.io/badge/Version-2.3-00cfff?style=for-the-badge&labelColor=0d1117)
![Security](https://img.shields.io/badge/Hardened-v7.1-ff2d2d?style=for-the-badge&logo=shield&labelColor=0d1117)
![License](https://img.shields.io/badge/License-MIT-gray?style=for-the-badge&labelColor=0d1117)
![Ethics](https://img.shields.io/badge/Authorized_Use_Only-⚠️-ff2d2d?style=for-the-badge&labelColor=0d1117)

</div>

---

## 🌐 What is FIXTT?

**FIXTT** is a modular, terminal-based Open Source Intelligence framework designed for security researchers, red teamers, and CTF players. It aggregates intelligence from **20+ data sources** into a single unified CLI — phones, emails, IPs, domains, images, dark web, and more.

Actively maintained and security-hardened by **[krypthane](https://github.com/wavegxz-design)** — Red Team Operator from Mexico 🇲🇽.

---

## 🎬 Demo

<div align="center">

| Installation | ProtonMail OSINT |
|:---:|:---:|
| ![Install](Demo/install.gif) | ![ProtonMail](Demo/protonmail-osint.gif) |

</div>

---

## 🧩 Modules

```
╔══════════════════════════════════════════════════════╗
║                  FIXTT  v2.3                      ║
╠═══════════════════════╦══════════════════════════════╣
║  [01] IP Address Info ║  [11] Metadata Extraction   ║
║  [02] Email Info      ║  [12] Twitter Status Check  ║
║  [03] Image Location  ║  [13] Subdomain Enum        ║
║  [04] Host Search     ║  [14] Google Dork Hacking   ║
║  [05] Port Scanner    ║  [15] SMTP Analysis         ║
║  [06] Exploit CVE     ║  [16] InfoStealer Check     ║
║  [07] Exploit OSVD    ║  [17] Dark Web Search       ║
║  [08] DNS Lookup      ║  [99] Auto-Update           ║
║  [09] DNS Reverse     ║  [101] What's New?          ║
║  [10] Email Finder    ║  [100] About                ║
╚═══════════════════════╩══════════════════════════════╝
```

---

## 🔒 Security Hardening — v7.1

> Audit and patches applied by **krypthane**

| # | Issue | Severity | Fix |
|---|-------|----------|-----|
| 1 | Stripe API key hardcoded in source | 🔴 HIGH | Moved to `STRIPE_API_KEY` env var |
| 2 | `shell=True` in `run_command()` | 🟡 MED | `shlex.split()` + `shell=False` + timeout |
| 3 | `shell=True` in Tor service check | 🟡 MED | Split into safe separate calls |
| 4 | `git reset --hard` without confirmation | 🟡 MED | Explicit `yes` prompt required |

---

## 🚀 Installation

<details>
<summary><b>🐧 Linux — Kali / Parrot / Ubuntu</b></summary>

```bash
git clone https://github.com/wavegxz-design/FIXTT
cd FIXTT
chmod +x setup.sh
sudo bash setup.sh
```

</details>

<details>
<summary><b>📱 Termux — Android</b></summary>

```bash
git clone https://github.com/wavegxz-design/FIXTT
cd FIXTT
bash setup.sh
```

</details>

<details>
<summary><b>🍎 macOS</b></summary>

```bash
git clone https://github.com/wavegxz-design/FIXTT
cd FIXTT
bash setup.sh
```

</details>

---

## ⚙️ Configuration

Set your API keys as environment variables — **never hardcode secrets**:

```bash
# Add to ~/.bashrc or ~/.zshrc
export STRIPE_API_KEY="sk_test_..."        # Optional — payment support
export OPENCAGE_API_KEY="your_key"         # Optional — IP geolocation
export GOOGLE_CSE_API_KEY="your_key"       # Optional — reverse image search
export GOOGLE_CSE_ENGINE_ID="your_id"      # Optional — reverse image search
```

---

## 🖥️ Usage

```bash
xosint
# or
python3 xosint
```

---

## 🤝 Contributing

Contributions are welcome. Please follow the security guidelines below.

```bash
# 1. Fork the repo
git fork https://github.com/wavegxz-design/FIXTT

# 2. Create your feature branch
git checkout -b feat/module-name

# 3. Commit with clear message
git commit -m "feat: add [module-name] — brief description"

# 4. Open a Pull Request
git push origin feat/module-name
```

**Security checklist before submitting PR:**
- [ ] No hardcoded API keys, tokens or passwords
- [ ] No `shell=True` with user-controlled input
- [ ] No calls to undisclosed external servers
- [ ] Tested on Linux and Termux
- [ ] Module added to README module map

> ⚠️ PRs with backdoors, obfuscated code, or malicious logic will be rejected and reported.

---

## ⚠️ Legal Disclaimer

```
This tool is for AUTHORIZED security research and educational purposes ONLY.

✅  Authorized penetration testing
✅  CTF competitions
✅  Personal security research
✅  Bug bounty programs (within scope)

❌  Unauthorized access to systems or accounts
❌  Stalking, harassment or privacy violations
❌  Any illegal activity under local or international law

The author assumes NO responsibility for misuse of this tool.
```

---

## 👤 Author & Maintainer

<div align="center">

| | |
|:---:|:---|
| <img src="https://github.com/wavegxz-design.png" width="90" style="border-radius:50%"/> | **krypthane** — Red Team Operator & Open Source Developer<br/>📍 Mexico 🇲🇽 · UTC-6<br/>*"Know the attack to build the defense."* |

<br/>

[![GitHub](https://img.shields.io/badge/GitHub-wavegxz--design-00ff41?style=for-the-badge&logo=github&labelColor=0d1117)](https://github.com/wavegxz-design)
[![Telegram](https://img.shields.io/badge/Telegram-Skrylakk-00cfff?style=for-the-badge&logo=telegram&labelColor=0d1117)](https://t.me/Skrylakk)
[![Email](https://img.shields.io/badge/Email-Workernova@proton.me-ff2d2d?style=for-the-badge&logo=protonmail&labelColor=0d1117)](mailto:Workernova@proton.me)
[![Portfolio](https://img.shields.io/badge/Portfolio-krypthane-00ff41?style=for-the-badge&logo=cloudflare&labelColor=0d1117)](https://krypthane.workernova.workers.dev)

</div>

---

## ⭐ Support

If FIXTT helped you in a CTF, bug bounty, or research — drop a ⭐  
It helps the project reach more security researchers.

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=00ff41&height=120&section=footer&fontColor=000000&animation=fadeIn&text=krypthane+%C2%B7+wavegxz-design+%C2%B7+Ethical+Hacking+Only" width="100%"/>

</div>
