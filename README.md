# cours-Big Data-2026





## 🚀 Guide de démarrage : Votre environnement Spark en 1 clic

Pour ce cours, nous allons utiliser **GitHub Codespaces**. Cela vous évite d'installer Java, Python ou Spark sur votre propre ordinateur. Tout se passe dans votre navigateur.

### Étape 1 : Préparer votre dépôt

1. Connectez-vous à votre compte **GitHub**.
2. Allez sur le dépôt du cours fourni par l'enseignant.
3. Cliquez sur le bouton vert **[ <> Code ]** en haut à droite.
4. Sélectionnez l'onglet **Codespaces**, puis cliquez sur **Create codespace on main**.

### Étape 2 : Initialisation (Patientez 2 minutes)

* Une nouvelle fenêtre s'ouvre avec une interface identique à **VS Code**.
* Le système installe automatiquement **Java** et **PySpark** (grâce au fichier `.devcontainer` que j'ai configuré).
* *Note :* La première fois, cela peut prendre 1 à 2 minutes. Les lancements suivants seront instantanés.

### Étape 3 : Créer votre premier Notebook

1. Dans l'explorateur de fichiers à gauche, faites un clic droit et créez un nouveau fichier nommé `test_spark.ipynb`.
2. Dans la première cellule, copiez ce code de test :
```python
from pyspark.sql import SparkSession
spark = SparkSession.builder.appName("CoursBigData").getOrCreate()
df = spark.createDataFrame([("Apprenant", 1)], ["Statut", "OK"])
df.show()

```


3. Cliquez sur **Exécuter** (la petite flèche à gauche de la cellule).
4. Si on vous demande de choisir un "Kernel", sélectionnez **Python 3.10.x**.


### 💡 Astuces utiles pour les étudiants :

* **L'interface Spark :** Quand Spark tourne, une petite notification en bas à droite vous proposera d'ouvrir le port **4040**. Cliquez dessus pour voir l'interface Spark UI et surveiller vos calculs.
* **Arrêt du travail :** Codespaces s'arrête automatiquement si vous ne l'utilisez plus (votre travail est sauvegardé). Vous pourrez le reprendre plus tard via [github.com/codespaces](https://github.com/codespaces).
* **Quota :** Vous disposez de **60 heures gratuites par mois**, ce qui est largement suffisant pour ce module.

