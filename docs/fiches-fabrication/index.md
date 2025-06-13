# Section : Fiches de Fabrication

Les fiches de fabrication sont la mise en application concrète de la méthode HACCP pour nos recettes. Elles transforment une recette de cuisine en une procédure de travail sûre et reproductible.

Chaque fiche détaille :
- Les ingrédients et leur origine.
- Le déroulement des opérations sous forme de diagramme.
- Les points de maîtrise et les CCP (Points Critiques) avec leurs limites.

## Comment lire les diagrammes ?

Les diagrammes de fabrication permettent de visualiser rapidement le processus. Une attention particulière doit être portée aux étapes colorées :


graph TD
    A[Étape normale] --> B;
    B{Étape de contrôle critique (CCP)} --> C;
    C[Étape finale]

    style B fill:#ff9999,stroke:#333,stroke-width:2px



- **Les boîtes blanches** représentent les étapes de fabrication standards.
- **Les boîtes rouges (CCP)** représentent un **Point Critique de Contrôle**. C'est une étape où une perte de maîtrise entraîne un risque inacceptable pour le consommateur. Elle doit être surveillée et enregistrée.