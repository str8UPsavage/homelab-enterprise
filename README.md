# homelab-enterprise
Enterprise homelab project focused on core infrastructure setup and configuration. Includes Active Directory, DHCP, and network services as part of the “homework” environment for building and testing enterprise-like systems. Still work in progress.
---

# 🧠 Mini Enterprise HomeLab (Work in Progress)

*Status:* 🔧 Progetto in corso  
*Virtualization Platform:* VMware Workstation  
*Objective:* Creare un’infrastruttura aziendale virtuale completa per esercitarsi con Active Directory, DNS, DHCP e integrazione Linux/Windows in un ambiente simulato.

---

## ⚙ Panoramica del progetto

Il *Mini Enterprise HomeLab* è un laboratorio virtuale progettato per replicare un’infrastruttura IT aziendale base.  
L’obiettivo è imparare a gestire reti ibride (Windows + Linux), servizi di directory, DNS interni, DHCP, e successive integrazioni (come SMB, join di sistemi Linux, ecc.).

Attualmente il progetto è *in sviluppo attivo*: la parte Windows è completata, quella Linux è in preparazione.

---

## 🧩 Architettura di rete attuale

*Tipo di rete:* NAT VMware (VMnet8)  
*Subnet:* 192.168.149.0/24  
*Gateway NAT:* 192.168.149.2  
*DNS / Dominio interno:* lab.local

| Macchina | Ruolo | IP | Sistema Operativo | Stato |
|-----------|--------|----|------------------|--------|
| *DC01* | Domain Controller, DNS, DHCP | 192.168.149.10 | Windows Server 2022 Datacenter | ✅ Configurato |
| *Ubuntu01* | Linux Server (integrazione AD / test servizi) | 192.168.149.20 | Ubuntu Server 22.04 LTS | ⏳ Da configurare |
| *FileSRV01* | File Server (SMB Share) | 192.168.149.30 | TBD | ⏳ Previsto |

---

## 🖥 Configurazione VMware

- *Virtual Network (VMnet8):*
  - NAT abilitato, subnet 192.168.149.0/24
  - Gateway virtuale 192.168.149.2
  - DHCP locale disattivato (gestito da DC01)
- *DC01:*
  - CPU: 2 vCore
  - RAM: 4 GB
  - Disco: 60 GB (SCSI)
  - Rete: VMnet8 (NAT)
  - DNS interno: 192.168.149.10
- *Ubuntu01 (previsto):*
  - IP statico: 192.168.149.20
  - Gateway: 192.168.149.2
  - DNS: 192.168.149.10

---

## 🧱 Servizi implementati finora

| Servizio | Descrizione | Stato |
|-----------|-------------|--------|
| *Active Directory (AD DS)* | Dominio lab.local configurato e operativo | ✅ |
| *DNS Server* | Zone forward/reverse integrate in AD | ✅ |
| *DHCP Server* | Scope 192.168.149.100–200 (client range) | ✅ |
| *Gateway NAT* | Accesso Internet tramite VMware NAT | ✅ |
| *Linux Integration* | Join dominio e test comunicazione | 🚧 In sviluppo |

---

## 🔍 Test effettuati

- ✅ Risoluzione DNS interna (dc01.lab.local)
- ✅ Ping e tracert verso Internet (NAT funzionante)
- ✅ DHCP attivo e autorizzato in Active Directory
- ✅ Connessione Internet del DC01 stabile
- 🕓 In preparazione: test join Ubuntu01 → dominio lab.local

---

## 🚀 Step successivi

1. Installazione e configurazione *Ubuntu01 (192.168.149.20)*  
   - IP statico, DNS interno, join dominio tramite realmd/sssd  
2. Creazione di *FileSRV01 (192.168.149.30)* con SMB share centralizzato  
3. Test di autenticazione cross-platform (Windows ↔ Linux)  
4. Documentazione tecnica finale e diagramma aggiornato (Draw.io)

---

## 🧾 Note finali

Questo progetto è in costante evoluzione.  
Attualmente è online solo la prima fase (infrastruttura base Windows).  
Le prossime release aggiungeranno l’integrazione Linux, automazione Ansible e gestione centralizzata dei servizi.

---

📅 *Aggiornamento:* Ottobre 2025  
📍 *Stato:* Fase 1 completata – Active Directory + DNS + DHCP pienamente operativi


---
