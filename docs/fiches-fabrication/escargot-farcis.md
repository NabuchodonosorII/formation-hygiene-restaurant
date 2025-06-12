graph TD
    subgraph Réception / Stockage
        A1[Beurre] --> B1(Froid positif)
        A2[Persil] --> B2(Température ambiante)
        A3[Assaisonnement] --> B2
        A4[Ail, Echalotes] --> B2
        A5[Coquilles d'escargots] --> B2
        A6[Escargots en conserve] --> B2
    end

    subgraph Mise en place
        B1 -- Beurre --> C1(Découpe)
        B2 -- Persil --> C2(Lavage / égouttage)
        C2 --> C3(Hachage)
        B2 -- Ail, Echalotes --> C4(Epluchage)
        C4 --> C5(Découpe)
        B2 -- Coquilles --> C6(Lavage / égouttage)
        B2 -- Escargots --> C7(Déconditionnement)
    end

    subgraph Beurre d'escargot
        C1 --> D1(Mélange)
        C3 --> D1
        C5 --> D1
        B2 -- Assaisonnement --> D1
    end

    subgraph Assemblage
        D1 --> E1(Assemblage)
        C6 --> E1
        C7 --> E1
        E1 --> F1(Maintien au froid)
    end
    
    F1 --> G1(Cuisson (180°C : 10 min))
    G1 --> H1(Remise au client)