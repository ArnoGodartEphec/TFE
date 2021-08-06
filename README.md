# Conception, gestion et sécurisation d’une infrastructure virtualisée au moyen d'Ansible
  ## Commande générale
      sudo apt upgrade && sudo apt install
  ## Commandes principales liées à l'installation d'Ansible
   ### Installer Python sur le controler node 
      sudo apt install python3-pip
  ### Installer Ansible via pip
      pip3 install ansible
  ### Installation via les distributions Debian
      sudo apt install ansible
  ### Installation d'Ansible sous Centos
      sudo yum install ansible
  ### Vérifier la version d’Ansible
      ansible --version
      
 ## Commandes principales liées à SSH      
  ### Installer OpenSSH server 
      sudo apt install openssh-server
  ### Vérifier le status du service SSH
      sudo service ssh status
  ### Générer une paire de clés (ici le -t pour le type de clés (selon l'algorithme de chiffrement ecdsa) ainsi que le -b pour la longueur de clés)
      ssh-keygen -t ecdsa -b 521
  ### Injecter la clé publique sur le serveur distant
      ssh-copy-id [nomdutilisateur]
  ### Utiliser la clé privée pour se connecter sur le serveur distant
      ssh -i ~/.ssh/id_ecdsa
  ### Utiliser un agent SSH pour "embarquer" la configuration SSH durant la période de session
      eval `ssh-agent`
      ssh-add
  ###
  ###
