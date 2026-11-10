# School Notes

Petite application Android pour gérer des élèves et leurs notes, pour s'exercer à Jetpack Compose et à la base de données locale Room.

## Fonctionnalités

- Ajouter un élève par son nom
- Afficher la liste des élèves en direct
- Donner une note aléatoire à un élève et voir l'ensemble de ses notes

## Technologies

- Kotlin
- Jetpack Compose et Material 3
- Room (base de données locale) avec KSP
- Coroutines et `Flow`, pour que l'affichage se mette à jour dès que les données changent
- SDK minimum 24

## Modèle de données

```
Student (studentId, name)
Grade   (gradeId, ownerId -> Student, value)
```

Une note est liée à un élève. La suppression d'un élève supprime ses notes (`CASCADE`).

## Structure

```
app/src/main/java/com/example/schoolnote/
  MainActivity.kt    interface Compose
  SchoolSchema.kt    entités, DAO et base Room
```

## Lancer le projet

1. Cloner le dépôt :
   ```bash
   git clone https://github.com/imene-be/school-notes-android.git
   ```
2. L'ouvrir avec **Android Studio**.
3. Laisser Gradle se synchroniser, puis lancer sur un émulateur ou un téléphone (Android 7.0 minimum).

---

Réalisé par [Imène Bentifraouine](https://imenebe.fr).
