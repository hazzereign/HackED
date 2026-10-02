![Banner](./banner.jpeg)
# HackED — Advanced Network Operations Terminal
**v1.0 · Show no mercy against them.**


> **HackED** is a text-based underground network operations simulator.
>
> You are an operator. Take contracts, level up, manage your heat, plant backdoors, extract data, build your reputation, and communicate with AI-powered handlers.

<br>

> [!WARNING]
> **Everything in HackED is fictional.**
>
> No real hacking actions are performed against real-world targets. All domains, hosts, vulnerabilities, and network operations are simulated exclusively for the game.

---

## Requirements

- **Python 3.8+**
- [`requests`](https://pypi.org/project/requests/)
- [`python-whois`](https://pypi.org/project/python-whois/) — optional, but recommended for real WHOIS lookups

Install the dependencies with:

```bash
pip install requests python-whois
```

---

## Installation

### 1. Clone or download the repository

```bash
git clone <repository-url>
cd HackED
```

### 2. Configure your Groq API key

Create a file named:

```text
GROQ_API_KEY
```

Place it in the same directory as the main script and paste your Groq API key inside it.

### 3. Launch HackED

```bash
python3 hacked.py
```

On Windows, you can also use:

```powershell
py hacked.py
```

---

## First Launch

On the first execution, HackED automatically creates the following files:

| File | Purpose |
|---|---|
| `operator_profile.txt` | Your editable operator profile |
| `localStorage.json` | Balance, extraction history, and local game data |
| `savegame.json` | Created when using the `save` command |
| `GROQ_API_KEY` | Your Groq API key |

You can edit `operator_profile.txt` to customize your callsign, age, affiliation, and other operator information.

---

# Gameplay

The basic operation loop is:

```text
whois <target>
      ↓
nmap <target>
      ↓
exploit / connect
      ↓
dump / db / exfil
      ↓
wipe
```

### Typical Workflow

1. Choose a target using `servers` or `missions`.
2. Perform reconnaissance with `whois` and `nmap`.
3. Gain access using `connect`, `exploit`, or another access method.
4. Extract loot using `dump`, `db`, `extract`, `stealer`, and other commands.
5. Cover your tracks using `wipe` or `ghost`.
6. Sell your loot or complete contracts.
7. Upgrade your operator and repeat.

---

# Commands

## Reconnaissance

| Command | Description |
|---|---|
| `scan` | Scan for nearby simulated Wi-Fi networks |
| `whois <target>` | Gather target intelligence — required before attacking |
| `nmap <target>` | Scan the target's simulated ports |
| `servers [region]` | List high-value targets |
| `netmap` | Display the local network topology |
| `honeypot` | Check whether the current host is a simulated trap |

<br>

## Access

| Command | Description |
|---|---|
| `connect <target>` | Attempt to obtain a shell |
| `exploit <target>` | Automatically exploit the target |
| `brute <target> <service>` | Simulated brute-force attack against SSH/FTP/RDP/etc. |
| `zeroday <target>` | Use an expensive zero-day exploit |
| `phish <domain>` | Launch a simulated phishing campaign |
| `inject <target>` | Simulate SQLi/RCE exploitation |

<br>

## Post-Exploitation

> Most post-exploitation commands require an active shell.

| Command | Description |
|---|---|
| `dump` / `db` | Extract simulated credentials and databases |
| `exfil` | Exfiltrate simulated data |
| `extract` | Extract simulated funds from the target |
| `backdoor` | Plant a persistent simulated backdoor |
| `rootkit` | Hide your simulated presence |
| `lateral` / `hop` | Perform simulated lateral movement |
| `mitm` | Simulate ARP/SSL interception |
| `ransom` | Deploy simulated ransomware |
| `deface` | Deface the simulated website |
| `shell` | Open an interactive simulated shell |

<br>

## Offensive & OPSEC

| Command | Description |
|---|---|
| `ddos <target>` | Simulate a botnet flood |
| `raid <region>` | Perform a mass raid — requires 50+ nodes |
| `wipe` | Reduce your heat |
| `ghost` | Enter Ghost Mode with reduced heat generation |
| `proxy` / `tor` | Rotate your simulated proxy/Tor identity |
| `botnet grow` | Expand your simulated botnet |

<br>

## Economy & Progression

| Command | Description |
|---|---|
| `missions` | Open the contract board |
| `shop` / `shop buy` | Access the darkweb shop |
| `sell` | Sell extracted loot |
| `wallet` / `loot` | View your wallet and inventory |
| `status` | Display your complete operator status |
| `achievements` | View unlocked achievements |
| `save` / `load` | Save or load your progress |
| `news` | Read the underground news feed and world events |

---

# AI Handlers

HackED features AI-powered handlers that communicate with the player through the Groq API.

The handlers are powered by a **Qwen-based model** and each one has its own personality and approach to operations.

## Handler Commands

| Command | Description |
|---|---|
| `agent` | Open a communication channel with the active handler |
| `agent list` | List available handlers |
| `agent <name>` | Switch to another handler |

### Available Handlers

| Handler | Personality |
|---|---|
| **Shadow** | Cold, professional, and results-oriented |
| **Ghost** | Tactical and focused on concrete steps |
| **Viper** | Aggressive and obsessed with body count |
| **Neon** | High-energy and constantly hyped |
| **Zero** | Minimalistic and focused exclusively on intelligence |

<br>

### Example

```text
> agent

[SHADOW] Channel established.
[SHADOW] You have a new contract.

> agent ghost

[GHOST] Handler switched.
[GHOST] Let's make this clean.
```

A valid `GROQ_API_KEY` is required to use the AI handlers.

---

# Progression Systems

HackED features multiple progression systems designed to make each operation affect your operator's development.

### Level & XP

Gain XP through operations and missions.

Higher levels unlock new abilities and improve existing ones, such as:

- Longer Ghost Mode duration
- Faster scans
- Better operational capabilities
- Access to advanced tools

### Reputation

Your reputation affects the underground economy and unlocks additional achievements.

Higher reputation can provide:

- Better selling prices
- Access to new contracts
- Additional achievements
- Increased standing within the underground network

### Streak

Maintain an operation streak without getting detected to receive bonuses.

### Heat

**Heat** represents how much attention your operator is attracting.

Loud operations increase heat.

High heat can result in:

```text
WARNING
Target security response detected.

HEAT: ████████████████ 92%

LOCKDOWN INITIATED
```

Use `wipe` and `ghost` to reduce or manage your heat.

### Missions

Complete contracts to earn:

- XP
- Reputation
- BTC
- Special rewards

### Achievements

Unlock permanent trophies by completing special objectives.

### Inventory

Collect and use different simulated items, including:

- Smoke bombs
- Exploit kits
- Specialized tools
- Other operational equipment

---

# Economy

HackED features an underground economy centered around simulated BTC, USD, loot, and contracts.

Your earnings can be used to purchase upgrades, tools, exploits, and other items.

The basic economic loop is:

```text
OPERATE
   ↓
EXTRACT
   ↓
SELL
   ↓
UPGRADE
   ↓
OPERATE AGAIN
```

---

# Save System

HackED provides a local save system.

Use:

```text
save
```

to create/update your save file.

Load your progress with:

```text
load
```

The save system stores your progression, inventory, economy, reputation, and other game state.

---

# Generated Files

| File | Function |
|---|---|
| `operator_profile.txt` | Editable operator profile |
| `localStorage.json` | USD/BTC balance and extraction history |
| `savegame.json` | Complete game save |
| `GROQ_API_KEY` | Groq API authentication key |

> **Keep `GROQ_API_KEY` private. Never commit it to Git.**

Add it to your `.gitignore`:

```gitignore
GROQ_API_KEY
localStorage.json
savegame.json
```

---

# Quick Tips

```text
[01] Always perform whois → nmap before attacking.

[02] Use wipe and ghost when your heat gets high.

[03] Complete missions to farm reputation and BTC.

[04] Zero-days are expensive, but significantly quieter.

[05] Build your botnet before attempting large-scale raids.

[06] Save frequently using the save command.

[07] Different handlers provide different approaches to operations.
```

---

# Example Session

```text
╔══════════════════════════════════════════╗
║            HACKED // TERMINAL            ║
╚══════════════════════════════════════════╝

> servers

[SERVER BOARD]
01. BLACKSITE-07
02. CYBERDYNE-NODE
03. SWIFT-NET
04. WORLD-BANK-SIM

> whois BLACKSITE-07

[WHOIS]
Target: BLACKSITE-07
Status: ONLINE
Security: HIGH
Value: ████████░░

> nmap BLACKSITE-07

[NMAP]
22/tcp    SSH
80/tcp    HTTP
443/tcp   HTTPS
3306/tcp  MYSQL

> exploit BLACKSITE-07

[+] Exploit successful.
[+] Shell acquired.

> dump

[DATABASE]
Credentials extracted.
Files discovered.
Financial records located.

> exfil

[+] Data successfully extracted.

> status

OPERATOR
────────────────────────
LEVEL:      12
XP:         7,450
REP:        1,830
BTC:        0.42
HEAT:       38%
STREAK:     7
────────────────────────

> ghost

[GHOST MODE]
Heat generation reduced.
Operator presence masked.

> save

[+] Game saved.
```

---

# Disclaimer

HackED is a **fictional text-based simulation game**.<br>

No real vulnerabilities are exploited, no real systems are attacked, and no real-world network operations are performed by the game.<br>

All targets, domains, vulnerabilities, credentials, financial systems, and network infrastructure represented in the game are fictional elements of the HackED universe.<br>

Some names may resemble real-world organizations or services, but they are used strictly as fictional placeholders within the simulation.<br>

**Do not use this software for unauthorized or illegal activities.**

<br>

```text
███████╗████████╗ █████╗ ██╗   ██╗
██╔════╝╚══██╔══╝██╔══██╗██║   ██║
█████╗     ██║   ███████║██║   ██║
██╔══╝     ██║   ██╔══██║██║   ██║
███████╗   ██║   ██║  ██║╚██████╔╝
╚══════╝   ╚═╝   ╚═╝  ╚═╝ ╚═════╝

STAY IN THE DARK.
OPERATOR.
```
