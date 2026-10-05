# Installation d'un serveur GLPI sous Debian

Projet réalisé dans le cadre de ma première année de BTS SIO option SISR (MyDigitalSchool Grenoble).

## Objectif
Mettre en place GLPI, un outil open source de gestion de parc informatique et de helpdesk,
pour inventorier le matériel d'une organisation et suivre les demandes d'assistance des utilisateurs.

## Environnement
- Machine virtuelle VirtualBox sous **Debian 13**
- **GLPI 10.0.18**
- Serveur web **Apache**, **PHP 8.3**, base de données **MariaDB**

## Ce que j'ai réalisé
- Installation et configuration d'Apache, de PHP et de MariaDB
- Création de la base de données et de l'utilisateur dédié à GLPI
- Configuration du VirtualHost Apache et de la réécriture d'URL (.htaccess)
- Installation de GLPI via l'assistant web et accès au tableau de bord administrateur

## Difficultés rencontrées et solutions
- **Changement d'environnement** : l'installation sous Windows rencontrait des bugs qui empêchaient
  d'aller jusqu'au bout. J'ai choisi de basculer sur une machine virtuelle Debian, un environnement
  Linux plus adapté à l'hébergement d'un serveur web comme GLPI.
- **Incompatibilité de version** : Debian 13 installe PHP 8.4, alors que GLPI 10.0.18 demande une version
  antérieure. J'ai ajouté un dépôt externe pour installer PHP 8.3, puis j'ai basculé Apache sur cette version.
- **Configuration Apache** : correction du VirtualHost pour que le site réponde correctement.
- **Base de données** : diagnostic et recréation de la base après un échec silencieux.

## Ce que j'ai appris
Lire les prérequis d'un logiciel avant de l'installer, diagnostiquer une erreur à partir des journaux,
et documenter chaque étape pour pouvoir reproduire l'installation.
