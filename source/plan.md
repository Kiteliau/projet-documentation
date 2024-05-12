(plan)=

# Plan 

:::{note}

Cette page décrit en gros les éléments qui doivent être présents dans la
documentation du projet.

:::

:::{contents}
:::

## Présentation du projet

Ce projet s'intitule "Who's comin' ?". Il permet donc, comme le nom le laisse suggérer, d'organiser et de gérer des événements entre proches. Tout utilisateur peut créer des événements, y inviter des proches et définir plusieurs tranches horaires, afin de laisser voter les invités pour leurs présences. Ces derniers peuvent donc répondre au sondage en spécifiant leur présence pour chacune des tranches horaires de l'événement, pour enfin définir la date finale qui convient au plus d'invités possible. Les événements sont classés en trois différentes catégories :

- Non lus = l'utilisateur n'a pas encore répondu au sondage
- En attente = l'utilisateur a répondu mais attend que tous les autres invités aient répondu
- Programmés = tous les invités ont répondu au sondage, la date finale est programmée.

L'idée était de créer une alternative à Doodle, site qui devenait très compliqué d'utilisation et trop complexe pour ce à quoi il servait.

## Manuel / conseils d'utilisation

Utilisation d'un hébergeur Web en local (tel que WAMP pour Windows ou AMPPS pour Mac).

Comptes utilisateurs :
Des comptes fictifs ont été créés afin d'améliorer l'expérience d'un utilisateur test. Pour découvrir l'application, vous pouvez utiliser mon login (latintelco@hotmail.com). Tous les utilisateurs ont leur propre login visible dans la base de données, sous la table t_utilisateur, et tous les mots de passe sont 123123.

Liste des proches : Pour ajouter des proches, l'utilisateur doit se rendre dans l'onglet 'Proches' et rechercher des proches en utilisant la barre de recherche. Cette dernière va rechercher selon les noms, prénoms et emails des autres utilisateur de la base de données. Pour ajouter un proche à sa liste, l'utilisateur doit simplement appuyer sur le bouton 'Ajouter' figurant dans la liste des résultats de la recherche.

Fonctionnement des événements : Lors de la création d'un événement, son auteur doit définir différentes informations textuelles telles que son titre et sa description. Puis, il peut créer plusieurs tranches horaires auxquelles il est disponible et ainsi laisser plusieurs options pour les invités. Ces tranches horaires concernent un seul jour, d'une heure de début à une heure de fin. L'auteur peut ensuite ajouter des invités depuis sa liste de proches (seuls les proches de l'auteur peuvent être invités à l'événement). Lors de la validation de l'événement, ce dernier sera créé et affiché dans la liste des événements de tous les utilisateurs invités, et l'auteur pourra regarder l'état des votes en temps réel.

Système de votes : Après la création de l'événement, celui-ci sera affiché pour tous les invités. Ces derniers pourront donc voter en utilisant le menu d'informations de l'événement (simplement en cliquant dessus). Pour chaque tranche horaire, l'invité pourra sélectionner s'il est disponible ou non, et utilisera le bouton 'Sauvegarder' pour valider ses votes. L'auteur ainsi que les invités pourront alors constater les nouveaux taux de présence pour chaque tranche horaire (calculés selon le nombre de votes positifs et nombre de votes totaux, les utilisateurs n'ayant pas encore répondu sont omis). Tant que tous les invités n'ont pas répondu, n'importe quel invité ayant déjà répondu au sondage peut modifier ses votes. Aussitôt que tous les invités ont répondu au sondage, la tranche horaire qui a le plus haut taux de vote (en cas d'égalité, celle la plus proche de la date du jour) est définie comme date finale de l'événement, et cette dernière ne peut plus être changée.

Premiers pas : Après avoir pris connaissance les différentes fonctionnalités avec l'utilisateur de test, le plus simple est de créer un nouveau compte (via la page d'inscription), de rechercher et d'ajouter des proches depuis l'onglet 'Proches', et finalement de créer un événement avec différentes tranches horaires et invités. Puis, pour tester le système de votes, utilisez le compte d'un invité de l'événement pour accéder à l'interface de vote.

## Explication du fonctionnement du code

Cette partie peut contenir plusieurs chapitres (entrées dans la `toctree` du
fichier `source/index.rst`). Elle doit contenir les éléments suivants

- Travail effectué par chacun des membres pour les binômes. Cela peut se faire
  en indiquant les fonctionnalités développées par chacun et les fichiers
  concernés

- Principaux fichiers, en particulier le **point d'entrée** (*entry point*), à
  savoir le fichier principal.

- Brève présentation des concepts fondamentaux et spécifiques utilisés dans le
  projet (exemple : WebSockets, programmation asynchrone, framework /
  technologies, ...)

- Explication d'au moins parties du code source qui sont plus difficiles à
  comprendre

- Présentation d'un élément qui a créé des difficultés et les solutions
  envisagées / trouvées.

## Regard critique et améliorations

- Dans cette partie, vous jetez un retard critique sur votre projet, en
  particulier par rapport aux objectifs initiaux. 

- Si vous estimez ne pas avoir réussi à satisfaire le cahier des charges initial
  (objectifs initiaux), évoquez brièvement les difficultés rencontrées qui vous
  en ont empêché et les éventuelles solutions que vous pourriez mettre en place
  pour atteindre les objectifs.

## Ce que vous avez appris

- Expliquez brièvement ce que vous avez appris en réalisant votre projet (au
  niveau technologique, conceptuel, gestion de projet, autres, ...)