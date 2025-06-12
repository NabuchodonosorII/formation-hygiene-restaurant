graph TD
    subgraph Réception / Stockage
        A1[Viande égrenée surgelée] --> B1(Froid négatif)
        A2[Fromage râpé] --> B2(Froid positif)
        A3[Beurre] --> B2
        A4[Farine] --> B3(Température ambiante)
        A5[Lait] --> B3
        A6[Lasagnes] --> B3
        A7[Coulis de tomate (conserve)] --> B3
        A8[Assaisonnement] --> B3
        A9[Ail, oignon] --> B3
    end

    subgraph Mise en place
        B1 -- Viande --> C1(Cuisson (90°C : 10 min))
        B3 -- Ail, oignon --> C2(Epluchage)
        C2 --> C3(Hachage)
        C1 --> C4(Assemblage)
        C3 --> C4
        B3 -- Coulis de tomate --> C5(Déconditionnement)
        C5 --> C4
        B3 -- Assaisonnement --> C4
    end

    subgraph Béchamel
        B3 -- Lait, Farine --> D1(Fabrication béchamel : Cuisson (90°C : 6 min))
        B2 -- Beurre --> D1
        B2 -- Fromage râpé --> D1
    end

    subgraph Montage / Cuisson
        C4 --> E1(Montage en température)
        D1 --> E1
        B3 -- Lasagnes --> E1
        E1 --> E2(Remise en température / Cuisson)
    end

    E2 --> F1(Refroidissement)
    F1 --> G1(Maintien au froid)
    G1 --> H1(Réchauffage)
    H1 --> I1(Maintien au chaud)
    H1 --> I2(Remise au client)