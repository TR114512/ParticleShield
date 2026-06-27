# ParticleShield — The World's Strongest Open-Source Free Minecraft Firewall

* * *

## What Is ParticleShield

ParticleShield is a **free, open-source, all-in-one enterprise-grade firewall** purpose-built for Minecraft Java Edition Paper 1.21.11 servers. It is far more than an anti-cheat plugin — it is a complete security ecosystem encompassing anti-cheat, exploit protection, anti-bot, anti-VPN/proxy, intelligent firewall, threat intelligence, forensic analysis, real-time monitoring, and row-level data security. ParticleShield integrates **58 protection modules** with **56 international language** translations, and is widely regarded as the most powerful open-source free Minecraft security solution known today.

Whether you run a small survival server, a large-scale proxy network, a minigame hub, or a commercial RPG server, ParticleShield delivers enterprise-grade protection at zero cost. From basic KillAura detection to the most sophisticated Netty protocol-layer buffer attacks, from simple IP blacklists to a machine-learning-powered anomaly detection engine — ParticleShield packs the entire security stack into a single 35MB JAR.

* * *

## 58 Protection Modules — Full Attack Surface Coverage

ParticleShield's defense architecture revolves around four core engines, comprising 58 protection modules that span the complete attack chain from the network layer to the application layer:

### Anti-Cheat Engine (10 Checks)

Powered by the GrimAC processor, the anti-cheat system provides 10 precision checks: AimDuplicateLook, AimModulo360, KillAura, AntiKB, Critical, Fly, Speed, Reach, Timer, InvalidPitch, and BlockBreak — covering aiming, combat, movement, player behavior, and world interaction across five dimensions, with false-positive rates optimized to below 8%.

### AstraGuard Exploit Protection Engine (30+ Sub-Modules)

ParticleShield's flagship exploit protection system, featuring 30+ exploit mitigation modules that cover virtually every known crash and duplication vulnerability in Minecraft history: Netty packet size limits, byte rate limits, packet rate limits, flood attack detection, the full Crasher/Dupe vulnerability family (NBT crash, sign crash, lectern crash, map label crash, item frame crash), creative mode item fixes, inventory duplication fixes, mule duplication fixes, bundle duplication fixes, portal break fixes, explosion limiters, falling block limiters, piston limiters, movement security, visual crash protection (fireworks/particles), command crash mitigation (//calc, //eval, and more), offline packet duplication fixes, and advanced duplication protection (portals/shulker boxes).

### Anti-Bot Detection (8 Progressive Layers)

An eight-layer progressive detection architecture combining connection rate, ping handshake, username entropy analysis, protocol compliance checks, first-join behavior analysis, gravity behavior detection, packet timing analysis, and post-join behavior analysis. Players are acted upon by score threshold — allow, delay, kick, or blacklist. With async processing, TPS impact drops from 2 TPS to just 1 TPS.

### Anti-VPN & IP Reputation System (7-Layer Filter Chain)

Whitelist → Manual Blacklist → GitHub Public Proxy List → CIDR Range Blocking → ASN Autonomous System Blocking (OVH/Hetzner/DigitalOcean/Alibaba Cloud) → External API checks (proxycheck.io) → Fallback API polling — a seven-layer serial filter chain ensures proxy and VPN traffic has nowhere to hide.

### Intelligent Firewall (MAF Firewall)

The built-in MAF Firewall provides traditional firewall capabilities including IP whitelisting/blacklisting, geographic region control, world routing, and connection limits, forming a defense-in-depth architecture alongside the anti-VPN system.

* * *

## Enterprise-Grade Integrated Protection

### Threat Intelligence Engine

ParticleShield features a built-in EWMA adaptive detection engine and Isolation Forest anomaly detection algorithm (150 isolation trees), capable of analyzing server traffic patterns in real time and automatically identifying new types of attacks without predefined rules. Combined with the Token Bucket algorithm (6 rate buckets), it achieves precise traffic shaping and rate limiting.

