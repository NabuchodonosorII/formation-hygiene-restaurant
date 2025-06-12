graph TD
    subgraph Réception / Stockage
        A1[Beurre] --> B1(Froid positif)
        A2[Viande de veau fraiche] --> B1
        A3[Fond brun de veau] --> B1
        A4[Champignons frais] --> B2(Température ambiante)
        A5[Tomates] --> B2
        A6[Oignons, ail] --> B2
        A7[Vin blanc] --> B2
    end

    subgraph Mise en place
        B1 -- Viande --> C1(Parage)
        C1 --> C2(Rissolage)
        B1 -- Beurre --> C2
        
        B2 -- Champignons --> C3(Découpe des pieds sablonneux)
        C3 --> C4(Lavage / égouttage)
        C4 --> C5(Cuisson (90°C : 5 min))

        B2 -- Tomates --> C6(Lavage / égouttage)
        C6 --> C7(Concassage)
        B2 -- Oignons, ail --> C8(Epluchage)
        C8 --> C9(Hachage)
    end

    subgraph Cuisson principale
        C2 --> D1(Cuisson (95°C : 45 min))
        B1 -- "Cf. fiche fond brun de veau" --> D1
        B2 -- Vin blanc --> D1
        C7 --> D1
        C9 --> D1
    end

    subgraph Assemblage
        D1 --> E1(Assemblage)
        C5 --> E1
    end

    E1 --> F1(Refroidissement)
    F1 --> G1(Maintien au froid)
    G1 --> H1(Réchauffage)
    H1 --> I1(Maintien au chaud)
    H1 --> I2(Remise au client)