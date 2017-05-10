# Présentation du stage pour l'obtention du titre de Développeur Logiciel / Web
## Quentin DEBOVE
### CEFIM, Session 2016-2017

---

# Au programme 
### I. Introduction
### II. Environnement de travail
### III. Android
### IV. Premier projet : Energetics
### V. Second projet : refactorisation d'Aintro
### VI. Conclusion
### VII. Questions ?

---

# I. Introduction

### Milieu paramédical : réorientation
### Ambiance unique

---

# II. Environnement de travail

+++

## Le mame
![Map MAME](http://www.tech-orleans.fr/wp-content/uploads/2015/06/FAA_MAME_TOURS_EXTERIEUR_PARVIS_03.jpg)

+++

##NOWLY

+++

|Manysinn Thin                                                                                                                       |Jérome Heissler                                                                        |Mathieu Bolard                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
|![Many](https://media.licdn.com/mpr/mpr/shrinknp_400_400/AAEAAQAAAAAAAAh_AAAAJDQ3ZDlkYTIyLWE1MzctNDNlYy1hNmU5LWRlNmM2MWVkYjEzNw.jpg)|![Jerome](https://media.licdn.com/mpr/mpr/shrinknp_400_400/p/3/000/121/063/2ae3e5d.jpg)|![Mathieu](https://media.licdn.com/mpr/mpr/shrinknp_400_400/p/4/005/099/26e/3f6eca5.jpg)| 

+++

## Les projets / prestations de NOWLY

+++

### Projets :
|                        |                                   |
|------------------------|-----------------------------------|
|Nowly                   | "papa" d'Aintro                   |
|Aintro                  |![Aintro](https://raw.githubusercontent.com/qdebove/oral_stage/master/assets/images/Aintro.jpg)|
|et d'autres             | Files, Senseï...                  |

+++

### Prestation :

| Satable | ![MacDO](https://heureu.com/wp-content/uploads/2016/10/redwire-singapore-ronald-macdonald-clown.jpg)|
|---------|-----------------------------------------------------------------------------------------------------|

+++?image=https://upload.wikimedia.org/wikipedia/commons/thumb/9/93/Fibonacci_spiral_34.svg/2000px-Fibonacci_spiral_34.svg.png

## Les outils de travail

* Bitbucket
* Jira + suite Fibonnaci
* Slack

---

# III. Apprentissage d'Android

+++

## Présentation d'Android

* Système exploitation mobile basé sur noyau Linux.
* Développé par Google, lancé en 2007.
* 80% parts de marché dans le monde.

+++

## Versionning

* Noms de desserts et progression alphabétique
![Versionning](http://3.bp.blogspot.com/-xxixKWi26CU/VnuOg6Z3d7I/AAAAAAAAAuM/qBrHidasRm0/s1600/droid.jpg)

+++

## Java et Android

* V4.4 et inférieur : Dalvik
* Au delà : ART (Android RunTime)

+++

## Création d'un projet

* Deux fichiers importants : Gradle et Manifest
* Version de l'API importante !

+++

![Arborescence](assets/images/arborescence_projet.png)
 
+++

## Vue, activité et fragment

+++

### Vue

![Vues](assets/images/view_group.png)

+++

### Activité

* Activité ~ une page et extends du Context.
![Activités](assets/images/android-pass-data-to-activity.png)

+++

### Fragment

![Fragments](assets/images/android_fragments_d001_why_fragments.png)

+++

## La principale difficulté rencontrée

### Cycle de vie 

|Activité                                                                                                                                |Fragment                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
|![Activity_life_transition](https://raw.githubusercontent.com/qdebove/oral_stage/master/assets/images/activity_lifecycle_transition.png)|![Fragment_life_transition](https://raw.githubusercontent.com/qdebove/oral_stage/master/assets/images/fragment_lifecycle_transition.jpg)|

---

# IV. Premier projet : Energetics
![Logo_energetics](assets/images/Energetics_Logo.jpeg)

+++

## Présentation

* Marque exclusive Intersport.
* Souhaite une application tampon "vitrine".

+++

## Apercu charte graphique (non validée)

+++

![Charte_graphique_energetics](assets/images/charte_graphique_energetics.png)

+++

## Les grandes lignes du code

* Une classe Article.
* Création de 2 RecycleView.
* Un Singleton.

+++

### La classe Article

* Facilité d'accès aux informations.
* Impléments Serializable.
* CharSequence

+++

### Les RecycleView

|    |RecycleView                                       |ListView                                                          |
|----|--------------------------------------------------|------------------------------------------------------------------|
|Pro |ViewHolder, Animation, Performances, LayoutManager|Mise en place, petite liste, données simples (un seul TextView...)|
|Cons|API min 7, plus compliquée à mettre en place      |Mauvaise avec les collections, pas d'animations personnalisées    |

+++

![!](assets/images/06-recyclerviewer-adapter.png)

+++

### Le singleton

TODO

+++

## Les bonus

* Librairie Picasso
```java
Picasso.with(context).load("http://i.imgur.com/DvpvklR.png").into(imageView);
```
* L'effet de parallaxe : SensorManager.
* Bounce sur RecycleView.

+++

## Conclusion du projet

* Intégration difficile.
* Problème de mémoire.
* UX important.

---

# V.Second projet : Réfactorisation d'Aintro
![Logo_Aintro](assets/images/Aintro.jpg)

+++

## Présentation

* Expérience reposant sur géoloc.
* Matching prédictif.
* Connection par Twitter et récemment Linkedin.
* Problèmes majeurs : transition entre écrans pas fluide + une activité lancée à chaque nouvelle page

+++

## Les bibliothèques utilisées

* ButterKnife
```'*.java'
@OnClick(R.id.submit)
public void submit(View view) {
  // TODO submit data to server...
}
```
* Retrofit
```'*.java'
public interface GitHubService {
  @GET("users/{user}/repos")
  Call<List<Repo>> listRepos(@Path("user") String user);
}
```
* Dagger 2

+++

## Exemple d'utilisation de fragments

```'*.java'
InvitationFragment invitationFragment = new InvitationFragment();
getActivity().getSupportFragmentManager()
        .beginTransaction()
        .setCustomAnimations(R.anim.anim_in_left, R.anim.anim_out_right, R.anim.anim_in_right, R.anim.anim_out_left)
        .replace(R.id.nearby_activity_fragment, invitationFragment, "invitationFragment")
        .addToBackStack(null)
        .commit();
```

+++

## Conclusion du projet

* Lecture du code / compréhension
* Manque de commentaire
* Dagger 2

---?image=https://raw.githubusercontent.com/qdebove/oral_stage/master/assets/images/android_vs_apple.jpg

# <p style="color: white">VI. Conclusion</p>

* <p style="color: white">Un vrai plaisir de voir ses applications !</p>
* <p style="color: white">Plein de personnes / métiers différents.</p>
* <p style="color: white">Développement personnel d'une petite application de récupération de playlist youtube.</p>

---

# VII. Des questions ?

![Android_happy](assets/images/Android-Happy2-e1357315066858.jpg)