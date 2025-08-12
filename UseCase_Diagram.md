# Diagrammes UML du Projet makeTICeasy

## 1. Diagramme de Cas d'Utilisation

```mermaid
graph TD
    actor_unauth[Utilisateur Non Authentifié]
    actor_student[Élève]
    actor_teacher[Enseignant]
    actor_admin[Administrateur]

    subgraph Système makeTICeasy
        uc_view_home(Voir Page d'Accueil)
        uc_view_catalog(Voir Catalogue de Cours)
        uc_register(S'inscrire)
        uc_login(Se Connecter)
        uc_logout(Se Déconnecter)

        uc_view_student_dashboard(Voir Tableau de Bord Élève)
        uc_track_progress(Suivre Progression)
        uc_take_lesson(Suivre une Leçon)
        uc_take_quiz(Passer un Quiz)
        uc_view_badges(Voir Badges)
        uc_view_assignments(Voir Devoirs)
        uc_submit_assignment(Soumettre un Devoir)

        uc_view_teacher_dashboard(Voir Tableau de Bord Enseignant)
        uc_manage_classes(Gérer Classes)
        uc_manage_assignments(Gérer Devoirs)
        uc_view_student_progress(Voir Progression Élèves)
        uc_create_assignment(Créer un Devoir)
        uc_grade_assignment(Noter un Devoir)

        uc_view_admin_dashboard(Voir Tableau de Bord Admin)
        uc_manage_users(Gérer Utilisateurs)
        uc_manage_courses(Gérer Cours)
        uc_manage_system(Gérer Paramètres Système)
    end

    actor_unauth --> uc_view_home
    actor_unauth --> uc_view_catalog
    actor_unauth --> uc_register
    actor_unauth --> uc_login

    actor_student --> uc_login
    actor_student --> uc_logout
    actor_student --> uc_view_student_dashboard
    actor_student --> uc_view_catalog
    actor_student --> uc_track_progress
    actor_student --> uc_take_lesson
    actor_student --> uc_take_quiz
    actor_student --> uc_view_badges
    actor_student --> uc_view_assignments
    actor_student --> uc_submit_assignment

    actor_teacher --> uc_login
    actor_teacher --> uc_logout
    actor_teacher --> uc_view_teacher_dashboard
    actor_teacher --> uc_manage_classes
    actor_teacher --> uc_manage_assignments
    actor_teacher --> uc_view_student_progress
    actor_teacher --> uc_create_assignment
    actor_teacher --> uc_grade_assignment

    actor_admin --> uc_login
    actor_admin --> uc_logout
    actor_admin --> uc_view_admin_dashboard
    actor_admin --> uc_manage_users
    actor_admin --> uc_manage_courses
    actor_admin --> uc_manage_system

