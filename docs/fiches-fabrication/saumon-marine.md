graph TD
    subgraph Réception / Stockage
        A1[Plantes aromatiques] --> B1(Température ambiante)
        A2[Huile] --> B1
        A3[Assaisonnements] --> B1
        A4[Saumon frais entier habillé] --> B2(Froid positif)
        A5[Citron entier] --> B2
    end

    subgraph Mise en place
        B1 -- Plantes aromatiques --> C1(Lavage / Egouttage)
        C1 --> C2(Découpe)
        B2 -- Saumon --> C3(Filetage)
        C3 --> C4(Désarêtage)
        C4 --> C5(Pelage / parage)
        C5 --> C6(Rinçage / Essuyage)
        C6 --> C7(Tranchage)
        B2 -- Citron --> C8(Lavage)
        C8 --> C9(Découpe)
    end

    subgraph Techniques culinaires
        B1 -- Huile, Assaisonnements --> D1(Fabrication marinade)
        C2 --> D1
        C9 --> D1
        C7 --> D2(Marinage (<3°C, durant maximum 2 jours))
        D1 --> D2
        D2 --> D3(Pressage)
        D3 --> D4(Maintien au froid)
    end

    D4 --> E1(Remise au client)