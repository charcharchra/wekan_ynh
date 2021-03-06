<!--
N.B.: This README was automatically generated by https://github.com/YunoHost/apps/tree/master/tools/README-generator
It shall NOT be edited by hand.
-->

# Wekan pour YunoHost

[![Niveau d'intégration](https://dash.yunohost.org/integration/wekan.svg)](https://dash.yunohost.org/appci/app/wekan) ![Statut du fonctionnement](https://ci-apps.yunohost.org/ci/badges/wekan.status.svg) ![Statut de maintenance](https://ci-apps.yunohost.org/ci/badges/wekan.maintain.svg)  
[![Installer Wekan avec YunoHost](https://install-app.yunohost.org/install-with-yunohost.svg)](https://install-app.yunohost.org/?app=wekan)

*[Read this readme in english.](./README.md)*

> *Ce package vous permet d'installer Wekan rapidement et simplement sur un serveur YunoHost.
Si vous n'avez pas YunoHost, regardez [ici](https://yunohost.org/#/install) pour savoir comment l'installer et en profiter.*

## Vue d'ensemble

WeKan ® est une application de tableau kanban collaborative entièrement libre et open source avec une licence MIT.


**Version incluse :** 6.30~ynh1

**Démo :** https://demo.sandstorm.io/appdemo/m86q05rdvj14yvn78ghaxynqz7u2svw6rnttptxx49g1785cdv1h

## Captures d'écran

![Capture d'écran de Wekan](./doc/screenshots/screenshot.jpg)

## Avertissements / informations importantes

* Il n'y a actuellement **pas d'intégration SSO**, bien qu'elle puisse être intégrée à un moment donné dans l'application, maintenant qu'elle est supportée par Meteor/Wekan. En attendant, les utilisateurs peuvent créer des comptes (en fait, ils peuvent créer un nombre infini de comptes) manuellement, et doivent se connecter manuellement spécifiquement dans Wekan.
* Cette application **ne fonctionne que sur une architecture x86, 64bits** ! En particulier, elle ne fonctionnera pas sur les machines 32 bits ou ARM. Voir la discussion [ici] (https://github.com/YunoHost-Apps/wekan_ynh/issues/1#issuecomment-401612500).
* Les utilisateurs de YunoHost ayant plus d'une adresse e-mail ne peuvent pas se connecter à wekan en utilisant ldap. Par exemple, le premier utilisateur de YunoHost a plusieurs adresses e-mail : root@domain ; admin@domain ; webmaster@domain ; postmaster@domain, etc.... Solution : supprimez tous les alias de messagerie de l'utilisateur que vous voulez connecter, connectez-vous une fois sur wekan, recréez les alias de l'utilisateur YunoHost.

## Configuration :
L'authentification LDAP étant activée par défaut, les admins de Wekan correspondent à la permission `Wekan Admin`. L'utilisateur que vous choisissez lors de l'installation est membre de ce groupe.
Pour ajouter un compte admin, vous pouvez :

- [avec le webadmin] allez dans Utilisateurs > Groupes et permissions > Ajouter l'utilisateur à la permission `Wekan Admin`.
- [ou avec la ligne de commande] `yunohost user permission update wekan.admin -a the_user_to_add`.

Tous les autres utilisateurs de YunhoHost peuvent accéder avec l'authentification LDAP.

Si vous avez désactivé l'authentification LDAP, le premier utilisateur enregistré sera l'administrateur, et les suivants seront des utilisateurs normaux. Si vous voulez d'autres administrateurs, vous pouvez changer leur permission à admin dans le panneau d'administration de Wekan.

**Mode privé/public:** En mode privé, seuls les membres autorisés de YunoHost peuvent accéder au Wekan.

## Documentations et ressources

* Site officiel de l'app : <https://wekan.github.io>
* Documentation officielle de l'admin : <https://github.com/wekan/wekan/wiki>
* Dépôt de code officiel de l'app : <https://github.com/wekan/wekan>
* Documentation YunoHost pour cette app : <https://yunohost.org/app_wekan>
* Signaler un bug : <https://github.com/YunoHost-Apps/wekan_ynh/issues>

## Informations pour les développeurs

Merci de faire vos pull request sur la [branche testing](https://github.com/YunoHost-Apps/wekan_ynh/tree/testing).

Pour essayer la branche testing, procédez comme suit.

``` bash
sudo yunohost app install https://github.com/YunoHost-Apps/wekan_ynh/tree/testing --debug
ou
sudo yunohost app upgrade wekan -u https://github.com/YunoHost-Apps/wekan_ynh/tree/testing --debug
```

**Plus d'infos sur le packaging d'applications :** <https://yunohost.org/packaging_apps>
