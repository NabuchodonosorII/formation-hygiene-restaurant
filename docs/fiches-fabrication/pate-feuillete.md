graph TD
    subgraph Réception / Stockage
        A1[Sel] --> B1(Température ambiante)
        A2[Farine] --> B1
        A3[Eau] --> B1
        A4[Beurre] --> B2(Froid positif)
    end

    subgraph Mise en place
        B2 --> C1(Découpe)
    end

    subgraph Techniques culinaires
        B1 -- Sel, Farine, Eau --> D1(Détrempe / Boulage)
        D1 --> D2(Repos (3°C))
        D2 --> D3(Beurrage / Feuilletage)
        C1 --> D3
        D3 --> D4(Repos (3°C))
        D4 --> D5(Division / moulage)
        D5 --> D6(Congélation et maintien au froid)
        D6 --> D7(Utilisation)
    end