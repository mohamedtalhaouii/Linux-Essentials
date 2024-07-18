## Guide des Commandes Essentielles de Linux et du Scripting Shell

### Commandes de Base

1. **`pwd`**: Afficher le répertoire de travail.
   ```bash
   pwd
   ```
   - Affiche le répertoire courant.

2. **`ls`**: Lister le contenu d'un répertoire.
   ```bash
   ls
   ls -l  # Format long
   ls -a  # Afficher les fichiers cachés
   ```
   - Liste les fichiers et répertoires dans le répertoire courant.

3. **`cd`**: Changer de répertoire.
   ```bash
   cd /chemin/vers/repertoire
   cd ..  # Remonter d'un niveau
   cd ~   # Aller au répertoire personnel
   ```
   - Change le répertoire courant.

4. **`mkdir`**: Créer des répertoires.
   ```bash
   mkdir nouveau_repertoire
   mkdir -p /chemin/vers/nouveau_repertoire  # Créer les répertoires parents si nécessaire
   ```
   - Crée de nouveaux répertoires.

5. **`rmdir`**: Supprimer des répertoires vides.
   ```bash
   rmdir repertoire_vide
   ```
   - Supprime des répertoires vides.

6. **`touch`**: Créer un fichier vide ou mettre à jour l'horodatage d'un fichier.
   ```bash
   touch nouveau_fichier.txt
   ```
   - Crée ou met à jour l'horodatage d'un fichier.

7. **`rm`**: Supprimer des fichiers ou des répertoires.
   ```bash
   rm fichier.txt
   rm -r repertoire  # Supprimer récursivement un répertoire
   ```
   - Supprime des fichiers ou des répertoires.

8. **`cp`**: Copier des fichiers ou des répertoires.
   ```bash
   cp source.txt destination.txt
   cp -r repertoire_source repertoire_destination  # Copier récursivement un répertoire
   ```
   - Copie des fichiers ou des répertoires.

9. **`mv`**: Déplacer ou renommer des fichiers ou des répertoires.
   ```bash
   mv ancien_nom.txt nouveau_nom.txt
   mv fichier.txt /nouveau/chemin/
   ```
   - Déplace ou renomme des fichiers ou des répertoires.

10. **`cat`**: Concaténer et afficher le contenu d'un fichier.
    ```bash
    cat fichier.txt
    ```
    - Affiche le contenu d'un fichier.

11. **`echo`**: Afficher une ligne de texte.
    ```bash
    echo "Bonjour tout le monde !"
    ```
    - Affiche du texte dans le terminal.

### Permissions de Fichiers

1. **`chmod`**: Changer le mode (permissions) d'un fichier.
   ```bash
   chmod 755 fichier.txt  # rwxr-xr-x
   chmod u+x script.sh    # Ajouter la permission d'exécution pour l'utilisateur
   ```
   - Change les permissions d'un fichier.

2. **`chown`**: Changer le propriétaire et le groupe d'un fichier.
   ```bash
   chown utilisateur:groupe fichier.txt
   ```
   - Change le propriétaire et le groupe d'un fichier.

3. **`chgrp`**: Changer le groupe propriétaire d'un fichier.
   ```bash
   chgrp groupe fichier.txt
   ```
   - Change le groupe propriétaire d'un fichier.

### Gestion des Processus

1. **`ps`**: Afficher un instantané des processus actifs.
   ```bash
   ps aux
   ```
   - Affiche les processus actifs.

2. **`top`**: Afficher les tâches Linux.
   ```bash
   top
   ```
   - Affiche les tâches système.

3. **`kill`**: Envoyer un signal à un processus.
   ```bash
   kill PID
   kill -9 PID  # Terminer un processus de force
   ```
   - Termine un processus.

4. **`killall`**: Terminer des processus par nom.
   ```bash
   killall nom_processus
   ```
   - Termine des processus par leur nom.

5. **`bg`**: Reprendre un travail arrêté en arrière-plan.
   ```bash
   bg %1
   ```
   - Reprend un travail en arrière-plan.

