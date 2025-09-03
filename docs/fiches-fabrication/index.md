# Fiches de Fabrication HACCP - Méthode Optimale

Les fiches de fabrication sont la mise en application concrète de la méthode HACCP pour nos recettes. Elles transforment une recette de cuisine en une procédure de travail sûre et reproductible.

Chaque fiche détaille :
- Les ingrédients et leur origine
- Le déroulement des opérations sous forme de diagramme
- Les points de maîtrise et les CCP (Points Critiques) avec leurs limites

## Comment lire les diagrammes ?

Les diagrammes de fabrication permettent de visualiser rapidement le processus. Une attention particulière doit être portée aux étapes critiques, les étapes notées en rouge.

## Code Couleur et Symbolique

| Type d'étape | Apparence | Signification |
|--------------|-----------|---------------|
| **Étape normale** | Rectangle bleu clair | Opération standard de fabrication |
| **CCP (Point Critique)** | Rectangle rouge avec bordure épaisse | Contrôle obligatoire pour la sécurité ★ |
| **Contrôle qualité** | Rectangle vert | Vérification ponctuelle |
| **Porte qualité** | Rectangle vert foncé | Validation avant passage à l'étape suivante |
| **Attente/Retravail** | Rectangle orange | Pause ou correction dans le processus |

## Modèle de Diagramme de Fabrication

```mermaid
flowchart TD
    %% Définition des styles pour les différents types d'étapes
    classDef normal fill:#e1f5fe,stroke:#64b5f6,color:#000,stroke-width:1px
    classDef ccp fill:#ffcdd2,stroke:#f44336,color:#000,stroke-width:3px,font-weight:bold
    classDef controle fill:#c8e6c9,stroke:#4caf50,color:#000,stroke-width:1px
    classDef attente fill:#fff3e0,stroke:#ff9800,color:#000,stroke-width:1px
    classDef qualite fill:#e8f5e8,stroke:#2e7d32,color:#000,stroke-width:2px,dashArray:5 5

    %% Processus de fabrication optimal
    A[Réception ingrédients<br/>Vérification fournisseurs]:::normal --> B[/Contrôle documentaire<br/>Traçabilité/]:::qualite
    B --> C[Stockage<br/>Conditions requises]:::normal
    C --> D[(PRÉPARATION CRITIQUE ★ CCP1<br/>Température < 5°C<br/>Durée max 30min)]:::ccp
    D --> E[/Contrôle température<br/>Visuel/]:::controle
    E --> F[Cuisson<br/>T°=75°C pendant 2min]:::normal
    F --> G[(CONSERVATION CRITIQUE ★ CCP2<br/>Chaîne du froid<br/>T° < 8°C)]:::ccp
    G --> H[/Contrôle final<br/>Goût/Odeur/Aspect/]:::qualite
    H --> I[Conditionnement<br/>Emballage]:::normal
    I --> J[(STOCKAGE FINI ★ CCP3<br/>T° 0-4°C<br/>DLUO respecté)]:::ccp

    %% Gestion des non-conformités
    E -- Conforme --> F
    E -- Non conforme --> E1[Rejet lot ★ CCP4<br/>Incident qualité]:::ccp

    H -- Conforme --> I
    H -- Non conforme --> H1[Analyse<br/>Destruction]:::attente
```

# Identification des Points Critiques

Les CCP sont identifiés selon les critères suivants :

## 1. Risques microbiologiques
- Températures dangereuses (zone 5-65°C)
- Temps d'exposition prolongé
- Manutention sans protection

## 2. Risques physiques
- Étapes de découpe/tranchage
- Utilisation d'équipements lourds
- Manipulation de produits chauds

## 3. Risques chimiques
- Utilisation d'additifs alimentaires
- Nettoyage/assainissement
- Conservation avec produits chimiques

## 4. Critères de validation
- Impact direct sur la sécurité consommateur
- Non-détection possible en étape ultérieure
- Mesure objective possible
- Limites clairement définies

# Informations obligatoires pour chaque CCP

Chaque CCP identifié doit comporter :
- ★ CCP + Numéro (identification claire)
- Limite critique (température, temps, pH, etc.)
- Méthode de surveillance
- Fréquence de contrôle
- Personne responsable
- Actions correctives prévues