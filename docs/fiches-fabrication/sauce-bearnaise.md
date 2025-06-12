graph TD
    subgraph Réception / Stockage
        A1[Beurre] --> B1(Froid positif)
        A2[Œufs coquilles EXTRA FRAIS] --> B1
        A3[Echalotes] --> B2(Température ambiante)
        A4[Plantes aromatiques] --> B2
        A5[Assaisonnement] --> B2
        A6[Vin, vinaigre] --> B2
    end

    subgraph Mise en place
        B1 -- Beurre --> C1(Clarification)
        B1 -- Œufs --> C2(Cassage)
        C2 --> C3(Clarification)
        C3 --> C4(Réservation des jaunes)
        B2 -- Echalotes --> C5(Epluchage)
        C5 --> C6(Hachage)
        B2 -- Plantes aromatiques --> C7(Lavage/égouttage)
        C7 --> C8(Hachage)
    end

    subgraph Techniques culinaires
        B2 -- Assaisonnement, Vin, vinaigre --> D1(Réduction)
        C6 --> D1
        C8 --> D1
        D1 --> D2(Refroidissement)
        D2 --> D3(Cuisson à basse température)
        C4 --> D3
        C1 --> D3
    end

    D3 --> E1(Maintien au chaud)
    D3 --> E2(Utilisation directe)