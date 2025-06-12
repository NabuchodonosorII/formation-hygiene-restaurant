graph TD
    subgraph Réception / Stockage
        A1[Œufs coquille extra-frais] --> B1(Froid positif)
        A2[Sucre] --> B2(Température ambiante)
        A3[Chocolat] --> B2
    end

    subgraph Mise en place
        B1 -- Oeufs --> C1(Cassage)
        C1 --> C2(Clarification)
        C2 --> C3(Réservation des blancs d'œufs)
        C3 --> D1(Monter à la neige)

        B2 -- Chocolat --> C4(Cassage)
        C4 --> D2(Fusion au bain marie)
    end

    subgraph Techniques culinaires
        D2 --> E1(Mélange)
        B2 -- Sucre --> E1
        E1 --> E2(Incorporation des blancs)
        D1 --> E2
        E2 --> E3(Refroidissement)
    end

    E3 --> F1(Maintien au froid)
    F1 --> G1(Remise au client)