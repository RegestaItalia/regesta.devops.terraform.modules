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

| Modulo                           | Descrizione breve                                              | Repository GitHub                                                                                                 |
|-----------------------------------|---------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| btp-cloudfoundry-creation         | Attiva un'istanza Cloud Foundry su un subaccount SAP BTP      | [regesta.devops.terraform.modules.btp-cloudfoundry-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-cloudfoundry-creation) |
| btp-integration-suite-creation    | Abilita entitlements e servizi per SAP Integration Suite       | [regesta.devops.terraform.modules.btp-integration-suite-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-integration-suite-creation) |
| btp-subaccount-creation           | Crea un subaccount SAP BTP                                    | [regesta.devops.terraform.modules.btp-subaccount-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.btp-subaccount-creation) |
| cf-build-and-deploy-mta           | Gestione build e deploy di applicazioni MTA su Cloud Foundry   | [regesta.devops.terraform.modules.cf-build-and-deploy-mta](https://github.com/RegestaItalia/regesta.devops.terraform.modules.cf-build-and-deploy-mta) |
| cf-space-creation                 | Crea uno space Cloud Foundry e assegna utenti                 | [regesta.devops.terraform.modules.cf-space-creation](https://github.com/RegestaItalia/regesta.devops.terraform.modules.cf-space-creation) |
| sap-idp-users-provisioning        | Gestione utenti e gruppi su SAP Identity Provider via SCIM    | [regesta.devops.terraform.modules.sap-idp-users-provisioning](https://github.com/RegestaItalia/regesta.devops.terraform.modules.sap-idp-users-provisioning) |
