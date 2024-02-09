/*
 * Click nbfs://nbhost/SystemFileSystem/Templates/Licenses/license-default.txt to change this license
 */


package com.mycompany.mavenproject6;

import java.util.Scanner;

public class Mavenproject6 {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Administrateur administrateur = new Administrateur();

        int choix;

        do {
            System.out.println("Menu:");
            System.out.println("1. Ajouter un apprenant");
            System.out.println("2. Supprimer un apprenant");
            System.out.println("3. Consulter la liste des apprenants");
            System.out.println("4. Ajouter une classe");
            System.out.println("5. Supprimer une classe");
            System.out.println("6. Afficher la liste des classes");
            System.out.println("0. Quitter");
            System.out.print("Veuillez choisir une option : ");

            choix = scanner.nextInt();

            switch (choix) {
                case 1:
                    // Ajouter un apprenant
                    System.out.print("Nom de l'apprenant : ");
                    String nom = scanner.next();
                    System.out.print("Prénom de l'apprenant : ");
                    String prenom = scanner.next();
                    System.out.print("Numéro de classe de l'apprenant : ");
                    String numeroClasse = scanner.next();
                    Apprenant nouvelApprenant = new Apprenant(nom, prenom, numeroClasse);
                    administrateur.ajouterApprenant(nouvelApprenant);
                    break;
                case 2:
                    // Supprimer un apprenant
                    System.out.print("Nom de l'apprenant à supprimer : ");
                    String nomASupprimer = scanner.next();
                    System.out.print("Prénom de l'apprenant à supprimer : ");
                    String prenomASupprimer = scanner.next();
                    // Rechercher et supprimer l'apprenant
                    Apprenant apprenantASupprimer = administrateur.rechercherApprenant(nomASupprimer, prenomASupprimer, null);
                    if (apprenantASupprimer != null) {
                        administrateur.supprimerApprenant(apprenantASupprimer);
                    } else {
                        System.out.println("Apprenant non trouvé !");
                    }
                    break;
                case 3:
                    // Consulter la liste des apprenants
                    System.out.println("Liste des apprenants :");
                    administrateur.consulterListeApprenants();
                    break;
                case 4:
                    // Ajouter une classe
                    System.out.print("Numéro de classe : ");
                    String numeroClasseAjout = scanner.next();
                    System.out.print("Nom de la classe : ");
                    String nomClasse = scanner.next();
                    System.out.print("Effectif de la classe : ");
                    int effectifClasse = scanner.nextInt();
                    Classe nouvelleClasse = new Classe(numeroClasseAjout, nomClasse, effectifClasse);
                    administrateur.ajouterClasse(nouvelleClasse);
                    break;
                case 5:
                    // Supprimer une classe
                    System.out.print("Numéro de classe à supprimer : ");
                    String numeroClasseASupprimer = scanner.next();
                    // Rechercher et supprimer la classe
                    Classe classeASupprimer = administrateur.rechercherClasse(numeroClasseASupprimer);
                    if (classeASupprimer != null) {
                        administrateur.supprimerClasse(classeASupprimer);
                    } else {
                        System.out.println("Classe non trouvée !");
                    }
                    break;
                case 6:
                    // Afficher la liste des classes
                    System.out.println("Liste des classes :");
                    administrateur.afficherListeClasses();
                    break;
                case 0:
                    // Quitter le programme
                    System.out.println("Programme terminé.");
                    break;
                default:
                    System.out.println("Choix invalide. Veuillez réessayer.");
            }

        } while (choix != 0);
    }
}



