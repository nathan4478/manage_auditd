[[_TOC_]]
***

# Nom

  manage_auditd

## Description

```bash
  # Installation du rpm
  # Configuration /etc/audit/auditd.conf
  # Implémentation des règles de surveillance ( /etc/audit/auditd.rules )
```

## Prérequis ( librairies, rpm, files, … )

```bash
  # fichier de règles auditd
  url => https://github.com/bfuzzy/auditd-attack/blob/master/auditd-attack.rules
```

## Tags

```bash
  # Installation et configuration auditd
  all, install 
  ou 
  auditd, install
  # Implémentation ou Update des règles
  auditd, install
```

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

```yaml
# ansible-playbook -i ${INVENTAIRE_DIR}/ --e "servers=<target >" -t "install,auditd,all" ${ROLE_DIR}/manage_auditd/tests/pbk_manage_auditd.yml --check
# ansible-playbook -i ${INVENTAIRE_DIR) --e "servers=< target >" -t "install,auditd,all" $(ROLE_DIR}/manage_auditd/tests/pbk_manage_auditd.yml

    - hosts: "{{ servers }}"
      gather_facts: yes

      roles:
        - { role: manage_auditd, tags: [auditd, all], become_user: root, become: yes }
```

## Mode opératoire pour l'execution du Playbook

### STEP1

### STEP2

### STEP3

## commandes ansible

## Auteur
