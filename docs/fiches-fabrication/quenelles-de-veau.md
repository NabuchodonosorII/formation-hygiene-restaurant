graph TD
    subgraph Réception / Stockage
        A1[Jaune d'œuf (ovoproduit)] --> B1(Froid positif)
        A2[Beurre] --> B1
        A3[Escalope de veau] --> B1
        A4[Blanc d'œuf] --> B1
        A5[Assaisonnement, Echalotes] --> B2(Température ambiante)
        A6[Farine] --> B2
        A7[Lait entamé] --> B2
    end

    subgraph Mise en place
        B1 -- Escalope de veau --> C1(Hachage / mixage)
    end

    subgraph Panade
        B2 -- Farine, Lait --> D1(Cuisson)
        D1 --> D2(Desséchage)
        D2 --> D3(Fabrication de la panade : Mélange)
        B2 -- Assaisonnement, Echalotes --> D3
        B1 -- Jaune d'oeuf, Beurre --> D3
        D3 --> D4(Refroidissement)
    end
    
    subgraph Appareil
        D4 --> E1(Mélange à froid)
        C1 --> E1
        B1 -- Blanc d'oeuf --> E1
    end

    subgraph Cuisson
        E1 --> F1(Façonnage)
        F1 --> F2(Pochage (jusqu'à flottement) / égouttage)
        F2 --> F3(Refroidissement)
        F3 --> F4(Maintien au froid)
    end

    F4 --> G1(Utilisation)