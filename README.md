<div align="center">

```
██╗  ██╗      ██████╗ ███████╗██╗███╗   ██╗████████╗
╚██╗██╔╝     ██╔═══██╗██╔════╝██║████╗  ██║╚══██╔══╝
 ╚███╔╝█████╗██║   ██║███████╗██║██╔██╗ ██║   ██║   
 ██╔██╗╚════╝██║   ██║╚════██║██║██║╚██╗██║   ██║   
██╔╝ ██╗     ╚██████╔╝███████║██║██║ ╚████║   ██║   
╚═╝  ╚═╝      ╚═════╝ ╚══════╝╚═╝╚═╝  ╚═══╝   ╚═╝  
```

<img src="images/X-osintv2.2.png" alt="X-OSINT Banner" width="800"/>

---

![Python](https://img.shields.io/badge/Python-3.8%2B-00ff41?style=for-the-badge&logo=python&logoColor=00ff41&labelColor=000a00)
![Platform](https://img.shields.io/badge/Platform-Linux%20%7C%20Termux%20%7C%20macOS-00ff41?style=for-the-badge&labelColor=000a00)
![License](https://img.shields.io/badge/License-MIT-ff2d2d?style=for-the-badge&labelColor=000a00)
![Version](https://img.shields.io/badge/Version-2.3-00cfff?style=for-the-badge&labelColor=000a00)
![Security](https://img.shields.io/badge/Security_Hardened-v7.1-00ff41?style=for-the-badge&labelColor=000a00)
![Ethics](https://img.shields.io/badge/Authorized_Use_Only-⚠️-ff2d2d?style=for-the-badge&labelColor=000a00)

<br/>

> **Advanced Open Source Intelligence Framework**  
> *Gather intelligence. Stay ethical. Leave no trace.*

</div>

---

## ⚡ What is X-OSINT?

**X-OSINT** is a modular, terminal-based OSINT framework built for security researchers, red teamers, and investigators.  
It aggregates intelligence from 20+ sources into a single unified interface — phones, emails, IPs, domains, images, dark web, and more.

Maintained and security-hardened by **[krypthane](https://github.com/wavegxz-design)** — Red Team Operator, Mexico 🇲🇽.

---

## 🧩 Module Map

```
┌─────────────────────────────────────────────────────────────────┐
│                        X-OSINT  v2.3                           │
├──────────────────────────┬──────────────────────────────────────┤
│  [01] IP Address Info    │  [11] Metadata Extraction  [NEW]    │
│  [02] Email Address Info │  [12] Twitter Status Check          │
│  [03] Image Location     │  [13] Subdomain Enumeration         │
│  [04] Host Search        │  [14] Google Dork Hacking           │
│  [05] Port Scanner       │  [15] SMTP Analysis                 │
│  [06] Exploit CVE        │  [16] InfoStealer Attack Check      │
│  [07] Exploit O.S.V.D    │  [17] Dark Web Search               │
│  [08] DNS Lookup         │  [99] Auto-Update (confirmed)       │
│  [09] DNS Reverse        │  [100] About                        │
│  [10] Email Finder       │  [101] What's New?                  │
└──────────────────────────┴──────────────────────────────────────┘
```

---

## 🔒 Security Hardening — v7.1

> Security audit and patches applied by **krypthane**

| # | Vulnerability | Severity | Status |
|---|---------------|----------|--------|
| 1 | Stripe API key hardcoded in source | 🔴 HIGH | ✅ Fixed — moved to `STRIPE_API_KEY` env var |
| 2 | `shell=True` in `run_command()` — shell injection risk | 🟡 MED | ✅ Fixed — `shlex.split()` + `shell=False` |
| 3 | `shell=True` in Tor check — command chaining risk | 🟡 MED | ✅ Fixed — split into safe list calls |
| 4 | Auto-update `git reset --hard` without confirmation | 🟡 MED | ✅ Fixed — explicit `yes` prompt required |

---

## 🚀 Installation

### Linux / Kali / Parrot
```bash
git clone https://github.com/wavegxz-design/X-osint
cd X-osint
chmod +x setup.sh
sudo bash setup.sh
```

### Termux (Android)
```bash
git clone https://github.com/wavegxz-design/X-osint
cd X-osint
bash setup.sh
```

### macOS
```bash
git clone https://github.com/wavegxz-design/X-osint
cd X-osint
bash setup.sh
```

---

## ⚙️ Configuration

Before running, set your API keys as environment variables — **never hardcode them**:

```bash
# Required only for payment support (optional)
export STRIPE_API_KEY="sk_test_..."

# Optional — enhances IP geolocation
export OPENCAGE_API_KEY="your_key_here"

# Optional — reverse image search
export GOOGLE_CSE_API_KEY="your_key_here"
export GOOGLE_CSE_ENGINE_ID="your_engine_id"
```

Add to `~/.bashrc` or `~/.zshrc` to persist across sessions.

---

## 🖥️ Usage

```bash
# Standard run
xosint

# Or directly
python3 xosint
```

```
[krypthane@x-osint ~]$ xosint

██╗  ██╗      ██████╗ ███████╗██╗███╗   ██╗████████╗
╚██╗██╔╝     ██╔═══██╗██╔════╝██║████╗  ██║╚══██╔══╝
...

[??] Choose an option:
[1] IP Address Info
[2] Email Address Info
[3] Extract Location from Image
...
```

---

## 📋 Requirements

<details>
<summary>Click to expand full dependency list</summary>

```
requests · flask · beautifulsoup4 · phonenumbers · pillow
piexif · cryptography · colorama · prompt_toolkit · folium
opencage · googlesearch-python · stripe · scapy · ping3
google-api-python-client · python-whois · python-dotenv
qrcode · vininfo · imdbpy · rich · and more...
```

Install all at once:
```bash
pip install -r requirements.txt
```

</details>

---

## 📸 Demo

<div align="center">

| Install | Protonmail OSINT |
|---------|-----------------|
| ![Install](Demo/install.gif) | ![Protonmail](Demo/protonmail-osint.gif) |

</div>

---

## ⚠️ Legal Disclaimer

```
This tool is provided for educational and authorized security research purposes ONLY.

✅ Authorized penetration testing
✅ CTF competitions  
✅ Personal security research
✅ Bug bounty programs (within scope)

❌ Unauthorized access to systems or accounts
❌ Stalking, harassment, or privacy violations
❌ Any illegal activity under local or international law

The author (krypthane) assumes NO responsibility for misuse.
Usage implies full acceptance of this disclaimer.
```

---

## 🤝 Contributing

```bash
# 1. Fork the repo
# 2. Create your feature branch
git checkout -b feature/new-module

# 3. Commit with clear message
git commit -m "feat: add [module-name] OSINT module"

# 4. Push and open a Pull Request
git push origin feature/new-module
```

**Before submitting PR:**
- [ ] No hardcoded API keys or secrets
- [ ] No `shell=True` with user-controlled input  
- [ ] Code tested on Linux and Termux
- [ ] Added to module map in README

---

## 📡 Contact & Author

<div align="center">

| Platform | Link |
|----------|------|
| 🐙 **GitHub** | [github.com/wavegxz-design](https://github.com/wavegxz-design) |
| ✈️ **Telegram** | [t.me/Skrylakk](https://t.me/Skrylakk) |
| 📧 **Email** | [Workernova@proton.me](mailto:Workernova@proton.me) |
| 🌐 **Portfolio** | [krypthane.workernova.workers.dev](https://krypthane.workernova.workers.dev) |
| 📍 **Location** | Mexico 🇲🇽 UTC-6 |

</div>

---

## ⭐ Support

If X-OSINT helped you in a CTF, bug bounty, or research — drop a ⭐ on the repo.  
It helps the project grow and reach more security researchers.

---

<div align="center">

```
// krypthane · wavegxz-design · RED TEAM OPERATOR · ETHICAL HACKING ONLY //
```

*"Know the attack to build the defense."*

</div>
