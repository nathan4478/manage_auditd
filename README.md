[[_TOC_]]
***

# Nom

    manage_auditd

## Description

    Déploiement du rpm auditd
    Configuration /etc/audit/auditd.conf
    Implémentation des règles de surveillance ( /etc/audit/auditd.rules )

## Prérequis ( librairies, rpm, files, … )

    Fichier de règles auditd. 
    ex : https://github.com/bfuzzy/auditd-attack/blob/master/auditd-attack.rules

## Tags

    - all, install
    - auditd, install
    - auditd, config
    
## Variables
    
* Variables sécurisées nécessaires au déploiement de l'applicatif ( container vault )

* Variables nécessaires au déploiement de l'applicatif 

```yaml
    # Fichier de règles à appliquer sur l'instance cible
    auditd_rules_file: "auditd_default.rules"

    # Exclusion des règles ( par defaut, elles sont toutes appliquées )
    auditd_exclude_rules:
      - "-w /etc/sudoers.d/ -p wa -k actions"
```

## Dépendances ( Liste des urls des roles )

## Example Playbook

## Mode opératoire pour l'execution du Playbook

### STEP1

### STEP2

### STEP3

## commandes ansible

## Auteur

