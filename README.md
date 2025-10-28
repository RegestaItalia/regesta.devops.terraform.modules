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
| btp-destinations-creation          | Gestione e creazione di destinazioni SAP BTP tramite REST API | [regesta.devops.terraform.modules.btp-destinations-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-destinations-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |

| btp-adobeformservice-creation      | Gestione e provisioning di Adobe Form Service su SAP BTP      | [regesta.devops.terraform.modules.btp-adobeformservice-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-adobeformservice-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
| btp-sapbuild-process-automation-creation | Provisioning e gestione di SAP Build Process Automation su SAP BTP | [regesta.devops.terraform.modules.btp-sapbuild-process-automation-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-sapbuild-process-automation-creation) | ![Completed](https://img.shields.io/badge/completed-brightgreen)   |
