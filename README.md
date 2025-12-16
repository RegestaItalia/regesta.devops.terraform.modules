# Moduli Terraform Regesta

Questo repository raccoglie tutti i moduli Terraform sviluppati da Regesta Italia per facilitare l'automazione e la gestione di risorse SAP BTP, Cloud Foundry e servizi correlati.

## Utilizzo dei moduli

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
## Versioni provider

Tutti i moduli sono stati aggiornati per utilizzare le ultime versioni disponibili dei provider:

- **SAP BTP Provider**: `~> 1.18.0` (versione più recente: 1.18.1)
- **Cloud Foundry Provider**: `~> 1.11.0` (versione più recente: 1.11.0)
- **Restapi Provider**: `2.0.1` (versione più recente: 2.0.1)

## Changelog recenti

### Dicembre 2025
- **btp-destinations-creation**: Migrato dall'uso del provider REST API al provider nativo SAP BTP per la gestione delle destinazioni
  - Supporto nativo per tutte le feature del provider BTP
  - Migliore gestione delle credenziali e autenticazione
  - Struttura dati semplificata e tipizzata
- **Tutti i moduli**: Aggiornamento alle ultime versioni dei provider Terraform (BTP 1.18.0, CloudFoundry 1.11.0)