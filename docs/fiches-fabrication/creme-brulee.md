graph TD
    subgraph Réception / Stockage
        A1[Œufs] --> B1(Froid positif)
        A2[Crème] --> B1
        A3[Gousses de vanille] --> B2(Température ambiante)
        A4[Lait] --> B2
    end

    subgraph Mise en place
        B1 -- Oeufs --> C1(Cassage)
        C1 --> C2(Séparation des jaunes)
        B2 -- Vanille --> C3(Extraction des graines)
    end

    subgraph Assemblage et Cuisson
        B2 -- Lait --> D1(Ebullition)
        C3 --> D1
        D1 --> D2(Mélange)
        C2 --> D2
        B1 -- Crème --> D2
        D2 --> D3(Conditionnement)
        D3 --> D4(Cuisson (90°C : 90 min))
        D4 --> D5(Refroidissement)
    end

    subgraph Finition
        D5 --> E1(Maintien au froid)
        E1 --> E2(Effet chalumeau)
        E2 --> F1(Remise au client)
    end