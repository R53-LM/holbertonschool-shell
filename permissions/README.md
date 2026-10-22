# Shell - Permissions

Projet Holberton School : gestion des permissions, des utilisateurs et des groupes sous Linux.

Repo : `holbertonschool-shell`
Dossier : `permissions`

## Description

Ce projet regroupe 17 scripts shell (taches 0 a 16) qui manipulent les permissions, les proprietaires et les groupes de fichiers et de dossiers. Chaque script contient exactement 2 lignes : le shebang `#!/bin/bash` puis une seule commande.

## Environnement et regles

- Teste sur Ubuntu 22.04 LTS
- Editeurs autorises : `vi`, `vim`, `emacs`
- Chaque script fait exactement 2 lignes et se termine par une nouvelle ligne
- Interdits : backticks, `&&`, `||`, `;`
- Tous les fichiers sont executables
- Les taches 3, 13, 14, 15 et 16 sont a realiser dans le sandbox (script place dans `/tmp`)

## Utilisation

```bash
chmod u+x nom_du_script
./nom_du_script
```

Pour les scripts qui modifient le proprietaire ou le groupe, il faut les lancer avec les droits de root :

```bash
sudo ./nom_du_script
```

## Liste des scripts

| N  | Fichier                        | Commande                                 | Description                                                                                   |
|----|--------------------------------|------------------------------------------|-----------------------------------------------------------------------------------------------|
| 0  | `0-iam_betty`                  | `su betty`                               | Change l'utilisateur courant pour `betty` (commande de 8 caracteres, retour a la ligne exclu) |
| 1  | `1-who_am_i`                   | `whoami`                                 | Affiche le nom de l'utilisateur courant                                                       |
| 2  | `2-groups`                     | `groups`                                 | Affiche tous les groupes auxquels appartient l'utilisateur courant                            |
| 3  | `3-new_owner`                  | `chown betty hello`                      | Change le proprietaire du fichier `hello` pour `betty` (sandbox)                              |
| 4  | `4-empty`                      | `touch hello`                            | Cree un fichier vide nomme `hello`                                                            |
| 5  | `5-execute`                    | `chmod u+x hello`                        | Ajoute la permission d'execution au proprietaire du fichier `hello`                           |
| 6  | `6-multiple_permissions`       | `chmod ug+x,o+r hello`                   | Ajoute l'execution au proprietaire et au groupe, et la lecture aux autres, sur `hello`        |
| 7  | `7-everybody`                  | `chmod a+x hello`                        | Ajoute l'execution pour tous les utilisateurs sur `hello`, sans utiliser de virgule           |
| 8  | `8-James_Bond`                 | `chmod 007 hello`                        | Met `hello` sans aucun droit pour le proprietaire et le groupe, et tous les droits pour les autres |
| 9  | `9-John_Doe`                   | `chmod 753 hello`                        | Donne a `hello` les permissions `-rwxr-x-wx`                                                  |
| 10 | `10-mirror_permissions`        | `chmod --reference=olleh hello`          | Donne a `hello` les memes permissions que le fichier `olleh`                                  |
| 11 | `11-directories_permissions`   | `chmod a+x */`                           | Ajoute l'execution pour tous, uniquement sur les dossiers du repertoire courant               |
| 12 | `12-directory_permissions`     | `mkdir -m 751 my_dir`                    | Cree le dossier `my_dir` avec les permissions `rwxr-x--x`                                     |
| 13 | `13-change_group`              | `chgrp school hello`                     | Change le groupe du fichier `hello` pour `school` (sandbox)                                   |
| 14 | `14-change_owner_and_group`    | `chown vincent:staff *`                  | Change le proprietaire en `vincent` et le groupe en `staff` pour tous les fichiers et dossiers du repertoire courant (sandbox) |
| 15 | `15-symbolic_link_permissions` | `chown -h vincent:staff _hello`          | Change le proprietaire et le groupe du lien symbolique `_hello` lui-meme, en `vincent` et `staff` (sandbox) |
| 16 | `16-if_only`                   | `chown --from=guillaume vincent hello`   | Change le proprietaire de `hello` en `vincent`, seulement si il appartient actuellement a `guillaume` (sandbox) |

## Auteur

Projet realise dans le cadre de la formation Holberton School.
