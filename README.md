De vuejs.org, création de la librairie "vue2.6.12.js" en la copiant et collant dans le script html  

npm init (qui crée le package.json) pour pouvoir installer notre serveur "npm install lite-server"
rajout dans le package.json : "start": "lite-server" d'ou npm start...pour lancer lite-server

chrome vue js (pour pouvoir suivre ds la console)

***************************************************************************************
Index
***************************************************************************************

* index1.html:
two way binding 'v-model':
 data vers la div du body (v-bind) | chemin inverse (v-model)

* index2.html: TodoApp
*Gerer les events via les 'methods' de l'instance new vue
*Method 'push' | ds data creation de 'tasks' []

* index3.html: 
Soumission d'un form
.event: pour ne pas rafraichir tte la page

Parcours d'un []
On aimerait pouvoir voir les taches ajouter sr la page
v-for en itérant (et ul li ) d'ou gestion dynamique

* index4.html: Parcours d'un {[]}
changement de la method et rajout infos dans le li

* index5.html : Ajouter une class CSS conditionnellement

* index6.html : Afficher du contenu HTML conditionnellement
On se servira de la librairie "font awsome"
switchMode | v-if, v-else

Gerer les evenements du clavier v-on:keyup: 

Gerer la suppression d'une tache (v-on:click="deleteTask")
filter: on passe en revue chaque 'tache' et pr chaque 'tache' passée en revue...

* hooks.html: utilisation de l'API jsonplaceholder.com
Life cycle hooks : https://fr.vuejs.org/v2/guide/instance.html

On utilise axios soit pr ligne de cde (npm i axios) soit pr un CDN

*****************************************************************************************
Components global | local
*****************************************************************************************

* components global.html

* components local.html

* componentlocal1.html : Ajouter des données à un composant enfant
une data est produite avec une fonction qui retourne un {}

* componentslocal2.html : Ajouter des méthodes à un composant enfant
Le click sur le button n'impact que le composant concerné

* componentslocal3.html : Passer des données d'un composant parent à un composant enfant
var vm : composant parent | var myCmp : composant enfant (bien regardé son template...)

* componentslocal4.html : Passer le result d'une req Ajax effectué par le parent à son enfant 
On pourra vérifier dans le navigateur vue

* componentslocal5.html : Organisation en hierarchie de composants

* componentslocal6.html : Insérer du contenu entre les tags dun composant à l'aide des slots

* componentslocal7.html : Emettre un custom "event" depuis un composant enfant et le gerer dans le composant parent
Av: Les méthods reste ds le parent au lieu de s'éparpiller ds l'enfant , couplage faible entre composant, ce qui est conforme aux bonnes pratiques
Du composant usr-details, on va ajouter un bouton "accepter une invite" par exemple

* componentslocal8.html : Afficher dans le parent les composants petits enfants qui ont emis un event
On souhaite afficher les utilisateurs qui ont accepter l'invite via un v-for (plutot dans le composant racine que dans le composant parent)
passer en tant que props v-bin:users-coming

* componentslocal9.html : Pré-rendu et rendu d'un tableau d'{}
v-for="user in usersWhoWillCome" (on itère sur un tableau d'objet)

*******************************************************************************
DIVERS
********************************************************************************

* divers1.html : Créer un filtre

* divers2a.html : computed properties (sans le computed)
charge trop vite , undefined ! , ne marchera donc pas !

* divers2b.html : computed properties (avec le computed)

* divers3.html Activer/Desactiver un bouton en fct de la valeur d'une computed property
Exemple de s'inscrire à une newsletter
récupérer une variable à partir de v-model (email), utilisation de regex...

* divers4.html : Surveiller le contenu d'un champ texte à l'aide d'un watcher
Ex: Donner à l'utilisateur son avis, filter les messages d'insultes..., surveiller des saisies dans le champ texte, les watcher sont idéals!
Ajout de la propiété watch (lié à 'opinion' dans html)
Le watcher executera bien la logique (if else ) mise en place

* divers5a.html : Requetes asynchrones et watcher couplé à debounce pr filtrer ls requetes
watcher péréféré!!! à computed ds le cas de requetes asynchrones.
On va donc "requeter" sur l'API de github

* divers5b.html : Requetes asynchrones et watcher couplé à debounce pr filtrer ls requetes
En utilisant la fonction "debounce", on utiValérie Cauro lisera moins de bande passante lors des requetes
On télechargera le CDN de lodash (librairie qui comporte beaucoup de fonction utilitaire dont 'debounce')
Reduire le nombre de requetes asynchrone 
(solution autre que le CDN, la cde: npm i --save lodash.debounce)

