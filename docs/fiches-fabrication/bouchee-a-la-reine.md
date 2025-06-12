graph TD
    subgraph Réception / Stockage
        A1[Pâte feuilletée] --> B1(Froid négatif)
        A2[Quenelles] --> B2(Froid positif)
        A3[Fond brun de veau] --> B2
        A4[Carottes, Poireau, Céleri] --> B2
        A5[Champignons] --> B2
        A6[Ris de veau] --> B2
        A7[Vin blanc] --> B3(Température ambiante)
        A8[Farine] --> B3
        A9[Beurre, Crème fraiche] --> B2
        A10[Jaune d'œuf en brique] --> B2
    end

    subgraph Mise en place
        B1 -- "cf. fiche Pâte feuilletée" --> C1(Façonnage / dorure)
        A10 --> C1
        C1 --> C2(Cuisson (180°C : 25 min))
        C2 --> C3(Refroidissement)
        
        B2 -- Quenelles "cf. fiche Quenelles de veau" --> D1
        
        B2 -- Fond brun "cf. fiche Fond brun de veau" --> D2

        B2 -- Légumes --> C4(Epluchage)
        C4 --> C5(Lavage / Egouttage)
        C5 --> C6(Découpe)

        B2 -- Champignons --> C7(Découpe des pieds terreux)
        C7 --> C8(Lavage / Egouttage)
        C8 --> C9(Découpe)

        B2 -- Ris de veau --> C10(Dégorgement / égouttage)
        C10 --> C11(Blanchiment)
        C11 --> C12(Parage et Elimination peau et nerfs)
        C12 --> C13(Cuisson (110°C : 20 min))
        C13 --> C14(Refroidissement)
        C14 --> C15(Découpe des ris)
    end

    subgraph Sauce
        B3 -- Vin, Farine --> E1(Fabrication de la sauce : Mélange / Cuisson)
        B2 -- Beurre, Crème fraiche --> E1
        D2 --> E1
    end

    subgraph Assemblage
        E1 --> F1(Assemblage)
        D1 --> F1
        C6 --> F1
        C9 --> F1
        C15 --> F1
    end

    F1 --> G1(Réchauffage)
    G1 --> H1(Maintien au chaud)
    G1 --> I1(Remise au client)
    C3 --> I1