graph TD
    subgraph Réception / Stockage
        A1[Pâte feuilletée] --> B1(Froid négatif)
        A2[Emmental râpé en sachet] --> B2(Froid positif)
        A3[Lardons] --> B2
        A4[Crème fraiche] --> B2
        A5[Œufs coquilles frais] --> B2
        A6[Lait UHT (Non ouvert)] --> B3(Température ambiante)
        A7[Assaisonnements] --> B3
    end

    subgraph Mise en place
        B1 -- "cf. fiche pâte feuilletée" --> C1(Décongélation)
        C1 --> C2(Façonnage)
        B2 -- Lardons --> C3(Cuisson)
        B2 -- Œufs --> C4(Cassage)
    end

    subgraph Assemblage
        B2 -- Emmental --> D1(Garnissage)
        C3 --> D1
        subgraph Appareil
            C4 -- Œufs --> D2(Mélange)
            B2 -- Crème fraiche --> D2
            B3 -- Lait, Assaisonnements --> D2
        end
        D2 --> D1
    end

    subgraph Cuisson / Refroidissement
        C2 --> E1(Cuisson (180°C : 30-45 min))
        D1 --> E1
        E1 --> E2(Refroidissement)
    end

    E2 --> F1(Maintien au froid)
    F1 --> G1(Remise au client)
    F1 --> G2(Réchauffage)
    G2 --> G1