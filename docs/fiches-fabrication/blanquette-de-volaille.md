graph TD
    subgraph Réception / Stockage
        A1[Citron entier] --> B1(Froid positif)
        A2[Escalopes de volaille] --> B1
        A3[Champignons] --> B1
        A4[Beurre] --> B1
        A5[Crème fraiche] --> B1
        A6[Farine] --> B2(Température ambiante)
        A7[Fond de volaille, Assaisonnement] --> B2
    end

    subgraph Mise en place
        B1 -- Citron --> C1(Lavage)
        C1 --> C2(Pressage)
        B1 -- Escalopes --> C3(Découpe)
        B1 -- Champignons --> C4(Lavage / Egouttage)
        C4 --> C5(Découpe)
    end

    subgraph Cuisson
        C3 --> D1(Cuisson (80°C : 1h 20 min))
        C2 --> D1
        C5 --> D1
    end

    subgraph Liaison
        D1 --> E1(Mélange)
        B1 -- Beurre, Crème fraiche --> E1
        B2 -- Farine, Fond de volaille, Assaisonnement --> E1
    end

    E1 --> F1(Refroidissement)
    F1 --> G1(Maintien au froid)
    G1 --> H1(Réchauffage)
    H1 --> I1(Maintien au chaud)
    H1 --> I2(Remise au client)