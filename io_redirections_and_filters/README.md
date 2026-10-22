# Shell, redirections et filtres
 
Projet `io_redirections_and_filters` du depot `holbertonschool-shell`.
 
Chaque script fait exactement deux lignes : le shebang `#!/bin/bash` suivi d'une seule commande. Les scripts sont executables et testes sous Ubuntu 20.04 LTS.
 
Restrictions : pas de backticks, de `&&`, de `||`, de `;`, ni de `sed` et `awk`.
 
## Scripts
 
| Fichier | Description |
|---|---|
| `0-hello_world` | Affiche "Hello, World" suivi d'un retour a la ligne. |
| `1-confused_smiley` | Affiche le smiley confus `"(Ôo)'`. |
| `2-hellofile` | Affiche le contenu du fichier `/etc/passwd`. |
| `3-twofiles` | Affiche le contenu de `/etc/passwd` puis celui de `/etc/hosts`. |
| `4-lastlines` | Affiche les 10 dernieres lignes de `/etc/passwd`. |
| `5-firstlines` | Affiche les 10 premieres lignes de `/etc/passwd`. |
| `6-third_line` | Affiche la troisieme ligne du fichier `iacta` (present dans le repertoire courant). |
| `7-file` | Cree un fichier au nom tres special (rempli de caracteres speciaux) contenant "Best School" suivi d'un retour a la ligne. |
| `8-cwd_state` | Ecrit le resultat de `ls -la` dans le fichier `ls_cwd_content` (cree s'il n'existe pas, ecrase sinon). |
| `9-duplicate_last_line` | Duplique la derniere ligne du fichier `iacta`. |
| `10-no_more_js` | Supprime tous les fichiers reguliers `.js` du repertoire courant et de ses sous-dossiers (les dossiers ne sont pas touches). |
| `11-directories` | Compte les dossiers et sous-dossiers du repertoire courant, caches inclus, sans compter `.` ni `..`. |
| `12-newest_files` | Affiche les 10 fichiers les plus recents du repertoire courant, un par ligne, du plus recent au plus ancien. |
| `13-unique` | Lit une liste de mots (un par ligne) sur l'entree standard et affiche, tries, ceux qui n'apparaissent qu'une seule fois. |
| `14-findthatword` | Affiche les lignes de `/etc/passwd` contenant le motif "root". |
| `15-countthatword` | Affiche le nombre de lignes de `/etc/passwd` contenant le motif "bin". |
| `16-whatsnext` | Affiche les lignes de `/etc/passwd` contenant "root", ainsi que les 3 lignes qui suivent chacune. |
| `17-hidethisword` | Affiche les lignes de `/etc/passwd` qui ne contiennent pas le motif "bin". |
| `18-letteronly` | Affiche les lignes de `/etc/ssh/sshd_config` qui commencent par une lettre (minuscule ou majuscule). |
| `19-AZ` | Lit l'entree standard et remplace les caracteres `A` par `Z` et `c` par `e`. |
| `20-hiago` | Lit l'entree standard et supprime toutes les lettres `c` et `C`. |
| `21-reverse` | Lit l'entree standard et inverse l'ordre des caracteres de chaque ligne. |
| `22-users_and_homes` | Affiche tous les utilisateurs de `/etc/passwd` avec leur repertoire personnel, au format `login:home`, tries par nom d'utilisateur. |
 
## Utilisation
 
Rendre un script executable, puis le lancer :
 
```
chmod +x 0-hello_world
./0-hello_world
```
 
Les scripts `13` et `19` a `21` lisent l'entree standard, on les utilise avec un pipe :
 
```
echo "texte" | ./21-reverse
```
 
## Verifications
 
- `wc -l fichier` doit afficher `2`.
- `./script | cat -e` permet de controler les retours a la ligne (le `$` marque la fin de chaque ligne).
