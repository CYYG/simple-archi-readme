# Exemple de documentation d'application
## Description de l'application

Ce README est un exemple de documentation d'application afin de comprendre son activité, les informations et services dont elle a besoin, les messages qu'elle envoit ainsi que les informations qu'elle expose.

L'exemple d'application ici est une application de gestion d'offre commerciale. 

## Domaine de responsabilité

### Données référentes

**Offre**
* Prix
* Date de début
* ...

### Applications sources
* [Produits]
* [Fournisseurs]

[Produits]: https://github.com/CYYG/simple-archi-readme/tree/master/exemple_app_produits
[Fournisseurs]: https://github.com/CYYG/simple-archi-readme

### Applications cible
* [Catalogue]
* [Gestion documentaire]

[Catalogue]: https://github.com/CYYG/simple-archi-readme
[Gestion documentaire]: https://github.com/CYYG/simple-archi-readme

## Flux d'informations entrants et sortants

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
[Catalogue] | Liste des offres à indexer dans le catalogue | HTTP/JSON | Async batch
[Gestion documentaire] | Déposer le rapport d'import des produit dans la GED du fournisseur | HTTP/JSON | Async bus


### Informations exposées
Information/service | format
--- | --- 
Liste des offres d'un fournisseur | HTTP/JSON, FTP/CSV HTTP/CSV
Détail d'une offre | HTTP/JSON

API Ref: _**TODO:** lien Swagger ou ReDoc_

## Détails de l'application
> [Architecture applicative](./architecture)
> [ADR (Architecture Decision Record)](./adr)