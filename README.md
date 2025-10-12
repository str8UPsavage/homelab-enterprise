Mini Enterprise HomeLab

Il progetto Mini Enterprise HomeLab nasce come esercitazione tecnica per la costruzione progressiva di una piccola infrastruttura aziendale virtuale, interamente gestita all’interno di VMware Workstation.
L’obiettivo principale è quello di comprendere in modo concreto il funzionamento dei principali servizi di rete — Active Directory, DNS, DHCP, e l’interoperabilità con sistemi Linux — riproducendo un ambiente realistico ma su scala ridotta e completamente controllata.

La rete, denominata LabNAT, è stata progettata come ambiente isolato dal sistema host, ma con accesso regolato a Internet tramite gateway NAT.
All’interno di questa infrastruttura operano attualmente due sistemi principali:

DC01, un Domain Controller Windows Server che gestisce i ruoli Active Directory, DNS e DHCP.

Ubuntu01, un server Linux configurato come membro del dominio lab.local, utilizzato per testare e studiare l’integrazione tra ambienti Windows e Unix-like.

Ogni configurazione è stata eseguita manualmente e documentata in modo dettagliato, con particolare attenzione alle motivazioni tecniche dietro ogni scelta.
Il progetto si basa su un principio preciso: tutto ciò che viene implementato deve poter essere riprodotto con risorse open-source o con strumenti liberamente accessibili.
Questa scelta permette di mantenere il laboratorio indipendente da licenze commerciali, garantendo al tempo stesso la possibilità di sperimentare in piena libertà e trasparenza.
L’utilizzo di software libero consente inoltre di estendere e adattare la struttura nel tempo, restando coerenti con l’obiettivo educativo e tecnico del progetto.

Mini Enterprise HomeLab è concepito come una piattaforma in costante evoluzione.
Ciò che oggi rappresenta un laboratorio di base, domani potrà trasformarsi in un’infrastruttura più complessa, integrando nuove funzionalità come la gestione centralizzata delle policy, l’automazione dei processi amministrativi, la simulazione di reti multi-sede o l’introduzione di sistemi di monitoraggio e sicurezza avanzati.
Ogni espansione verrà realizzata con la stessa logica metodica e documentata che caratterizza le fasi iniziali, mantenendo sempre un equilibrio tra sperimentazione e rigore tecnico.

La documentazione ufficiale del progetto, in formato .docx, accompagna questa repository e illustra in modo completo ogni procedura, configurazione e verifica.
Il presente repository GitHub rappresenta invece una panoramica sintetica e aggiornata del laboratorio, tracciandone l’evoluzione nel tempo e mantenendo un filo logico tra le varie fasi operative.

In prospettiva, Mini Enterprise HomeLab non è solo un ambiente di test: è un percorso di crescita, una piattaforma personale dove teoria e pratica si incontrano.
Un progetto costruito per essere ampliato, perfezionato e condiviso, mantenendo come principio guida la disponibilità, la trasparenza e l’utilizzo di tecnologie aperte.