6. **`fg`**: Ramener un travail en premier plan.
   ```bash
   fg %1
   ```
   - Ramène un travail en premier plan.

7. **`jobs`**: Lister les travaux actifs.
   ```bash
   jobs
   ```
   - Liste les travaux en arrière-plan.

### Recherche de Fichiers

1. **`find`**: Rechercher des fichiers dans une hiérarchie de répertoires.
   ```bash
   find /chemin/vers/recherche -name "nom_fichier"
   ```
   - Recherche des fichiers.

2. **`grep`**: Afficher les lignes qui correspondent à des motifs.
   ```bash
   grep "motif" fichier.txt
   grep -r "motif" /chemin/vers/recherche  # Recherche récursive
   ```
   - Recherche des motifs dans les fichiers.

3. **`locate`**: Trouver des fichiers par leur nom.
   ```bash
   locate nom_fichier
   ```
   - Trouve rapidement des fichiers.

4. **`which`**: Localiser une commande.
   ```bash
   which commande
   ```
   - Affiche le chemin d'une commande.

### Utilisation du Disque

1. **`df`**: Afficher l'utilisation de l'espace disque du système de fichiers.
   ```bash
   df -h
   ```
   - Affiche l'utilisation du disque.

2. **`du`**: Estimer l'espace disque utilisé par les fichiers.
   ```bash
   du -sh /chemin/vers/repertoire
   ```
   - Affiche l'utilisation du disque par un répertoire.

3. **`mount`**: Monter un système de fichiers.
   ```bash
   sudo mount /dev/sdX /mnt
   ```
   - Monte un système de fichiers.

4. **`umount`**: Démonter des systèmes de fichiers.
   ```bash
   sudo umount /mnt
   ```
   - Démonte un système de fichiers.

### Réseau

1. **`ping`**: Envoyer des paquets ICMP ECHO_REQUEST à des hôtes réseau.
   ```bash
   ping exemple.com
   ```
   - Teste la connectivité réseau.

2. **`ifconfig`**: Configurer une interface réseau.
   ```bash
   ifconfig
   ```
   - Configure les interfaces réseau.

3. **`netstat`**: Afficher les connexions réseau, les tables de routage, les statistiques d'interface, les connexions masquées et les adhésions multicast.
   ```bash
   netstat -tuln
   ```
   - Affiche les connexions réseau.

4. **`ssh`**: Client SSH OpenSSH (programme de connexion à distance).
   ```bash
   ssh utilisateur@hote
   ```
   - Se connecte à un hôte distant.

5. **`scp`**: Copie sécurisée (programme de copie de fichiers à distance).
   ```bash
   scp fichier.txt utilisateur@hote:/chemin/vers/destination
   ```
   - Copie des fichiers entre hôtes.

6. **`wget`**: Téléchargeur réseau non interactif.
   ```bash
   wget http://exemple.com/fichier.zip
   ```
   - Télécharge des fichiers depuis le web.

7. **`curl`**: Transfère des données vers ou depuis un serveur.
   ```bash
   curl http://exemple.com
   ```
   - Transfère des données via des URLs.

### Gestion des Paquets

1. **`apt-get`**: Utilitaire de gestion des paquets APT (pour les distributions basées sur Debian).
   ```bash
   sudo apt-get update
   sudo apt-get install nom_paquet
   ```
   - Gère les paquets sur les systèmes basés sur Debian.

2. **`yum`**: Gestionnaire de paquets (pour les distributions basées sur RPM).
   ```bash
   sudo yum update
   sudo yum install nom_paquet
   ```
   - Gère les paquets sur les systèmes basés sur RPM.

3. **`dpkg`**: Gestionnaire de paquets Debian.
   ```bash
   sudo dpkg -i paquet.deb
   ```
   - Gère les paquets Debian.

4. **`rpm`**: Gestionnaire de paquets RPM.
   ```bash
   sudo rpm -i paquet.rpm
   ```
   - Gère les paquets RPM.

### Compression

