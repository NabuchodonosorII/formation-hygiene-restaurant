graph TD
    subgraph Réception / Stockage
        A1[Huile] --> B1(Température ambiante)
        A2[Assaisonnement] --> B1
        A3[Moutarde et Ketchup (pot non entamé), Tabasco] --> B1
        A4[Oignons] --> B1
        A5[Câpres conserve] --> B1
        A6[Plantes aromatiques, jus de citron] --> B2(Froid positif)
        A7[Œufs coquilles extra-frais] --> B2
        A8[Viande de bœuf] --> B2
    end

    subgraph Mise en place
        B1 -- Oignons --> C1(Epluchage)
        C1 --> C2(Découpe)
        B1 -- Câpres --> C3(Déconditionnement)
        C3 --> C4(Egouttage)
        B2 -- Plantes aromatiques --> C5(Lavage/égouttage)
        C5 --> C6(Hachage)
        B2 -- Œufs --> C7(Cassage)
        C7 --> C8(Clarification)
        C8 --> C9(Réservation des jaunes)
        B2 -- Viande --> C10(Parage)
        C10 --> C11(Découpe)
        C11 --> C12(Hachage)
    end
    
    subgraph Assemblage
        B1 -- Huile, Assaisonnement, Moutarde, etc. --> D1(Mélange)
        C2 --> D1
        C4 --> D1
        C6 --> D1
    end

    subgraph Façonnage / Remise au client
        D1 --> E1(Façonnage)
        C9 --> E1
        C12 --> E1
        E1 --> E2(Remise au client immédiate)
    end