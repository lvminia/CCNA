# Chapitre 10 : Couche application

**La couche application** comprends tous les protocoles permettant de faire communiquer l'application en contact avec l'utilisateur et le réseau. On y voie des protocoles comme HTTP, FTP, SSH, etc.

**La couche présentation** a pour but de présenter les données dans une forme compréhensible par l'autre hote. On y retrouve des formats de compression et d'encodage de video, d'audio, d'image, etc.

**La couche session** a pour but de maintenir un dialogue entre les applications sources et distantes.

La couche application se représente le plus souvent comme un système client-serveur. Dans ce système, le client demande des informations au serveur qui répond par un ou plusieurs flux de données.

La couche application peut aussi utiliser un système peer-to-peer permettant un échange décentralisé entre les hotes. Ce système est notemment utilisé dans le protocole gNutella ou Bittorent permettant le partage de fichiers.

Le protocole HTTP permet de recupèrer une page Web sur le WorldWideWeb codé en HTML permettant à chaque navigateur de l'interpréter. Ce protocole bien qu'efficace n'est pas très sécurisé et le protocole HTTPS est mis en place pour garantire cette sécurité par le chiffrement des flux.

la messagerie email fait intervenir 3 protocoles SMTP, IMAP et POP permettant d'envoyer et de recevoir des emails.

Le protocol SMTP permet d'envoyer des emails sur le port 25 par defaut. le serveur SMTP recoit un email bien formaté a envoyer, il essaye alors de s'executer. Si il n'arrive pas à se connecter au serveur destinataire, il place le message en file d'attente. Si il n'arrive finalement pas a l'envoyer, il le renvoie au destinateire comme non délivrable.

Un serveur POP attends sur le port 110 une connexion du client. Des que la connexion est éfféctuée, les messages sont supprimés et téléchargés chez le client. POP ne stocke pas le messages contrairement a IMAP. Lors d'une connexion, les messages sont copiés et restent sur le serveur. L'utilisateur peut aussi organiser ses messages selon une hiérarchie de dossiers.

> Pour DNS et DHCP, voir les CERs associés

Le protocole FTP permet le transfert de fichiers, il utilise deux connexions, l'une pour le controle des flux (port 21) et l'autre pour l'envoie de fichiers (20).
