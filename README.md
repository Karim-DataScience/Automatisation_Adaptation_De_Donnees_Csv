# Automatisation et Adaptation de Données CSV
## Contexte
J'ai eu besoin d'automatiser une tache, répétitive, donc programmable.
## Explications du code
Ce code utilise la bibliothèque Pandas pour lire un fichier CSV nommé "ville_commerce.csv" et pour créer des DataFrame.

Il commence par ouvrir le fichier et enregistrer son encodage dans la variable "encoding". Ensuite, il utilise la fonction "pd.read_csv" pour lire le fichier en utilisant le séparateur ";" et l'encodage enregistré précédemment. Le résultat est stocké dans la variable "df".

Ensuite, il sélectionne différentes colonnes du fichier original et les répète 23 fois chacune en utilisant la méthode "repeat()" de Pandas. Ces colonnes répétées sont ensuite concaténées en une seule DataFrame appelée "principal".

Il y a ensuite une liste de noms de magasins "Commerce" qui est utilisée pour sélectionner les colonnes correspondantes dans le fichier original. Ces colonnes sont concaténées en une seule DataFrame appelée "Nbrs_Commerce".

Ensuite, il crée une liste de valeurs "val_list" pour les types de magasins et utilise une boucle "for" pour créer 23 DataFrames, chacun contenant un type de magasin répété 33800 fois. Ces DataFrames sont ensuite concaténés en un seul DataFrame appelé "result".

Enfin, il utilise la méthode "reset_index()" pour réinitialiser les index des DataFrames "principal", "Nbrs_Commerce" et "result" et les concatène en utilisant la méthode "pd.concat()". Le résultat final est stocké dans "merged_df" et enregistré dans un fichier CSV en utilisant la méthode "to_csv()".
