Création d’utilisateurs et programmation

 Nano (nom fu fichier)

#! /bin/bash
While red line; do
    Sudo useradd “$line”
done < (nom du fichier)
—————————————
Installation de programmes

(smn 10)
mkdir (nom du fichier)
ls
cd (nom du fichier)
ls
gcc hello.c
ls
./a out 
————————
Copiez l’exécutable dans un répertoire faisant partie du PATH des 4 utilisateurs créés précédemment et modifiez les permissions de cet exécutable pour que seuls ces 4 utilisateurs puissent l’exécuter.

echo $PATH
export PATH=$PATH:/usr/local/bin
sudo cp (nom du fichier) /usr/local/bin
chmod u+x (nom du fichier)
ls -l
—————————
Téléchargez le programme suivant sur github et installez‐le :
sudo apt-get install git 
git clone (site)
cd proxychains 
sudo apt-get install build-essential
./configure
make sudo install
———
Quelle est la taille de chacune des partitions sur votre VM Debian?
df -h
—— 
Sur votre VM téléchargez http://www.tinycorelinux.net/13.x/x86/release/CorePlus‐ current.iso puis montez le fichier ISO dans le répertoire /media/iso/core

wget(site)
mkdir -p (ou tu vx le mettre)
——
Cherchez dans le journal des authentifications pour savoir combien de fois l’utilisateur info a utilisé la commande sudo.

cat /var/log/auth.log or less
grep sudo /var/log/auth.log
grep sudo /var/log/auth.log | wc -1
grep -w “user info” /var/log/auth.log | grep sudo | wc -1