1. **`tar`**:

 Archiver des fichiers.
   ```bash
   tar -cvf archive.tar repertoire
   tar -xvf archive.tar
   ```
   - Crée et extrait des archives tar.

2. **`gzip`**: Compresser des fichiers.
   ```bash
   gzip fichier.txt
   ```
   - Compresse des fichiers.

3. **`gunzip`**: Décompresser des fichiers.
   ```bash
   gunzip fichier.txt.gz
   ```
   - Décompresse des fichiers gzip.

4. **`zip`**: Emballer et compresser des fichiers.
   ```bash
   zip archive.zip fichier.txt
   ```
   - Crée des archives zip.

5. **`unzip`**: Extraire des fichiers compressés.
   ```bash
   unzip archive.zip
   ```
   - Extrait des archives zip.

### Traitement de Texte

1. **`awk`**: Langage de traitement et de recherche de motifs.
   ```bash
   awk '{print $1}' fichier.txt
   ```
   - Traite le texte en fonction de motifs.

2. **`sed`**: Éditeur de flux pour filtrer et transformer le texte.
   ```bash
   sed 's/ancien/nouveau/g' fichier.txt
   ```
   - Modifie le texte dans les flux.

3. **`sort`**: Trie les lignes des fichiers texte.
   ```bash
   sort fichier.txt
   ```
   - Trie les lignes des fichiers texte.

4. **`uniq`**: Rapporte ou omet les lignes répétées.
   ```bash
   uniq fichier.txt
   ```
   - Filtré les lignes répétées.

### Informations Système

1. **`uname`**: Affiche des informations système.
   ```bash
   uname -a
   ```
   - Affiche des informations système.

2. **`uptime`**: Indique depuis combien de temps le système est en marche.
   ```bash
   uptime
   ```
   - Indique le temps de fonctionnement du système.

3. **`dmesg`**: Affiche ou contrôle le tampon circulaire du noyau.
   ```bash
   dmesg
   ```
   - Affiche les messages du noyau.

4. **`who`**: Affiche qui est connecté.
   ```bash
   who
   ```
   - Affiche les utilisateurs connectés.

5. **`free`**: Affiche la quantité de mémoire libre et utilisée dans le système.
   ```bash
   free -h
   ```
   - Affiche l'utilisation de la mémoire.

### Gestion des Utilisateurs

1. **`adduser`**: Ajouter un utilisateur au système.
   ```bash
   sudo adduser nom_utilisateur
   ```
   - Ajoute un nouvel utilisateur.

2. **`deluser`**: Supprimer un utilisateur du système.
   ```bash
   sudo deluser nom_utilisateur
   ```
   - Supprime un utilisateur.

3. **`passwd`**: Mettre à jour les jetons d'authentification d'un utilisateur (mot de passe).
   ```bash
   passwd
   ```
   - Change le mot de passe d'un utilisateur.

### Scripting Shell

#### Écrire un Script Shell

1. **Créer un nouveau fichier**:
   ```bash
   touch script.sh
   ```
   - Crée un nouveau fichier de script.

2. **Le rendre exécutable**:
   ```bash
   chmod +x script.sh
   ```
   - Rend le script exécutable.

3. **Modifier le script**:
   ```bash
   nano script.sh
   ```
   - Ouvre le script dans un éditeur de texte (comme nano).

4. **Script Exemple**:
   ```bash
   #!/bin/bash
   echo "Bonjour à tous !"
   ```
   - Un script simple qui affiche "Bonjour à tous !".

5. **Exécuter le script**:
   ```bash
   ./script.sh
   ```
   - Exécute le script.

Ce guide couvre les commandes essentielles et les techniques de scripting shell de base essentielles pour toute personne apprenant ou utilisant Linux. Pratiquez régulièrement et explorez davantage pour maîtriser efficacement ces outils.

<hr>
<h3 align="center"> 🧑🏻‍💻 | Made By : <a href="https://github.com/mohamedtalhaouii" target="_blank">Mohamed Talhaoui</a></h3>
