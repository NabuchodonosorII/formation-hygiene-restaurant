``` mermaid
graph TD
    subgraph Réception / Stockage
        A1[Mayonnaise] --> B1(Froid positif)
        A2[Tomates fraiches] --> B1
        A3[Œufs coquilles frais] --> B1
        A4[Jambon entier] --> B1
        A5[Cornichons pot non entamé] --> B2(Température ambiante)
        A6[Pommes de terre] --> B2
        A7[Assaisonnement] --> B2
    end

    subgraph Mise en place
        B1 -- Tomates fraiches --> C1(Lavage)
        C1 --> C2(Découpe)
        B1 -- Œufs --> C3(Cuisson 90-100°C : 10 min)
        C3 --> C4(Refroidissement)
        C4 --> C5(Ecalage / Découpe)
        B1 -- Jambon entier --> C6(Découpe)
        B2 -- Cornichons --> C7(Déconditionnement)
        C7 --> C8(Egouttage / Découpe)
        B2 -- Pommes de terre --> C9(Lavage)
        C9 --> C10(Cuisson 90-100°C : 30-45 min)
        C10 --> C11(Refroidissement)
        C11 --> C12(Epluchage / Découpe)
    end

    subgraph Assemblage
        A1 -- "cf. fiche Mayonnaise" --> D1(Assemblage)
        C2 --> D1
        C5 --> D1
        C6 --> D1
        C8 --> D1
        C12 --> D1
        B2 -- Assaisonnement --> D1
    end

    D1 --> E1(Remise au client)
```