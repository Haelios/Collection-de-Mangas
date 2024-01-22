# Collection-de-Mangas
Ce projet est un projet personnel sur un sujet qui me tient à coeur : les mangas.

## Partie 1 : Visualisation de ma collection
La première partie de ce projet consiste en un rapport/dashboard réalisé sur Power BI. C'est un outil que je n'avais pas eu l'occasion d'utiliser par le passé et je trouvais intéressant de l'implémenter dans ce projet afin de me familiariser avec.
J'ai donc préparer des visuels à partir de mon fichier de données, afin d'afficher et d'apprendre à connaître plus en détails ma propre collection, d'en ressortir les traits importants et tendances qui s'en dégagent afin de moi même comprendre les choses qui me plaisent.
J'avais notamment envie de m'intéresser au prix de ma collection, car je sais que certains prix ont sensiblement augmentés depuis que j'ai commencé à acheté des mangas, que je possède certains collectors qui ne sont actuellement plus édités, et je voulais donc un peu me rendre compte de la valeur de ce que je possédais, notamment en comparant les prix d'achats et le prix qu'il faudrait dépenser actuellement pour racheter ma collection.
Je me suis également intéressé aux répartitions en différentes catégories pour analyser mes préférences, les auteurs ou les éditeurs que je favorise, les genres et les formats, ainsi que l'évolution de ma consommation au fil des anneés.

## Partie 2 : Création d'un système de recommendation

Par la suite, j'ai décidé de créer et entraîner un modèle qui conseillerait de nouveaux mangas susceptibles de plaire en fonction de la liste des mangas précédemment lus. Pour cela j'ai du commencer par récupérer les données grâce à l'API de MyAnimeList.net. J'y ai scrap l'ensemble des données concernant les mangas existants, avec des informations telles que le nombre de personnes les ayant lu, les notes moyennes, les genres etc. J'ai ensuite été prendre les listes d'environ 30 000 utilisateurs afin d'entraîner mon modèle sur des cas existants, tout d'abord en utilisant uniquement les listes, c'est à dire uniquement ce qui a été lu chaque utilisateur, pour prédire mes résultats. Les résultats obtenus sur mon jeu de test personnel sont déjà très bon avec ce modèle assez simple.

J'ai ensuite essayé de créer un second recommender, en utilisant cette fois-ci Tensorflow et un modèle de Deep Learning, en associant les listes des utilisateurs avec les genres auxquels chaque manga appartient afin d'affiner la prédiction en utilisant les similarités entre utilisateurs et entre mangas.
