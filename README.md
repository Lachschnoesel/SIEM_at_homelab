# 🧪 Homelab Detection Engineering Lab

Ein kleines, aber leistungsfähiges Homelab zur Emulation von Angriffen und Entwicklung von Erkennungsmechanismen. Ziel ist es, in einem kontrollierten Umfeld adversariale Aktivitäten zu simulieren, um Detektionen zu testen, Angriffe zu blockieren und False Positives zu analysieren.

---

## 🔧 Setup

Das Lab besteht aus zwei kleinen virtuellen Maschinen:

- **Attacker-VM:** Führt simulierte Angriffe aus Payloads
- **Defender-VM:** Beinhaltet Logging, Detection Rules und YARA-Scanner.

> Virtualisierung = Mit VMware

---

## 🎭 Adversary Emulation

Hier versetzen wir uns in die Rolle eines Angreifers:

- Nutzung bekannter Angriffstechniken (MITRE ATT&CK)
- Erstellung und Ausführung von Payloads mithilfe von SLIVER C2

---

## 🔍 Detection Engineering

Auf der Defender-VM wird untersucht, ob und wie Angriffe erkannt werden:

- Erstellung & Test von **YARA-Regeln**
- Analyse der Prozesse und Logs mit LimaCharlie
- Einbindung von LimaCharlie für Thread Detection