### Punishment System (LightBans)

Integrated with the LightBans punishment framework, supporting 10 punishment types: Ban, TempBan, IPBan, Mute, TempMute, MuteIP, Kick, SoftBan, Blacklist, and Warn. Punishment records are strictly isolated through RLS row-level security policies.

### Trust Score System

A dynamic player trust scoring system that holistically evaluates player behavior patterns, influencing bypass thresholds for attack pattern detection, bot detection, and VPN detection, delivering personalized security policies unique to each player.

### Forensic Analysis

An end-to-end forensic analysis pipeline supporting attack snapshot capture, packet recording and replay, and JSON-format export, enabling administrators to retrospectively analyze any security incident. Forensic data is protected by independent permission nodes, with every access written to the audit log.

### Honeypot & Panic Mode

A built-in decoy Minecraft server honeypot (port 25566) actively lures and fingerprints attackers. Administrators can trigger emergency mode at any time via the `/panic` command, instantly activating the server's maximum protection level.

* * *

## 56 Languages — Truly Global

ParticleShield supports complete localization in **56 languages**, covering Arabic, Chinese, English, French, German, Japanese, Korean, Russian, Spanish, Portuguese, and major global language families, plus Afrikaans, Azerbaijani, Belarusian, Bengali, Bosnian, Catalan, Czech, Danish, Estonian, Persian, Finnish, Galician, Georgian, Greek, Hebrew, Hindi, Croatian, Hungarian, Indonesian, Italian, Kazakh, Khmer, Lao, Lithuanian, Latvian, Macedonian, Mongolian, Malay, Burmese, Norwegian, Nepali, Dutch, Polish, Brazilian Portuguese, Romanian, Sinhala, Slovak, Slovenian, Serbian, Swedish, Thai, Filipino, Turkish, Ukrainian, Urdu, Vietnamese, and more. No matter where your players come from, they experience the full security feature set in their native language.

* * *

## Observability & Operational Automation

ParticleShield v3.0.1 introduces a complete observability stack:

* **Prometheus Metrics Export**: Real-time exposure of key metrics including DDoS detection, bot surges, TPS fluctuations, and connection counts
* **Grafana Dashboard**: A 9-panel visual security dashboard covering attack trends, threat levels, and performance monitoring
* **10 Pre-Configured Alert Rules**: Automatic notification triggers for DDoS attacks, bot surges, abnormal TPS drops, and more
* **Triple-Channel Notifications**: Discord, Telegram, and Slack synchronized security event push

On the operations side, ParticleShield ships with Aikar's JVM-optimized startup flags, automatic crash restart (up to 3 retries), automatic OOM heap dumps, GC log rotation (7-day retention), daily configuration backups, and 30-day auto-cleanup — all wrapped in ready-to-use automation scripts covering both Windows (.bat) and Linux (.sh) platforms.

* * *

## Authentication & Data Security

ParticleShield's Web management panel employs the Argon2id password hashing algorithm (the 2022 Password Hashing Champion, configured with m=65536KB, t=3, p=4, 16-byte random salt), combined with JWT token authentication (30-minute auto-expiry), default 127.0.0.1 binding policy, and CORS local-origin restrictions — building an OWASP-recommended authentication perimeter. At the database level, RLS row-level security policies enforce punishment record isolation by enforcer, trust score isolation by player, independent authorization for forensic snapshot access, and intelligent IP log masking. Every sensitive data read is recorded in an audit log with a 90-day retention period.

* * *

## Completely Free, Completely Open-Source

ParticleShield is licensed under the MIT License — **permanently free, with no paywalls and no feature locks**. All 58 protection modules, 56 languages, Grafana monitoring dashboards, RLS row-level security, and operational automation scripts are fully available. The community is free to audit every line of code, freely modify it to suit their own needs, and freely redistribute it — this is the core of our commitment to open-source security.
