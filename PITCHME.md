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
|                        |                                                                                                                       |
|------------------------|-----------------------------------------------------------------------------------------------------------------------|
|Nowly                   | "papa" d'Aintro                                                                                                       |
|Aintro                  |![Aintro](https://lh3.googleusercontent.com/qF77BoA8pwfNvAtIYKzgN3d23EJE8WVjDtfHeVbcdmE6jKtP3pN5Dq67T-bwCmXqSA=w300-rw)|
|et d'autres             | Files, Senseï...                                                                                                      |

+++

### Prestation :

| Satable | ![MacDO](https://heureu.com/wp-content/uploads/2016/10/redwire-singapore-ronald-macdonald-clown.jpg)|
|---------|-----------------------------------------------------------------------------------------------------|

+++

## Les outils de travail

* Bitbucket
* Jira + suite Fibonnaci
---?image=https://upload.wikimedia.org/wikipedia/commons/thumb/9/93/Fibonacci_spiral_34.svg/2000px-Fibonacci_spiral_34.svg.png
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

## Arborescence d'un projet vierge

![Arborescence](assets/images/arborescence_projet.png)
 
+++

## Vues, activités et fragments

* Vue : base des composants pour intéraction et l'interactivité. Placées dans des layout (xml)
* Exemple de vue : Button, TextView...
* Activité ~ une page et extends du Context.

+++

* Fragments : parties de l'écran.
* Destinés à être remplacés ou détruits.
* Constructeur par défaut uniquement.

+++

## Difficulté rencontrée

### Cycle de vie 

|Activité                                                                    |Fragment                                                                    |
|----------------------------------------------------------------------------|----------------------------------------------------------------------------|
|![Activity_life_transition](assets/images/activity_lifecycle_transition.png)|![Fragment_life_transition](assets/images/fragment_lifecycle_transition.jpg)|

---

# IV. Premier projet : Energetics