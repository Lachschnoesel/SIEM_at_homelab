# 🧪 Homelab Detection Engineering Lab

Ein kleines, aber leistungsfähiges Homelab zur Emulation von Angriffen und Entwicklung von Erkennungsmechanismen. Ziel ist es, in einem kontrollierten Umfeld adversariale Aktivitäten zu simulieren, um Detektionen zu testen, Angriffe zu blockieren und False Positives zu analysieren.

---

## 🔧 Setup

Das Lab besteht aus zwei kleinen virtuellen Maschinen:

- **Attacker-VM:** Führt simulierte Angriffe aus Payloads
- **Defender-VM:** Beinhaltet Logging, Detection Rules und YARA-Scanner.

> Virtualisierung = VMware.

---

## 🎭 Adversary Emulation

Hier versetzen wir uns in die Rolle eines Angreifers:

- Nutzung bekannter Angriffstechniken (MITRE ATT&CK)
- Erstellung und Ausführung von Payloads

---

## 🔍 Detection Engineering

Auf der Defender-VM wird untersucht, ob und wie Angriffe erkannt werden:

- Erstellung & Test von **YARA-Regeln**
- Analyse mit Tools wie **Sysmon**
- Einbindung von **LimaCharlie** für Thread Detection

---

## 🚫 Blocking Measures

Nach dem Erkennen folgt das Blockieren:

- Windows Defender Policies
- Firewall-Regeln oder Network Segmentation
- Test auf Umgehbarkeit

---

## 🎯 Tuning False Positives

Um die Qualität der Regeln zu verbessern:

- Identifikation & Dokumentation von False Positives
- Regelanpassung und Retesting
- Ziel: Präzise, aber wirksame Detektion

---

## 🔎 Beispiel: YARA-Trigger

```yara
rule Suspicious_Payload
{
    meta:
        description = "Erkennt simplen Dropper"
    strings:
        $a = "powershell -enc"
    condition:
        $a
}
