<!-- .slide: class="sfeir-basic-slide" -->
# Le rôle d'un formulaire
<br><br>
<div class="flex-row">
    <ul>
        <li>Collecter de données utilisateur</li><br>
        <li>Valider les données saisies par les utilisateurs</li>
    </ul>
    <img alt="h-600 center" src="assets/images/school/forms/google_forms.png">
</div>

##==##

<!-- .slide: class="transitions-white sfeir-bg-pink" -->
# Collecter des données

##==##

<!-- .slide: class="sfeir-basic-slide" -->
# Un directive magique: v-model
<div>
    <div>Permet de réaliser un</strong>two-way databinding</strong></div><br><br>
    <img alt="center" src="assets/images/school/forms/v-model_basic.png">
</div>
Notes: 
 - un changement detéection two bbinding permet de rélaiser une liaison vue-controller controller-vue:
  - Si le template est modifié automatique le controlleur en est répercuté
  - Si le controlleur est modifié automatique le template en est répercuté

##==##

<!-- .slide: class="sfeir-basic-slide" -->
# L'utilisation de v-model
<br><br>
<div>
    <ul>
        <li>Placement de cette directive sur input, textarea, checkbox, radio, select et composants</li>
        <li>Peut être combiner avec v-for pour lister les options (select box)</li>
        <li>Utilisation de v-bind pour associer des valeurs dynamique (radio / checkbox)</li>
    </ul>
    <div class="flex-row">
        <img src="assets/images/school/forms/checkbox.png">
        <img src="assets/images/school/forms/radio.png">
    </div>
</div>

##==##

<!-- .slide: class="sfeir-basic-slide" -->
# Les modifiers de v-model
<br><br>
<ul>
    <li>lazy => changement de stratégie de synchronisation</li>
    <li>number => caster obligatoirement en number</li>
    <li>trim => éliminer les espaces superflus</li>
</ul>
<br><br>
<img alt="center" src="assets/images/school/forms/v-model_modificators.png">

##==##

<!-- .slide: class="sfeir-bg-pink exercice" -->
## Exercice
<br>
<ul>
    <li>Créer un composant monofichier Form.vue</li>
    <li>Appeler ce composant dans People.vue</li>
    <li>Propager les events cancel et save au People.vue</li>
    <li>Implémenter la méthode add dans People.vue au moment de l'event save</li>
</ul>
Notes:
 - Le composant People.vue a été aggrementé de deux méthodes showDiaolog et hideDialog
 - style, html du formulaire se trouve dans le dossier src/_static 
 - un bouton pour afficher la modal du formulaire a été ajouté
 - Api à utiliser pour sauvegarder une personne => http://localhost:9000/api/peoples/ (pensez à implémenter une méthode create dans le fichier service people)

 ##==##

 <!-- .slide: class="sfeir-bg-blue exercice" -->
 ## Solution
 <span class="full-center">localhost:8080/step11_solution</span>

 ##==##

 <!-- .slide: class="sfeir-bg-pink exercice" -->
 ## Exercice
<ul>
    <li>Créer un composant monofichier Update (dans le dossier views)</li>
    <li>Mettre à jour le ficher router.js (#/edit/:id)</li>
    <li>Réaliser la navigation vers l'update au click sur l'icon pencil de CardPanel.vue</li>
    <li>Dans le Hook beforeRouteEnter, penser à récupérer l'id et récupérer le détail d'une personne (Update.vue)</li>
</ul>
Notes: 
 - Penser à créer une methode fecthOne dans le people service
 - api à utiliser http://localhost:9000/api/peoples/:id (GET)

 ##==##

 <!-- .slide: class="sfeir-bg-pink exercice" -->
 ## Exercice
<ul>
    <li>Utiliser Form.vue dans Update.vue</li>
    <li>Passer la personn récupéré au composant Form.vue (props)</li>
    <li>Créer une computed method editMode qui prend true comme valeur quand on est dans le cas d'un update</li>
    <li>Propager l'event save dans Update.vue pour modifier une personne</li>
</ul>
Notes: 
 - si il y a une personne alors editMode true, si pas de personne editMode false (formulaire de création)
 - Penser à créer une méthode update dans le fichier people service
 - api:  http://localhost:9000/api/peoples/:id (PUT)

 ##==##

 <!-- .slide: class="sfeir-bg-blue exercice" -->
 ## Solution
 <span class="full-center">localhost:8080/step12_solution</span>