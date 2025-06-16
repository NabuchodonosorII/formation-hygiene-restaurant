``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Vinaigre] --> B1(Température ambiante)
        A2[Huile] --> B1
        A3[Moutarde <br> pot non entamé] --> B1
        A4[Assaisonnements] --> B1
        A5[Œufs extra-frais] --> B2(Froid positif)
    end

    subgraph Mise en place
        B2 --> C1(Cassage)
        C1 --> C2(Clarification)
        C2 --> C3(Réservation des jaunes)
    end

    subgraph Assemblage
        B1 -- Moutarde, Assaisonnements --> D1(Mélange)
        C3 --> D1
    end

    subgraph Techniques culinaires
        D1 --> E1(Début d'émulsion)
        B1 -- Huile --> E1
        E1 --> E2(Emulsion finale)
        B1 -- Vinaigre --> E2
    end

    E2 --> F1(Maintien au froid <br> <3 °C durant 24h maximum)
    F1 --> G1(Remise au client)
    F1 --> G2(Utilisation)
```