# Transformers
Objectif du projet:

L'objectif de ce projet était de construire et d'entraîner un modèle de traduction automatique simple utilisant une architecture Transformer. Le modèle est conçu pour traduire de courtes phrases d'anglais vers le français en utilisant un petit ensemble de données d'exemples de traduction.

Étapes réalisées :

Installation des dépendances: Les bibliothèques nécessaires (torch, numpy, tqdm) ont été installées. Préparation des données: Un petit ensemble de paires de phrases anglais-français a été créé. Cet ensemble de données a été étendu par duplication et mélange pour obtenir environ 1000 exemples. Un SimpleTokenizer a été implémenté pour convertir les phrases en séquences d'identifiants de mots, incluant des tokens spéciaux (, , , ). Une classe TranslationDataset a été définie pour préparer les données pour l'entraînement, y compris l'encodage des phrases et le padding à une longueur maximale. Un DataLoader a été créé pour charger les données par lots pendant l'entraînement. Définition du modèle: Un modèle Transformer simple a été défini à l'aide de PyTorch, comprenant des couches d'embedding, un encodage positionnel et des couches d'encodeur-décodeur Transformer standard. Entraînement du modèle: La fonction de perte CrossEntropyLoss et l'optimiseur Adam ont été configurés. Le modèle a été entraîné sur l'ensemble de données préparé pendant 20 époques. La perte d'entraînement a été suivie à chaque époque, montrant une diminution significative au fil du temps, ce qui indique que le modèle apprend. Résultats de l'entraînement :

La perte d'entraînement a diminué de manière constante sur les 20 époques. La perte finale d'environ 0.0034 suggère que le modèle a bien appris l'ensemble de données limité et est capable de prédire les séquences cibles avec une grande précision sur cet ensemble de données.

Inférence :

Une fonction translate a été définie pour utiliser le modèle entraîné afin de générer des traductions pour de nouvelles phrases d'entrée. Les exemples de test montrés ("Bonjour" et "Merci") ont produit les traductions attendues ("bonjour" et "bonjour" - notez que la traduction de "Merci" semble erronée dans l'exemple fourni dans le notebook, ce qui pourrait indiquer une limitation du modèle sur un ensemble de données aussi petit).

Prochaines étapes possibles :

Utiliser un ensemble de données de traduction plus grand et plus diversifié pour améliorer les performances et la généralisation du modèle. Ajouter des mécanismes d'attention plus sophistiqués au modèle Transformer. Mettre en œuvre un processus de validation pour évaluer les performances du modèle sur des données invisibles pendant l'entraînement. Expérimenter différents hyperparamètres (taille du modèle, nombre de couches, taux d'apprentissage, etc.). Déployer le modèle pour une utilisation pratique. Ce rapport résume les principales composantes et les résultats de ce projet de traduction automatique.
