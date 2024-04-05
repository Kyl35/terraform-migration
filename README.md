Ce projet consiste à présenter à un client la migration de son infrastructure vers le cloud avec Terraform afin de pouvoir déployer des ressources sur Azure.

1. Création d'une VM Ubuntu 22 sur Azure
- Connectez-vous à votre compte Azure.
- Cliquez sur "Créer une ressource" puis "Machine virtuelle".
- Remplissez les informations nécessaires telles que le nom de la machine virtuelle, la région, le groupe de ressources, etc.
- Choisissez l'image Ubuntu 22.
- Configurez les autres paramètres comme la taille de la VM, le stockage, le réseau, etc.
- Une fois les paramètres configurés, cliquez sur "Créer" pour déployer la VM Ubuntu 22 sur Azure.
- Ouvrez un terminal sur la VM.
- Faites la commande suivante pour installer Azure CLI :
```
curl -sL https://aka.ms/InstallAzureCLIDeb | sudo bash
```
- Une fois l'installation terminée, exécutez la commande suivante pour vous connecter à Azure :
```
az login
```
- Suivez les instructions à l'écran pour vous connecter à votre compte Azure et configurer les accès nécessaires.

2. Installation de Terraform
-  Ouvrez un terminal sur la VM Ubuntu 22.
- Téléchargez la dernière version de Terraform en utilisant la commande suivante :
```
wget https://releases.hashicorp.com/terraform/<VERSION>/terraform_<VERSION>_linux_amd64.zip
```
- Décompressez le fichier téléchargé en utilisant la commande suivante :
```
unzip terraform_<VERSION>_linux_amd64.zip
```
- Déplacez le binaire Terraform vers le répertoire /usr/local/bin en utilisant la commande suivante :
```
sudo mv terraform /usr/local/bin/
```
- Pour vérifier l'installation de Terraform, exécutez la commande suivante :
```
terraform --version
```

3. Création et déploiement de l'infrastructure avec Terraform
- Prenez le fichier de configuration Terraform fourni (avec l'extension .tf) contenant la définition de l'infrastructure.
- Initialisez le répertoire Terraform en utilisant la commande suivante :
```
terraform init
```
- Vérifiez la configuration de Terraform en utilisant la commande suivante :
```
terraform plan
```
- Déployez l'infrastructure en utilisant la commande suivante :
```
terraform apply
```
- Suivez les instructions à l'écran pour confirmer le déploiement de l'infrastructure.
