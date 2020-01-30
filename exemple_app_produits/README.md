# Exemple de documentation d'application
## Description de l'application

Ce README est un exemple de documentation d'application afin de comprendre son activité, les informations et services dont elle a besoin, les messages qu'elle envoit ainsi que les informations qu'elle expose.

L'exemple d'application ici est une application de gestion d'offre commerciale. 

## Domaine de responsabilité

> [Architecture applicative](./architecture)

### Données référentes

**Produit**
* Nom
* Description
* ...

### Applications sources
* [Fournisseurs]

[Fournisseurs]: https://www.github.com

### Applications cible
* Pas d'application cible

## Flux d'information entrant et sortant

### Dépendances
Application source | Information/Service consommé | Format utilisé | Type de flux
--- | --- | --- | ---
[Produits] | Liste des produits | HTTP/JSON | Async batch
[Produits] | Détail d'un produit | HTTP/JSON | Sync
[Produits] | Variantes d'un produit | HTPP/JSON | Sync
[Fournisseurs] | Liste de fournisseurs | HTTP/JSON | Async batch
[Fournisseurs] | Détail d'un fournisseur | HTTP/JSON | Sync

Application cible | Message envoyé | Format utilisé | Type de flux
--- | --- | --- | ---


### Informations exposées
Information/service | format
--- | --- 
Liste des produits | HTTP/JSON, FTP/CSV
Détail d'un produit | HTTP/JSON
Variantes d'un produit | HTPP/JSON