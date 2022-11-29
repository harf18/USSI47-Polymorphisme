# TP : Héritage & Polymorphisme

### Objectif
Utiliser l'héritage et le polymorphisme dans le cadre de la POO

### Prérequis
- Cloner le projet sur votre poste dans le repertoire de votre choix
- Ouvrir le projet :
	- Sur l'écran d'accueil d'IntelliJ, cliquer sur **Open**
	- Sélectionner le dossier **tpPolymorphisme-xxx** qui a été copié depuis github puis cliquer sur **OK**.
	- Le projet s'ouvre
	- Allez vérifier que le SDK est bien sélectionné dans **File > Project Structure** onglet **Project**

### Utilisation de GIT

- Créer une nouvelle branche **prenomNom**
- Faire **1 commit** par exercice
- Ouvrir **une seule** *pull request* sur github et **ne pas** la fermer/merger !!

----

## Problème 1

Les fichiers de ce problème sont à créer dans le package `net.lecnam.ussi47.probleme1`

### Exercice 1

Ecrivez une classe **Batiment** avec les propriétés *adresse*, *nbPieces* et *surface* (un entier) 
et son constructeur ```Batiment(String adresse, int nbPieces, int surface)```.  
Créer la méthode ```String toString()``` pour qu'elle retourne une description de ce Bâtiment.

On ne doit pas pouvoir créer une instance de **Batiment**

> Pensez a faire un commit !!

### Exercice 2

Écrivez une classe **Maison** avec l'attribut *surfaceJardin*. Une maison est un **Batiment**   
Écrivez le constructeur ```Maison(String adresse, int nbPieces, int surface, int surfaceJardin)```.  
Écrivez aussi la méthode ```String toString().``` pour l'adapter à la maison.

> Pensez a faire un commit !!


### Exercice 3
Écrivez une classe **Appartement** avec l'attribut *etage*. Un appartement est un **Batiment** également    
Écrivez le constructeur correspondant et la méthode ```String toString()``` adaptée à l'appartement.

> Pensez a faire un commit !!

### Exercice 4
Dans la méthode ```main``` de la classe **Exec**, instancier 2 maisons et 2 appartements et les afficher.  

> Pensez a faire un commit !!

### Exercice 5

Créer une classe **Cadastre** avec un tableau de 100 bâtiments.  
Écrivez une méthode ```void ajoutBatiment(Batiment batiment)``` qui permet d'ajouter un bâtiment dans le tableau.  
Écrivez une méthode ```void afficheBatiment()``` qui parcours le tableau et affiche les toString() de chaque bâtiment.

Dans Exec, instancier un Cadastre, ajouter les bâtiments créés à l'exercice 4

> Pensez a faire un commit !!

### Exercice 6
Dans la classe **Cadastre** :
- Écrivez une méthode ```void afficheSurfaceTotale()``` qui affiche la surface totale.
- Écrivez une méthode ```void afficheSurfaceJardinTotale()``` qui affiche le total des jardins des **maisons** du tableau. (Pensez à `instance of` qui permet de tester le type d'un objet)

> Pensez a faire un commit !!

### Exercice 7
L’impôt local d’un bâtiment est calculé selon la formule `TauxA × surface + TauxB × surfaceJardin` pour les maisons et `TauxA × surface` pour les appartements.  
Les valeurs actuelles sont : TauxA = 5.6 et TauxB = 1.5.  
Déclarer les variables *tauxA* et *tauxB* dans les classes appropriées.  
Écrire dans les bonnes classes une méthode ```double getMontantImpot()``` qui retourne le montant de l'impôt et afficher le résultat dans toString();  

> Pensez a faire un commit !!

### Exercice 8
Écrivez une classe **Entrepot** avec l'attribut *hauteurPlafond*
Un nouveau taux est créé (tauxC à 1.2) et l'impôt d'un entrepot est `(TauxA * 3) / 2 × surface + TauxC × hauteurPlafond`
Dans la méthode ```main```, créé 1 entrepôt et ajouter le au cadastre

> Pensez a faire un commit !!

### Exercice 9
Écrivez une classe **Personne**. Une personne a un *nom* et un *prénom*.  
Ajouter le constructeur et la méthode ```String toString().```

> Pensez a faire un commit !!

### Exercice 10
Les bâtiments ont un propriétaire.
Déclarer l'attribut **proprietaire** dans la classe appropriée, modifier le ou les constructeurs nécessaires et affichez le proprietaire dans ```String toString().```
Dans la méthode ```main```, créer 2 personnes pour qu'elles soient propriétaires des maisons et appartements

> Pensez a faire un commit !!


## Problème 2

Les fichiers de ce problème sont à créer dans le package `net.lecnam.ussi47.probleme2`

*Librement adapté de http://tdinfo.phelma.grenoble-inp.fr/2Apoo/td/tp4.pdf*

On vous demande de réaliser une ébauche d'application pour gérer un zoo

Un zoo contient des animaux avec les propriétés suivantes :  
– Chimpanzé : Végétarien, 3kg de fruits/jour  
– Autruche : Végetarien, 5kg de fruits/jour  
– Aigle : Carnivore, 1 kg de viande/jour  
– Orque : Carnivore, 70 kg de viande/jour  
– Tigre du Bengale : Carnivore, 10 kg de viande/jour  
– Tigre Blanc : Carnivore, 10 kg de viande/jour  

Chaque animal a un nom et un coût par jour :  
– pour un carnivore : (quantite de nourriture + 0.1)^2 / 5  
– pour un végétarien : 4.2 ∗ log((quantite de nourriture + 100) ∗ 2 + 1)  

On doit pouvoir afficher le détail d'un animal (nom, quantité de nourriture et cout)

Un zoo a un nom, des animaux et un budget quotidien maxi. Quand on ajoute un nouvel animal, il ne faut pas que le budget quotidien soit dépassé, sinon, ça affiche un message.

On doit pouvoir récupérer le cout total quotidien du zoo et afficher la liste des animaux du zoo

#### Ecrire sur ordinateur le programme nécessaire pour répondre à ces spécifications
