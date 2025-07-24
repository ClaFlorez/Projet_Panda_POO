# Analyse des Ventes avec Pandas

Ce projet Python met en œuvre une classe nommée `AnalyseVentes` pour effectuer une série d'analyses sur des données de ventes et de clients provenant de fichiers CSV.

## Objectifs du projet

- Charger des données de commandes et de clients
- Nettoyer et préparer les données (types, valeurs manquantes, doublons)
- Fusionner les deux jeux de données
- Afficher un aperçu des données prêtes à l’analyse

## Structure du projet

Le fichier principal contient la classe `AnalyseVentes` avec les méthodes suivantes :

| Méthode                      | Description |
|-----------------------------|-------------|
| `__init__()`                | Chargement des données clients et commandes |
| `convertir_types()`         | Conversion des dates et des prix |
| `gerer_valeurs_manquantes()`| Gestion des valeurs manquantes (quantité) |
| `supprimer_doublons_clients()` | Suppression des doublons dans les clients |
| `fusionner_donnees()`       | Fusion des données et calcul des montants |
| `afficher_apercu(n)`        | Affiche les `n` premières lignes du DataFrame fusionné |

## Fichiers requis

Les fichiers suivants sont utilisés dans ce projet (hébergés sur GitHub ou en local) :

- `clients.csv`
- `commandes.csv`

## Exemple d'utilisation

```python
url_clients = "https://raw.githubusercontent.com/votre-utilisateur/Projet_Panda_POO/main/clients.csv"
url_commandes = "https://raw.githubusercontent.com/votre-utilisateur/Projet_Panda_POO/main/commandes.csv"

analyse = AnalyseVentes(url_clients, url_commandes)
analyse.convertir_types()
analyse.gerer_valeurs_manquantes()
analyse.supprimer_doublons_clients()
analyse.fusionner_donnees()
analyse.afficher_apercu(10)
