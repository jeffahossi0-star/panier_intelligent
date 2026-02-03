# Panier Intelligent

Application web de gestion de courses et d'analyse de dépenses familiales développée en PHP natif avec architecture MVC.

## 🌐 **Application en ligne**

**🚀 Accédez à l'application :** [https://panierintelligentjeff.42web.io/](https://panierintelligentjeff.42web.io/)

### 📸 Capture d'écran de l'application

![Application Panier Intelligent](localhost_panier_index.php_success=1.png)

L'application vous permet de :
- ✅ Ajouter des produits avec prix en FCFA
- 📊 Visualiser les statistiques de dépenses
- 🏆 Identifier le top produit le plus acheté
- 📱 Interface moderne et responsive

## 📋 Fonctionnalités

- ✅ Ajouter des produits (nom, prix, quantité)
- ✅ Afficher la liste des produits avec calcul automatique des totaux
- ✅ Calculer le total des dépenses
- ✅ Identifier le "Top produit" (le plus acheté en quantité)
- ✅ Interface moderne et responsive
- ✅ Architecture MVC propre et sécurisée

## 🏗️ Structure du projet

```
panier/
├── config/
│   └── database.php          # Configuration de la base de données
├── models/
│   └── Produit.php           # Modèle Produit avec fonction calculTotal()
├── controllers/
│   └── ProduitController.php # Contrôleur principal
├── views/
│   ├── header.php            # En-tête HTML
│   ├── footer.php            # Pied de page HTML
│   ├── formulaire.php        # Formulaire d'ajout
│   ├── liste.php             # Liste des produits
│   └── statistiques.php      # Statistiques
├── assets/
│   └── css/
│       └── style.css         # Feuille de style
├── index.php                 # Point d'entrée principal
├── database.sql              # Script SQL de création
├── test_calculTotal.php      # Fichier de test
└── README.md                 # Documentation
```

## 🚀 Instructions de déploiement

### ✅ **Application déjà déployée**

L'application est déjà en ligne et fonctionnelle :
- **URL principale :** https://panierintelligentjeff.42web.io/
- **Tests unitaires :** https://panierintelligentjeff.42web.io/tests/run_tests.php

### 1. Prérequis (pour déploiement local)

- PHP 7.4 ou supérieur
- MySQL 5.7 ou supérieur
- Serveur web (Apache, Nginx)

### 2. Déploiement local (XAMPP/WAMP)

1. **Copier les fichiers** dans le dossier `htdocs/panier/`
2. **Créer la base de données** :
   ```sql
   -- Importer le fichier database.sql via phpMyAdmin
   -- Ou exécuter manuellement les commandes SQL
   ```
3. **Configurer la base de données** si nécessaire :
   - Modifier `config/database.php` avec vos identifiants
4. **Accéder à l'application** :
   - Ouvrir `http://localhost/panier/` dans votre navigateur

### 3. Déploiement sur hébergement mutualisé gratuit

#### Option 1: InfinityFree
1. Créer un compte sur [InfinityFree](https://infinityfree.net/)
2. Créer une base de données MySQL via le panneau de contrôle
3. Uploader tous les fichiers via FTP
4. Importer `database.sql` via phpMyAdmin
5. Modifier `config/database.php` avec les identifiants fournis


### 4. Configuration de la base de données

Modifier `config/database.php` :

```php
private $host = 'localhost';           // Serveur MySQL
private $db_name = 'panier_intelligent'; // Nom de la base
private $username = 'votre_utilisateur'; // Votre utilisateur
private $password = 'votre_motdepasse';  // Votre mot de passe
```

## 🧪 Tests Unitaires

### 🚀 **Lancer les tests en ligne**

**Suite complète de tests :** [https://panierintelligentjeff.42web.io/tests/run_tests.php](https://panierintelligentjeff.42web.io/tests/run_tests.php)

**Raccourci rapide :** [https://panierintelligentjeff.42web.io/test_runner.php](https://panierintelligentjeff.42web.io/test_runner.php)

### 📊 Tests disponibles

L'application dispose d'une suite de tests unitaires complète avec analyse de couverture de code :

```bash
# Tests locaux (développement)
http://localhost/panier/tests/run_tests.php

# Tests en ligne (production)
https://panierintelligentjeff.42web.io/tests/run_tests.php
```

### Tests inclus

#### 📊 Fonction `calculTotal()`
- ✅ Tableau vide
- ✅ Un seul produit  
- ✅ Plusieurs produits
- ✅ Quantité zéro

#### 🗄️ Classe `Produit`
- ✅ Création en base de données
- ✅ Lecture de tous les produits
- ✅ Calcul du total des dépenses

#### 📈 Rapport généré
- **Statistiques** : taux de réussite, temps d'exécution
- **Couverture de code** : analyse des fichiers PHP
- **Recommandations** : suggestions d'amélioration
- **Interface moderne** : design responsive avec animations

### Test rapide

Pour tester uniquement la fonction `calculTotal()` :

```bash
http://localhost/panier/test_calculTotal.php
```

## 🔒 Sécurité

- Utilisation de PDO avec requêtes préparées
- Protection contre les injections SQL
- Échappement des données avec `htmlspecialchars()`
- Validation des entrées utilisateur

## 🎨 Personnalisation

### Modifier les couleurs
Éditer `assets/css/style.css` et modifier les variables de couleur :

```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
```

### Ajouter de nouvelles fonctionnalités
1. Créer de nouvelles méthodes dans `models/Produit.php`
2. Ajouter les actions correspondantes dans `controllers/ProduitController.php`
3. Créer les vues nécessaires dans le dossier `views/`

## 📝 Notes importantes

- L'application utilise PHP natif sans framework pour une compatibilité maximale
- La structure MVC facilite la maintenance et l'évolution
- Le code est optimisé pour les hébergements mutualisés avec ressources limitées
- Tous les fichiers sont encodés en UTF-8

## 🐛 Dépannage

### Erreur de connexion à la base de données
- Vérifier les identifiants dans `config/database.php`
- S'assurer que la base de données existe
- Vérifier que l'utilisateur a les droits nécessaires

### Page blanche
- Activer l'affichage des erreurs PHP :
  ```php
  error_reporting(E_ALL);
  ini_set('display_errors', 1);
  ```
- Vérifier les logs d'erreurs du serveur

### Problèmes de permissions
- S'assurer que les dossiers ont les bonnes permissions (755)
- Vérifier que les fichiers sont accessibles en lecture (644)

---

## 🎯 **Liens rapides**

| Lien | Description |
|------|-------------|
| **🌐 Application** | [https://panierintelligentjeff.42web.io/](https://panierintelligentjeff.42web.io/) |
| **🧪 Tests Unitaires** | [https://panierintelligentjeff.42web.io/tests/run_tests.php](https://panierintelligentjeff.42web.io/tests/run_tests.php) |
| **📊 Rapport de Tests** | [https://panierintelligentjeff.42web.io/test_runner.php](https://panierintelligentjeff.42web.io/test_runner.php) |

---

## 📸 **Capture d'écran**

![Application Panier Intelligent](https://panierintelligentjeff.42web.io/imageapp.png)

*Interface de l'application Panier Intelligent avec gestion des courses et statistiques*
