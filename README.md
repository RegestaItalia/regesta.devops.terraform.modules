# Terraform per SAP BTP - Regesta Italia

Questo repository è il punto centrale per **moduli Terraform riutilizzabili** e **cookbooks** (ricette complete) sviluppati da Regesta Italia per l'automazione e la gestione di risorse SAP BTP, Cloud Foundry e servizi correlati.

## 📦 Cosa Trovi Qui

### 🧩 Moduli Terraform
Componenti atomici e riutilizzabili per il provisioning di singole risorse SAP BTP. Ogni modulo gestisce un servizio o risorsa specifica ed è progettato per essere combinato con altri moduli.

**[📖 Esplora i Moduli](#elenco-moduli-disponibili)**

### 🍳 Cookbooks Terraform
Ricette complete che orchestrano più moduli per implementare architetture end-to-end e scenari complessi. Soluzioni pronte all'uso per casi d'uso specifici.

**[📖 Vai ai Cookbooks](https://github.com/RegestaItalia/regesta.devops.terraform.cookbooks)**

## 🔧 Moduli vs Cookbooks

| Aspetto | Moduli | Cookbooks |
|---------|---------|-----------|
| **Scopo** | Provisioning atomico di singole risorse | Orchestrazione di architetture complete |
| **Complessità** | Bassa - 1 risorsa/servizio | Alta - più moduli + logica business |
| **Esempio** | Creare un Content Agent | Creare landscape completo (Dev/QA/Prod + Transport) |

---

## 🧩 Utilizzo dei Moduli

Per utilizzare uno dei moduli, è sufficiente referenziarlo direttamente dal repository GitHub nel proprio file Terraform, ad esempio:

```hcl
module "nome_modulo" {
  source = "git::https://github.com/RegestaItalia/regesta.devops.terraform.modules.nome_modulo.git?ref=main"
  # ...altri parametri...
}
```

## Elenco moduli disponibili

| Modulo                           | Descrizione breve                                              | Repository GitHub                                                                                                 | Stato                                         |
|-----------------------------------|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| btp-cloudfoundry-creation         | Attiva un'istanza Cloud Foundry su un subaccount SAP BTP      | [regesta.devops.terraform.modules.btp-cloudfoundry-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-cloudfoundry-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
| btp-integration-suite-creation    | Abilita entitlements e servizi per SAP Integration Suite       | [regesta.devops.terraform.modules.btp-integration-suite-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-integration-suite-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
| btp-subaccount-creation           | Crea un subaccount SAP BTP                                    | [regesta.devops.terraform.modules.btp-subaccount-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-subaccount-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
| btp-roles-collections-assignment  | Assegna role collection agli utenti su un subaccount BTP      | [regesta.devops.terraform.modules.btp-roles-collections-assignment](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-roles-collections-assignment) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
| cf-space-creation                 | Crea uno space Cloud Foundry e assegna utenti                 | [regesta.devops.terraform.modules.cf-space-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.cf-space-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
| sap-idp-user-provisioning         | Gestione utenti e gruppi su SAP Identity Provider via SCIM    | [regesta.devops.terraform.modules.sap-idp-user-provisioning](https://github.com/RegestaItalia/regesta.devops.terraform.modules.sap-idp-user-provisioning) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
| btp-destinations-creation          | Gestione e creazione di destinazioni SAP BTP tramite provider nativo | [regesta.devops.terraform.modules.btp-destinations-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-destinations-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
| btp-adobeformservice-creation      | Gestione e provisioning di Adobe Form Service su SAP BTP      | [regesta.devops.terraform.modules.btp-adobeformservice-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-adobeformservice-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
| btp-content-agent-creation | Provisioning e gestione di Content Agent su SAP BTP | [regesta.devops.terraform.modules.btp-content-agent-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-content-agent-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
| btp-print-server-creation | Provisioning e gestione di Print Server su SAP BTP | [regesta.devops.terraform.modules.btp-print-server-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-print-server-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
| btp-sapbuild-process-automation-creation | Provisioning e gestione di SAP Build Process Automation su SAP BTP | [regesta.devops.terraform.modules.btp-sapbuild-process-automation-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-sapbuild-process-automation-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
| btp-sapbuild-workzone-creation | Provisioning e gestione di SAP Build Work Zone su SAP BTP | [regesta.devops.terraform.modules.btp-sapbuild-workzone-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-sapbuild-workzone-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
| btp-ctms-creation | Provisioning e gestione di Cloud Transport Management Service (cTMS) su SAP BTP | [regesta.devops.terraform.modules.btp-ctms-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-ctms-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |

## Versioni provider

Tutti i moduli sono stati aggiornati per utilizzare le ultime versioni disponibili dei provider:

- **SAP BTP Provider**: `~> 1.18.0` (versione più recente: 1.18.1)
- **Cloud Foundry Provider**: `~> 1.11.0` (versione più recente: 1.11.0)
- **Restapi Provider**: `2.0.1` (versione più recente: 2.0.1)

## Changelog recenti

### Dicembre 2025
- **Nuova categoria**: Creazione repository [Cookbooks](https://github.com/RegestaItalia/regesta.devops.terraform.cookbooks) con ricette complete per scenari complessi
- **btp-ctms-creation**: Nuovo modulo per Cloud Transport Management Service
- **btp-destinations-creation**: Migrato dall'uso del provider REST API al provider nativo SAP BTP per la gestione delle destinazioni
  - Supporto nativo per tutte le feature del provider BTP
  - Migliore gestione delle credenziali e autenticazione
  - Struttura dati semplificata e tipizzata
- **Tutti i moduli**: Aggiornamento alle ultime versioni dei provider Terraform (BTP 1.18.0, CloudFoundry 1.11.0)

---

## 🍳 Cookbooks Disponibili

Le **cookbooks** sono ricette Terraform complete che orchestrano più moduli per implementare architetture end-to-end.

### Landscape Creation
Creazione automatizzata di un landscape completo BTP con:
- Subaccount per ambienti (Dev, Quality, Prod - configurabile)
- Subaccount dedicato per Transport Management
- Cloud Foundry per ogni subaccount
- Content Agent in ogni ambiente
- cTMS centralizzato con destinations verso tutti gli ambienti

**Tempo di provisioning**: ~20-30 minuti vs 4-6 ore manualmente

**[📖 Documentazione completa →](https://github.com/RegestaItalia/regesta.devops.terraform.cookbooks/tree/main/landscape-creation)**

---

## 🔗 Link Utili

- **[📚 Wiki Completa](https://github.com/RegestaItalia/regesta.devops.terraform/wiki)** - Documentazione dettagliata di tutti i moduli
- **[🍳 Cookbooks Repository](https://github.com/RegestaItalia/regesta.devops.terraform.cookbooks)** - Ricette complete per scenari complessi
- **[🏗️ Architecture Guide](https://github.com/RegestaItalia/regesta.devops.terraform/wiki/Architecture)** - Pattern architetturali e best practices
- **[👨‍💻 Development Guide](https://github.com/RegestaItalia/regesta.devops.terraform/wiki/Development-Guide)** - Guida per sviluppare nuovi moduli

---

**Maintainer:** Regesta Italia DevOps Team  
**Last Update:** Dicembre 2025