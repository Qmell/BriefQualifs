# Brief_Scoring_CVSS.md

##  Lieux :

- Salle sécurisée (AV = Réseau Local Uniquement) (CIA ne bouge pas)
- My home 		  (AV = Network, AC = Low)
- La plage 	 	  (AV = Network, CIA = High, Complexité d'accès = Low)

##  Environnements : 

- Les Smartphones   (Choisir 3 CVE)
- Open Sources	    (Choisir 3 logiciels Opensources)
- Microsoft 		(Choisir 3 logiciels Microsoft)

Exemple : Noter le timbre (formule de calcul CVSS) de la CVE choisie.

Reprendre le Scoring et l'adapter à notre environnement.

Noter le nouveau Score.

Comparer au Score par défaut de la CVE.

Associer 1 environnement avec 1 thème + la pilule et calculer le nouveau score.

Essayer d'associer un thème avec le meilleur environnement pour obtenir le score le plus bas.

Pilule Rouge pour tous les calculs = environnement hostile.

## Smartphones : 

### - Android 11  	   --> La plage 		  --> CVE-2021-0870  Score de base : 8.1  CVSS:3.1/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H/A:H

Score recalculé avec l'environnement La plage : **9.8** CVSS3.0/AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:N/MAC:L/MPR:N/MUI:N/MS:U/MC:H/MI:H/MA:H (https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:H/PR:N/UI:N/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:N/MAC:L/MPR:N/MUI:N/MS:U/MC:H/MI:H/MA:H&version=3.0)

Le score augmente de 8.1 à 9.8. Cette augmentation est due au faible niveau de sécurité de notre environnement. L'exploitation de la vulnérabilité ne nécessite ni prvilège, ni intervention d'un utilisateur, et pourrait conduire à l'execution de code à distance par le biai d'une situation de compétition (race condition). 
Il est vivement recommandé d'arrêter d'utiliser ses logiciels de production industrielle quand on va se faire dorer la pilule, qu'elle soit rouge où non.

### - IOS 15.1    	   --> My home 		      --> CVE-2021-30889 Score de base : 8.8  CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H

Score recalculé avec l'environnement My home : **8.8** CVSS3.0/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:N/MAC:L/MPR:N/MUI:R/MS:U/MC:H/MI:H/MA:H (https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:N/MAC:L/MPR:N/MUI:R/MS:U/MC:H/MI:H/MA:H&version=3.0)

Le score reste de 8.8. Cette vulnérabilité permet via l'usage de contenu web conçu dans un but malveillant, d'aboutir à une execution de code arbitraire (ACE). Ceci peut compromettre entièrement le système. Dans cet environnement cette vulnérabilité est très critique de par son faible niveau de sécurité.
Il est recommandé de ne pas consulter ou de ne pas cliquer sur des liens qui parraissent louches. 

### - Monterey    	   --> Salle Sécurisée    --> CVE-2021-30824 Score de base : 7.8  CVSS:3.1/AV:L/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H

Score recalculé avec l'environnement Salle Sécurisée : **6.3** CVSS3.0/AV:L/AC:H/PR:H/UI:R/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:L/MAC:H/MPR:H/MUI:R/MS:U/MC:H/MI:H/MA:H (https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:L/AC:H/PR:H/UI:R/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:L/MAC:H/MPR:H/MUI:R/MS:U/MC:H/MI:H/MA:H&version=3.0)

Le score diminue de 7.8 à 6.3. Dans cet environnement sécurisé l'accès aux machine est plus difficile et diminue les risques liés à cette vulnérabilité, basée sur de l'execution de code via une application malveillante. Toutefois la criticité reste élevée car si la vulnérabilité est exploitée, c'est le système entier qui pourrait être corrompu.
Il est recommandé ici de ne pas installer d'application, ou d'utiliser des périphériques de sources non-sûres sur le matériel de l'entreprise.

## Open Source : 

### - Firefox     	   --> La plage           --> CVE-2021-35053 Score de base : 7.5  CVSS:3.1/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N/A:H

Score recalculé avec l'environnement La plage : **9.8** CVSS3.0/AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N/A:H/CR:H/IR:H/AR:H/MAV:N/MAC:L/MPR:N/MUI:N/MS:U/MC:H/MI:H/MA:H (https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:N/S:U/C:N/I:N/A:H/CR:H/IR:H/AR:H/MAV:N/MAC:L/MPR:N/MUI:N/MS:U/MC:H/MI:H/MA:H&version=3.0)

Le score augmente de 7.5 à 9.8. Cette faille met hors service le système concerné par déni de service après la modification de certains paramètres du navigateur Firefox. L'environnement simplifie l'accès au système utilisé et ne requiert pas de privilèges élevés pour pouvoir être exploité, d'où l'augmentation du score.
Il est recommandé de sécuriser et de ne pas laisser sans surveillance la machine concernée afin de prévenir les tentatives malveillantes.

### - LibreOffice 	   --> My home 			  --> CVE-2021-25631 Score de base : 8.8  CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H

Score recalculé avec l'environnement My home : **8.8** CVSS3.0/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:N/MAC:L/MPR:N/MUI:R/MS:U/MC:H/MI:H/MA:H(https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:N/MAC:L/MPR:N/MUI:R/MS:U/MC:H/MI:H/MA:H&version=3.0)

Le score n'a pas été modifié et est de 8.8car libreoffice est utilisé ici dans un environnement domestique au niveau de sécurité plutôt bas. La vulnérabilité permet l'execution de fichiers executables par un manipulation de la denylist (liste d'extensions refusées par le logiciel). C'est donc une vulnérabilité critique car elle met en péril le système concerné si exploitée.
Il est recommandé ici de verrouiller sa session quand l'on quitte son poste et de ne pas accepter ou d'ouvrir des types de fichiers qui parraissent louches ou qui ne sont pas compatible avec le logiciel utilisé.

### - Chromium    	   --> Salle Sécurisée    --> CVE-2021-38112 Score de base : 8.8  CVSS:3.1/AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:H/A:H

Score recalculé avec l'environnement Salle Sécurisée : **6.7** CVSSv3.0/AV:L/AC:H/PR:L/UI:R/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:L/MAC:H/MPR:L/MUI:R/MS:X/MC:H/MI:H/MA:H (https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:L/AC:H/PR:L/UI:R/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:L/MAC:H/MPR:L/MUI:R/MS:X/MC:H/MI:H/MA:H&version=3.0)

Le score passe de 8.8 à 6.7. Cette baisse est due au fait que nous sommes en environnement sécurisé et en réseau local, et donc plus difficile d'accès pour un éventuel attaquant. 

Cette vulnérabilité reste tout de même assez dangereuse car elle permet l'execution de code à distance directement à partir de l'infratructure du logiciel(framework), sur les workspaces des serveurs AWS d'Amazon. Il s'agit de la gestion de serveur pouvant contenir des données sensibles et donc c'est une vulnérabilité critique.
Il est recommandé de n'utiliser que les navigateurs habituels de votre entreprise.

## Microsoft : 

### - Microsoft Edge     --> La plage 		  --> CVE-2021-38669 Score de base : 8.8  CVSS:3.1/AV:N/AC:L/PR:L/UI:N/S:U/C:H/I:H/A:H

Score recalculé avec l'environnement La plage : **8.8** CVSSv3.0/AV:N/AC:L/PR:L/UI:N/S:U/C:H/I:H/A:H/CR:M/IR:H/AR:H/MAV:N/MAC:L/MPR:L/MUI:N/MS:U/MC:H/MI:H/MA:H (https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:L/UI:N/S:U/C:H/I:H/A:H/CR:M/IR:H/AR:H/MAV:N/MAC:L/MPR:L/MUI:N/MS:U/MC:H/MI:H/MA:H&version=3.0)

Le score reste à 8.8. Pas de changement de score, nous sommes dans un lieu public, le risque reste élevé car il n'y pas de couche de sécurité supplémentaire. Les données ici sont sensibles car il s'agit dans le cas de cette vulnérabilité, d'agir sur les informations échangées entre le client et le serveur, par exemple sur un site d'e-commerce (Tampering Attack), pour modifier et altérer ces informations.

Il serait recommandé ici de passer par une connexion VPN afin de sécuriser les échanges de données.

### - Microsoft Skype    --> My home  		  --> CVE-2021-26422 Score de base : 7.2  CVSS:3.1/AV:N/AC:H/PR:L/UI:N/S:U/C:H/I:H/A:H

Score recalculé avec l'environnement My home : **8.8** CVSSv3.0/AV:N/AC:L/PR:H/UI:N/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:N/MAC:L/MPR:L/MUI:N/MS:U/MC:H/MI:H/MA:H (https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:H/UI:N/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:N/MAC:L/MPR:L/MUI:N/MS:U/MC:H/MI:H/MA:H&version=3.0)

Le score passe de 7.2 à 8.8. Cette hausse est due au fait que nous sommes en environnement privé, sur un réseau domestique et pas forcément sécurisé, une cible potentiellement facile d'accès pour un attaquant.

Il s'agit ici d'une faille permettant l'execution de code à distance. Ici les données traitées sont personnelles, potentiellement sensibles, et cette vulnérabilité, si elle est exploitée peut mener à la perte de contrôle du système et la fuite des données.

### - Microsoft Outlook  --> Salle Sécurisée  --> CVE-2021-34413 Score de base : 7.5  CVSS:3.1/AV:N/AC:H/PR:L/UI:N/S:U/C:H/I:H/A:H

Score recalculé avec l'environnement Salle Sécurisée : **6.3** CVSSv3.0/AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:L/MAC:H/MPR:H/MUI:R/MS:U/MC:H/MI:H/MA:H (https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:L/AC:H/PR:L/UI:N/S:U/C:H/I:H/A:H/CR:H/IR:H/AR:H/MAV:L/MAC:H/MPR:H/MUI:R/MS:U/MC:H/MI:H/MA:H&version=3.0)

Le score passe de 7.5 à 6.3. Cette baisse est due au fait que nous sommes en environnement sécurisé et en réseau local, et donc plus difficile d'accès pour un éventuel attaquant.

Toutefois les CIA restent en high car les données traitées sont potentiellement sensibles. L'utilisation de ce plugin peut permettre à un utilisateur mal intentionné d'incorporer son application malveillante pendant le processus d'installation, ce qui lui permet de s'executer par élévation de privilèges (MPR:H), et potentiellement de pouvoir installer une porte dérobée dans le système.

Il est recommandé de n'utiliser que des plugins qui sont autorisés et approuvés par votre RSSI.
